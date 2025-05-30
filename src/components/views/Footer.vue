<template>
  <footer class="footer">
    <button @click="downloadPDF">Скачать PDF</button>
  </footer>
</template>

<script setup>
import html2canvas from 'html2canvas'
import jsPDF from 'jspdf'

async function downloadPDF() {
  const el = document.querySelector('.brandbook')
  const canvas = await html2canvas(el, { scale: 2, useCORS: true })

  const imgData = canvas.toDataURL('image/png')

  const pdf = new jsPDF('p', 'mm', 'a4')
  const pageWidth = pdf.internal.pageSize.getWidth()
  const pageHeight = pdf.internal.pageSize.getHeight()

  const imgWidth = pageWidth
  const imgHeight = (canvas.height * imgWidth) / canvas.width

  let heightLeft = imgHeight
  let position = 0

  pdf.addImage(imgData, 'PNG', 0, position, imgWidth, imgHeight)
  heightLeft -= pageHeight

  while (heightLeft > 0) {
    position = heightLeft - imgHeight
    pdf.addPage()
    pdf.addImage(imgData, 'PNG', 0, position, imgWidth, imgHeight)
    heightLeft -= pageHeight
  }

  pdf.save('brandbook.pdf')
}

</script>

<style scoped>
.footer {
  text-align: center;
  margin: 60px auto 20px;
}

button {
  background-color: #e94560;
  color: #fff;
  border: none;
  padding: 12px 24px;
  font-size: 16px;
  border-radius: 8px;
  cursor: pointer;
  transition: 0.2s ease;
}

button:hover {
  background-color: #c7304b;
}
</style>
