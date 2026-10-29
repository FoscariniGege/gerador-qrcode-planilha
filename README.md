# 🏷️ Gerador de Etiquetas Térmicas com QR Code (Padrão Argox / WMS)

Automação em Python (desenvolvida para Google Colab) que lê planilhas de endereçamento e produtos do **Google Drive**, gera **QR Codes** dinâmicos para cada registro e compila um arquivo **PDF diagramado milimetricamente para impressoras térmicas Argox (101,6 mm x 25,4 mm)**.

---

## 🎯 Problema de Negócio Resolvido

Em operações de estoque e **WMS (Warehouse Management System)**, a criação manual de etiquetas de endereçamento, prateleiras ou SKUs a partir de planilhas consome horas de trabalho e frequentemente gera erros de formatação na impressora térmica.

Este script automatiza todo o fluxo: lê os códigos diretamente da planilha no Google Drive, renderiza os QR Codes com margem otimizada, posiciona o código legível ao lado e entrega o PDF pronto para envio direto à fila de impressão térmica.

---

## ⚡ Destaques Técnicos da Solução

* **Diagramação Milimétrica para Hardware (`ReportLab`):** Canvas configurado nas dimensões exatas de etiquetas térmicas padrão 4"x1" (`101.6 mm` de largura por `25.4 mm` de altura), garantindo alinhamento preciso do sensor da impressora a cada avanço de página (`showPage()`).
* **Controle de Layout e Tipografia:** Renderização do QR Code em proporção quadrada (`21.8 mm x 21.8 mm`) combinada com texto em `Helvetica-Bold
