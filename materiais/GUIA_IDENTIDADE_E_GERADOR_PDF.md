# Manual de Identidade Visual & Arquitetura do Gerador de PDFs
## Jefferson Pizzio Advisory (`jeffersonpizzio.com`)

Este documento consolida o guia de estilo visual oficial de **Jefferson Pizzio Advisory** e a especificação técnica para geração e exportação de materiais (One-Pager, Deck Institucional e Guias Autoexplicativos), além da base de arquitetura para a futura automação de relatórios e propostas personalizadas.

---

## 1. Identidade Visual da Marca (Brand Book Essencial)

### 1.1 Assinatura e Tipografia da Marca
A marca adota o conceito de *Quiet Luxury* (luxo silencioso e sóbrio), afastando-se deliberadamente de designs genéricos, cores fluorescentes ou clichês visuais de marketing digital de varejo.

* **Tipografia Principal da Marca**: `Cormorant Garamond` (Google Fonts), em caixa alta com kerning/tracking expandido:
  ```
  J E F F E R S O N   P I Z Z I O
  A D V I S O R Y
  ```
* **Tipografia Secundária / Técnica**: `IBM Plex Mono` (para numeração de seções, notas de rodapé, métricas e selos de jurisdição: `01 · DIAGNÓSTICO`, `02 · ARQUITETURA`).
* **Tipografia de Leitura / Corpo**: `Plus Jakarta Sans` ou `Inter` (para textos corridos, tabelas e propostas, garantindo legibilidade nítida e neutra).

---

### 1.2 Paleta Cromática Oficial

| Nome da Cor | Hexadecimal | RGB | Aplicação Principal |
| :--- | :--- | :--- | :--- |
| **Midnight Navy** | `#09121D` / `#0A1420` | `10, 20, 32` | Fundo principal da landing page e capas de materiais |
| **Surface Deep Blue** | `#0E1A2A` / `#132236` | `14, 26, 42` | Fundo de cartões, formulários e lâminas de slides |
| **Champagne Gold (Primário)** | `#C5A880` | `197, 168, 128` | Linhas divisórias, números, botões CTA e detalhes de prestígio |
| **Light Champagne** | `#DFCAAA` | `223, 202, 170` | Textos em ênfase itálica e títulos secundários |
| **Linen Off-White** | `#F6F4EE` | `246, 244, 238` | Títulos principais e textos de destaque (papel linho nobre) |
| **Slate Gray (Muted)** | `#9BB0C7` | `155, 176, 199` | Textos corridos, parágrafos explicativos e legendas |
| **Gold Border Subtle** | `rgba(197,168,128,0.24)` | — | Molduras ultrafinas de cards e caixas de dados |

---

## 2. As Fotografias Tratadas (Galeria de Imagens)

As fotos originais do Jefferson (que continham o logotipo da instituição anterior "Safra Invest" e estrelas na parede de fundo) foram processadas e salvas em `/assets/images/`:

1. **Retratos em Fundo de Estúdio Executivo Escuro (`.jpg`)**:
   * `jefferson_pizzio_portrait_1_studio.jpg`: Postura frontal, terno azul marinho, iluminação de estúdio suave com degradê navy. Aplicada na Hero da Landing Page e na Capa dos Materiais.
   * `jefferson_pizzio_portrait_2_studio.jpg`: Postura com braços soltos, sorriso confiante. Aplicada na seção "Sobre Jefferson Pizzio" da Landing Page.
   * `jefferson_pizzio_portrait_3_studio.jpg` e `jefferson_pizzio_portrait_4_studio.jpg`: Variações adicionais prontas para posts no LinkedIn, artigos e apresentações.
2. **Retratos com Fundo Transparente (`.png`)**:
   * `jefferson_pizzio_portrait_1.png` a `4.png`: Recorte com canal alfa (transparente), permitindo aplicação direta sobre qualquer fundo escuro ou vetor sem perda de qualidade.

---

## 3. Ecossistema de Materiais Criados

Todos os arquivos estão prontos para uso em `/home/volneis/Documents/Projeto Jeff/`:

| Arquivo | Destinatário | Finalidade |
| :--- | :--- | :--- |
| `landing-page/index.html` | Clientes e Parceiros (`jeffersonpizzio.com`) | Presença digital oficial de alta conversão para agendamento de "Reunião Consultiva". |
| `materiais/one-pager-parceiros.html` | Advogados tributaristas, contadores, M&A | Folha A4 única explicando a parceria sem conflito de interesse. |
| `materiais/guia-liquidez-sucessoria.html` | Famílias empresárias e sócios | Guia autoexplicativo de 3 páginas com simulação de custos do inventário e apólice internacional. |
| `materiais/deck-institucional.html` | Reuniões formais (presencial / Zoom) | Apresentação em slides 16:9 navegável por teclado com as 7 lâminas institucionais. |

---

## 4. Como Exportar os Arquivos para PDF em Alta Resolução

Todos os materiais foram desenvolvidos com estilos de impressão vetorial nativos (`@media print` e `@page`):

1. Abra qualquer um dos arquivos HTML no navegador Google Chrome / Brave / Edge.
2. Pressione **Ctrl + P** (ou Cmd + P no Mac).
3. Na janela de impressão:
   * **Destino**: `Salvar como PDF`.
   * **Layout**: Retrato (para o One-Pager e Guia) ou Paisagem (para o Deck).
   * **Mais definições**:
     * Tamanho do papel: `A4`.
     * Margens: `Nenhuma` ou `Mínima`.
     * **Gráficos de segundo plano**: **Marcar a caixa [X]** (para preservar as cores escuras e os tons dourados).
4. Clique em **Salvar**. O PDF gerado terá tipografia vetorial perfeita, sem serrilhados, pronto para envio pelo WhatsApp ou impressão gráfica.

---

## 5. Arquitetura para o Futuro "Gerador de PDFs Personalizados"

Para evoluir este ecossistema para um gerador automatizado onde o Jefferson insira os dados de um cliente e gere uma proposta/relatório com 1 clique:

### 5.1 Estrutura de Dados (Exemplo de Entrada JSON):
```json
{
  "cliente": {
    "nome_familia": "Família Albuquerque",
    "patrimonio_total": 35000000,
    "empresas": ["Metalúrgica Alfa Ltda", "Agropecuária Sul S/A"],
    "custo_inventario_projetado": 4900000
  },
  "solucao_proposta": {
    "apolice_internacional_usd": 1000000,
    "moeda": "USD",
    "jurisdicao": "Porto Rico / Cayman",
    "rating_seguradora": "A+ Superior"
  }
}
```

### 5.2 Motor de Renderização Sugerido:
* Uma interface web simples (ou script em Node.js / Python) que preenche um template HTML pré-formatado com a identidade visual da Jefferson Pizzio Advisory e converte para PDF usando o Chrome Headless (`google-chrome --headless --print-to-pdf`).
* Isso garantirá propostas sob medida com design de Private Bank em menos de 10 segundos.
