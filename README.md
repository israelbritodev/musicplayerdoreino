# 🎵 Player de Música Dinâmico com JavaScript Puro

## 1. Resumo do Projeto

Este é um componente de player de música totalmente funcional, construído do zero (sem frameworks ou bibliotecas) utilizando **HTML5, CSS3 e JavaScript (ES6+)**.

O objetivo principal foi demonstrar competência nas principais tecnologias front-end, com foco em:
* Manipulação avançada do DOM.
* Integração com a API de Áudio do HTML5.
* Gerenciamento de estado da aplicação (como dados de músicas e estado de play/pause) usando JavaScript puro.

O diferencial deste player é sua **interface dinâmica**, que altera programaticamente o tema (gradiente de fundo e arte da capa) para corresponder à música que está sendo tocada.

---

## 2. Funcionalidades Implementadas

* **Controles de Mídia:** Funcionalidade completa de Play, Pause, Avançar e Voltar faixa.
* **Barra de Progresso:** Barra de progresso (`input[type=range]`) sincronizada em tempo real com o áudio.
* **Exibição de Tempo:** Contadores de tempo atual e duração total da faixa, formatados corretamente.
* **UI Temática e Dinâmica:** A interface (capa e fundo) é atualizada automaticamente a cada mudança de faixa, carregando dados de um objeto JavaScript.

---

## 3. Hard Skills e Conceitos Técnicos Demonstrados

Este projeto serviu como um campo de prática para as seguintes habilidades técnicas:

### JavaScript (ES6+)

* **Manipulação Avançada do DOM:**
    * Seleção de elementos (`getElementById`, `querySelector`).
    * Modificação de estilos CSS via JS (`element.style.background`).
    * Alteração de atributos (`element.src`, `progressBar.value`).
    * Atualização de conteúdo textual (`.textContent`).
    * Gerenciamento de classes CSS (`.classList.add`, `.classList.remove`) para alternar o estado visual (ex: botões play/pause).

* **HTML5 Audio API:**
    * Utilização do construtor `new Audio()` para criar e gerenciar o objeto de mídia.
    * Implementação dos métodos `.play()`, `.pause()` e `.load()`.
    * Leitura das propriedades `.currentTime` e `.duration` para sincronizar a UI.

* **Manipulação de Eventos (Event Handling):**
    * Uso de `addEventListener` para capturar interações do usuário (`click`).
    * Uso do evento `loadedmetadata` do objeto de áudio para obter a duração da faixa antes de tocar.

* **Lógica e Estrutura de Dados:**
    * Gerenciamento do estado da aplicação (a playlist) através de um **Array de Objetos**, onde cada objeto armazena os metadados da faixa (caminho, título, autor, e dados de tema).
    * Implementação de lógica de playlist (funções `nextSong` e `prevSong`) usando o **operador módulo (%)** para garantir um loop contínuo.
    * Uso de `setInterval` para criar um loop de atualização em tempo real (a cada segundo) para a barra de progresso.
    * Criação de uma função utilitária (`formatarTempo`) para formatar dados (segundos) em um formato legível (MM:SS), usando `Math.floor` e `padStart`.

### CSS3

* **Layout com Flexbox:** O layout principal do card e o alinhamento dos controles e textos foram todos estruturados usando Flexbox.
* **Estilização de Componentes:** Demonstração de estilização de elementos do zero, incluindo a personalização da aparência do `input[type=range]`.
* **Design Responsivo (Básico):** Uso de unidades relativas (`rem`, `vh`) para garantir que o player se adapte a diferentes tamanhos de viewport.
* **Importação de Fontes:** Uso de `@import` (Google Fonts) para uma tipografia customizada.

### HTML5

* **Estrutura Semântica:** O HTML foi estruturado de forma limpa e semântica, facilitando a seleção via JavaScript e a acessibilidade.
* **Atributos de Mídia:** Uso de `<img>` e elementos de áudio controlados via script.

---

## 4. Como Executar

O projeto é "plug-and-play". Não requer build ou dependências.

1.  Clone este repositório:
    ```bash
    git clone https://github.com/israelbritodev/musicplayerdoreino.git
    ```
2.  Navegue até a pasta do projeto.
3.  Abra o arquivo `index.html` em qualquer navegador moderno.
