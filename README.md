# 🌾 Stardew Valley • Desafio de Pegar Todos os Itens (All Items Tracker)

Uma ferramenta web leve, rápida e visualmente tematizada para rastrear o progresso do **Desafio de Pegar Todos os Itens (All Items Challenge)** em **Stardew Valley** (compatível com a versão **1.6**).

Desenvolvida em um **único arquivo HTML (`index.html`)** com **jQuery**, pronta para ser hospedada diretamente no **GitHub Pages** sem necessidade de compilação ou backend.

---

## ✨ Funcionalidades

- **📦 Leitura Completa de Contêineres:**
  - Analisa **todos os baús** espalhados pela fazenda e outros mapas (Mina, Caverna da Caveira, Praia, Ilha Gengibre, celeiros, galinheiros, etc.).
  - Analisa o **inventário do jogador** e **itens equipados** (chapéus, botas, anéis e bugigangas da 1.6).
  - Analisa **geladeiras** da casa da fazenda e da cabana da ilha.
- **🏷️ Catálogo Completo com 1.030+ Itens:**
  - Base de dados e imagens integradas a partir da biblioteca [`stardew-valley-data`](https://github.com/chiefpansancolt/stardew-valley-data).
  - Inclui Culturas, Peixes, Artefatos, Minerais, Culinária, Criação (Crafting), Produtos Artesanais, Armas, Chapéus, Calçados, Anéis, Bugigangas (Trinkets 1.6), Ferramentas e Itens Especiais.
- **📊 Overview do Fazendeiro & Progresso:**
  - Barra de progresso global com contadores (Coletados vs Faltando) e percentual.
  - Cartões por categoria com barra de progresso individual e clique para filtrar.
  - Alternância entre **"🌐 Desafio Completo"** e **"🏆 Apenas Coleções Oficiais (Perfeição)"**.
- **📍 Onde está guardado?**
  - Ao inspecionar qualquer item coletado, o sistema mostra exatamente em quais baús e coordenadas o item está armazenado (ex: `Fazenda • Baú (67, 15) x 12`, `Inventário x 5`).
- **🔍 Filtros e Busca Rápida:**
  - Abas: **❌ Faltando (Missing)**, **🌟 Todos** e **✅ Coletados**.
  - Campo de busca instantânea por nome ou categoria.
  - Ordenação por Nome (A-Z, Z-A), Categoria, Preço de Venda e Quantidade.
- **📋 Exportação & Compartilhamento:**
  - Botão **"Copiar Faltantes"** para gerar uma checklist em Markdown pronta para Bloco de Notas ou Discord.
  - Botão **"Exportar CSV"** para download do relatório completo em planilha.
- **🌾 Save de Teste Integrado:**
  - Botão **"Carregar Save de Teste (MiniFazenda)"** para demonstrar a aplicação imediatamente usando o save `MiniFazenda_450568833` incluído no repositório.

---

## 🚀 Como Executar Localmente

Como a aplicação é construída em um único arquivo HTML estático, basta abrir o arquivo ou rodar um servidor HTTP local simples:

### Opção 1: Servidor HTTP Local (Recomendado para testar o save de demonstração)
```bash
npx serve -l 3000 .
```
Ou com Python:
```bash
python -m http.server 3000
```
Em seguida, acesse no navegador: `http://localhost:3000`.

### Opção 2: Abrir diretamente
Dê dois cliques no arquivo `index.html` para abrir diretamente no seu navegador.  
*(Nota: Para carregar o save de demonstração via `file://`, use o botão "Selecionar Arquivo de Save" e selecione `MiniFazenda_450568833`)*.

---

## 🌐 Publicação no GitHub Pages

A aplicação foi projetada para rodar nativamente no **GitHub Pages**:

1. Suba este repositório para o seu GitHub.
2. No repositório, acesse **Settings** > **Pages**.
3. Na seção **Build and deployment**:
   - **Source:** Selecione `Deploy from a branch`
   - **Branch:** Selecione `main` (ou `master`) e pasta `/ (root)`
   - Clique em **Save**.
4. Em poucos segundos seu site estará no ar na URL do GitHub Pages (ex: `https://seu-usuario.github.io/StardewValleyDesafioTodosItems/`).

*(Também incluímos um workflow em `.github/workflows/deploy.yml` para deploy automático via GitHub Actions caso prefira).*

---

## 📂 Onde Encontrar o Save do Stardew Valley

- **Windows:** Pressione `Win + R`, digite `%AppData%\StardewValley\Saves` e dê Enter.
- **Mac:** `~/.config/StardewValley/Saves`
- **Linux:** `~/.config/StardewValley/Saves`

Basta arrastar a pasta ou o arquivo do seu save para a página!

---

## 🛠️ Tecnologias Utilizadas

- **HTML5 & CSS3:** Interface responsiva inspirada no visual aconchegante de Stardew Valley.
- **jQuery 3.7.1:** Manipulação dinâmica de interface e eventos.
- **[`stardew-valley-data`](https://github.com/chiefpansancolt/stardew-valley-data):** Catálogo de itens e estrutura de dados de Stardew Valley.
- **Canvas Confetti:** Efeito comemorativo ao carregar o save.
- **Execução 100% Client-Side:** Todo o processamento do save é feito localmente no navegador, garantindo privacidade e velocidade instantânea.
