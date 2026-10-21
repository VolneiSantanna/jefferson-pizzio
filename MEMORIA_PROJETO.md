# 🏛️ MEMÓRIA MESTRA DO PROJETO — JEFFERSON PIZZIO ADVISORY

> **Aviso para Novos Agentes / Novas Sessões**:  
> Este documento consolida 100% das decisões de negócio, regras de compliance, identidade visual, estrutura técnica e o estado de todas as ferramentas desenvolvidas para **Jefferson Pizzio Advisory**. Leia atentamente este documento antes de realizar qualquer alteração no código.

---

## 1. Dados Oficiais & Posicionamento

* **Nome do Profissional**: Jefferson Pizio dos Santos (Nome Comercial: **Jefferson Pizzio**)
* **Marca Oficial**: **JEFFERSON PIZZIO | WEALTH & SUCCESSION ADVISORY**
* **Registro Profissional Oficial**: Corretor de Seguros habilitado pela Escola de Negócios e Seguros (ENS), aprovado no 75º Exame de Corretores de Seguros (Todos os Ramos) e registrado sob o nº **0335448** perante a SUSEP (Superintendência de Seguros Privados).
* **Canais de Contato**:
  - E-mail institucional: `consultor@jeffersonpizzio.com`
  - WhatsApp de atendimento: `(51) 99897-0838`
  - Base de atuação: Porto Alegre / RS (com atendimento nacional e internacional)
* **Domínio Oficial em Produção**: [https://jeffersonpizzio.com](https://jeffersonpizzio.com) (aliased com HTTPS na Vercel).
  - Canônica preferencial: `https://jeffersonpizzio.com/` (sem `www` e com `cleanUrls: true`).
  - Redirecionamento 301 permanente ativo: `www.jeffersonpizzio.com` redireciona via HTTP 301 para `https://jeffersonpizzio.com`.
  - Redirecionamento 308 permanente ativo: URLs com sufixo `.html` redirecionam para URLs limpas (ex: `/index.html` → `/`).
* **Repositório Git**: `https://github.com/VolneiSantanna/jefferson-pizzio.git` (branch `main`).

---

## 2. Regras Críticas de Compliance & Restrições (INVIOLÁVEIS)

1. ⚠️ **PROIBIÇÃO ABSOLUTA DE MARCAS E NOMES ESPECÍFICOS DE TERCEIROS**:
   - **NUNCA** utilizar no site, apresentações, códigos ou documentos os nomes:
     - ❌ `Grupo Origem`
     - ❌ `Banco Safra`
     - ❌ `Escritórios da XP` / `XP Investimentos`
   - **Motivo**: O profissional não possui autorização contratual para utilização dessas marcas comerciais.
   - **Como citar a trajetória passada**: Usar expressões institucionais elegantes e generalizadas:
     - ✅ *"ecossistemas e escritórios vinculados a instituições financeiras de primeira linha"*
     - ✅ *"ecossistemas líderes de assessoria patrimonial e private banking"*
     - ✅ *"Ecossistemas Financeiros de Primeira Linha"*

2. 🛡️ **Postura Consultiva e Ausência de Promessas Absolutas**:
   - Não utilizar expressões como *"garantimos caixa imediato"* ou *"blindagem absoluta"*.
   - Usar: *"estruturamos caixa em moeda forte e regras claras para que seu patrimônio e sua empresa atravessem a transição com segurança"*, *"planejamento tributário eficiente"*, *"preservação patrimonial"*.

3. ⚖️ **Relação com Advogados e Contadores**:
   - Jefferson Pizzio Advisory **não presta assessoria jurídica nem contábil** e não concorre com as bancas de confiança dos clientes.
   - Atua exclusivamente como braço técnico em liquidez sucessória, seguros internacionais de alta capacidade e gestão de riscos patrimoniais.

4. 📄 **Aviso Legal SUSEP Obrigatório no Rodapé**:
   > *"Jefferson Pizzio Advisory — Corretor de seguros habilitado pela ENS e registrado sob o nº 0335448 (Processo SUSEP). As informações deste site têm caráter informativo e não constituem oferta, recomendação de investimento ou consultoria jurídica ou tributária. Coberturas, prazos e condições dependem de cada apólice e de análise de aceitação pela seguradora. Produtos de investimento são distribuídos por meio de instituições autorizadas."*

---

## 3. Identidade Visual & Design System (Quiet Luxury)

* **Conceito**: *Quiet Luxury* (luxo discreto, refinamento institucional, paleta escura profunda com toques de ouro nobre, tipografia límpida e alto contraste de leitura).
* **Paleta de Cores**:
  - Fundo Geral: `--bg-dark: #08111C`
  - Superfícies / Seções Alternadas: `--bg-surface: #0D1A2B`
  - Cards e Painéis: `--bg-card: #122238` (hover: `#172C48`)
  - Ouro Primário: `--gold-primary: #C5A880`
  - Ouro Claro: `--gold-light: #DFC9AB`
  - Ouro Escuro / Bordas: `--gold-dark: #8C6F47` / `--gold-border: rgba(197, 168, 128, 0.20)`
  - Texto Principal: `--text-main: #F6F4EE`
  - Texto de Parágrafos / Contraste Elevado: `--text-muted: #B8C2D4`
  - Texto Suave / Metadados: `--text-dim: #60758B` ou `#7E92A8`
* **Tipografia**: `'Plus Jakarta Sans', system-ui, sans-serif` (pesos 300 a 700).
* **Regras de Estilo**:
  - `text-wrap: balance;` nos títulos dos cards.
  - Parágrafos de leitura em `#B8C2D4` para excelente legibilidade sobre o azul marinho profundo.
* **Fotos de Estúdio Oficiais** (tratadas, com iluminação quente de estúdio e sem logos antigos):
  - `assets/images/jefferson_pizzio_portrait_1_studio.jpg` (Hero / Retrato Principal)
  - `assets/images/jefferson_pizzio_portrait_2_studio.jpg` (Seção Sobre / Trajetória)
  - `assets/images/jefferson_pizzio_signature_gold.png` (Assinatura Manuscrita Dourada)
  - `assets/images/og-share-card.jpg` (Card oficial de compartilhamento WhatsApp/LinkedIn)

---

## 4. Mapa da Estrutura de Arquivos & Ferramentas

```
/home/volneis/Documents/Projeto Jeff/
├── index.html                     # Landing page principal em produção
├── privacidade.html               # Página dedicada de Política de Privacidade (LGPD)
├── landing-page/
│   ├── index.html                 # Cópia 100% sincronizada da landing page
│   └── privacidade.html           # Cópia 100% sincronizada da política de privacidade
├── materiais/
│   ├── gerador-documentos.html    # Criador didático de documentos PDF (Estúdio A4 Split)
│   ├── assinatura-email.html      # Criador oficial de assinatura de e-mail (Outlook/GoDaddy)
│   ├── deck-institucional.html    # Apresentação institucional executiva em slides
│   ├── one-pager-parceiros.html   # One-pager para escritórios de advocacia e contabilidade
│   ├── contrato-parceria.html     # Contrato oficial de parceria e indicação (6 páginas A4 Quiet Luxury)
│   ├── guia-liquidez-sucessoria.html # Guia executivo sobre liquidez no inventário
│   ├── mercado-internacional.html # Guia sobre diversificação e moeda forte offshore
│   └── GUIA_IDENTIDADE_E_GERADOR_PDF.md # Manual técnico do gerador de documentos
├── assets/
│   └── images/                    # Fotos tratadas, logos e cards de compartilhamento
└── MEMORIA_PROJETO.md             # ESTE DOCUMENTO MESTRE DE MEMÓRIA
```

---

## 5. Detalhamento das Páginas e Ferramentas

### 5.1. Landing Page Principal (`index.html`)
* **Header**: Marca minimalista, menu desktop (`Especialidades`, `Metodologia`, `Parcerias`, `Sobre`, dropdown `Materiais`), botão dourado `Agendar Reunião`, e drawer mobile lateral responsivo.
* **Hero**: Título focado em *Preservação patrimonial, liquidez sucessória e proteção societária*, foto tratada e CTA de alta conversão.
* **Diagnóstico de Mercado**: 3 cards técnicos abordando liquidez no ITCMD progressivo (até 8%), acordo de compra e venda de quotas e concentração em risco Brasil.
* **6 Especialidades (Grid 2x3)**:
  1. *Liquidez Sucessória em Moeda Forte* (A+ A.M. Best)
  2. *Proteção Societária & Acordo entre Sócios (Buy-Sell)*
  3. *Seguro de Homem-Chave & Riscos Corporativos*
  4. *Governança Patrimonial & Sucessão Transfronteiriça*
  5. *Seguro Saúde Internacional* (Johns Hopkins, Mayo Clinic, Cleveland Clinic, rede premium)
  6. *Previdência & Investimentos Internacionais* (acumulação em jurisdições de alta solidez)
* **Modelo de Parcerias**: Atuação complementar e respeito às bancas de confiança da família.
* **Metodologia (4 Etapas)**: Diagnóstico Confidencial, Mapeamento de Gargalos, Desenho Sob Medida, Implantação & Revisão.
* **Sobre Jefferson Pizzio**: Mais de 25 anos corporativos, atuação em instituições de primeira linha, consultoria independente.
* **Modal de Agendamento**:
  - Campos: Nome, WhatsApp, E-mail, Assunto (8 opções alinhadas às especialidades) e Mensagem opcional.
  - Checkbox de consentimento obrigatório para a Lei Geral de Proteção de Dados (LGPD).
  - Envio direto e formatado para o WhatsApp com confirmação.
* **Rodapé**: Links completos, Política de Privacidade e Aviso Legal com registro SUSEP nº 0335448.

### 5.2. Política de Privacidade (`privacidade.html`)
* Desenvolvida especificamente para a LGPD (Lei nº 13.709/2018).
* Identifica Jefferson Pizio dos Santos como Controlador (SUSEP 0335448).
* Trata sobre minimização de dados, bases legais (art. 7º, V e IX), direitos do titular (art. 18), sigilo absoluto e canais diretos do encarregado (DPO).

### 5.3. Criador de Documentos Executivos em PDF (`materiais/gerador-documentos.html`)
* **URL online**: `https://jeffersonpizzio.com/materiais/gerador-documentos`
* **Arquitetura Studio Split**:
  - O cabeçalho e a barra de passos didáticos são **fixos no topo**.
  - O editor à esquerda e a visualização A4 à direita possuem **rolagem independente**, impedindo cortes na tela ou vazios pretos ao rolar páginas adicionais.
  - **Barra flutuante de navegação e zoom** (`−`, `100%`, `+`, `📄 Folha 1`, `📄 Folha 2`).
  - **Divisores visuais automáticos** de início de folha no editor (`✂️ Início da Folha 2`).
  - **Algoritmo anti-títulos órfãos**: se o conteúdo desce para a folha seguinte, o título correspondente acompanha.
  - **Suporte a blocos flexíveis**: Títulos, Parágrafos, Destaques dourados, Tabelas customizáveis (linhas x colunas), Imagens (upload e colar via `Ctrl+V`), e Assinatura oficial posicionada no fechamento do documento.
  - **Exportação limpa**: regras de impressão `@media print` otimizadas para exportação multipáginas em PDF nítido.

### 5.4. Criador de Assinatura de E-mail (`materiais/assinatura-email.html`)
* **URL online**: `https://jeffersonpizzio.com/materiais/assinatura-email`
* Gera assinatura em HTML em linha (`table-based`) compatível com todos os clientes de e-mail (Outlook Desktop, Outlook Web, Apple Mail, Webmail GoDaddy, Gmail, Thunderbird).
* Inclui botão didático de cópia com um clique e guias passo a passo de configuração ilustrados para **Outlook** e **GoDaddy Webmail**.

---

## 6. Fluxo de Trabalho, Versionamento & Deploy

* **Comandos de Deploy**:
  1. Sempre verificar se há alterações pendentes: `git status`
  2. Adicionar arquivos: `git add .`
  3. Commitar: `git commit -m "tipo: descricao clara"`
  4. Enviar para GitHub: `git push origin main`
  5. Deploy na Vercel:
     `npx vercel --prod --token $VERCEL_TOKEN --yes`
* **Sincronização Obrigatória**:
  - Toda alteração em `index.html` deve ser copiada para `landing-page/index.html`.
  - Toda alteração em `privacidade.html` deve ser copiada para `landing-page/privacidade.html`.

---

## 7. Instrução de Continuidade (Para Novas Sessões)

Ao iniciar uma nova sessão ou caso de uso, utilize o seguinte prompt para carregar o contexto completo:

```text
Olá! Estamos dando continuidade ao projeto Jefferson Pizzio Advisory.
Por favor, leia atentamente o arquivo MEMORIA_PROJETO.md na raiz do repositório para carregar todo o histórico, regras de compliance (especialmente a proibição absoluta de marcas de terceiros), padrão visual Quiet Luxury, páginas existentes e o estado atual de produção antes de iniciarmos qualquer nova tarefa.
```
