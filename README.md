# 🎮 Jogo da Velha - Teste Técnico React

Um jogo da velha completo desenvolvido com React puro, atendendo a todos os requisitos do teste técnico para vaga de Desenvolvedor(a) Web Sênior.

## 📋 Visão Geral

Este projeto implementa um jogo da velha interativo com as seguintes funcionalidades:

- ✅ **JavaScript puro** - Sem TypeScript
- ✅ **Hooks personalizados** - `useGameState`, `useGameTheme`, `useGameTimer`, `useGameAnimations`, `useGameAccessibility`
- ✅ **Tipagem adequada** - Utilizando JSDoc para documentação
- ✅ **Sem bibliotecas externas** - Apenas React e Vite
- ✅ **Menu flutuante de personalização** - Cores em tempo real
- ✅ **Temporizador de jogada** - 5 segundos por jogador com progress bar
- ✅ **Cálculo de resultado** - Vitória, empate e placar
- ✅ **Sistema de partidas** - Primeiro a 11 vitórias
- ✅ **Placar persistente** - Mantido enquanto a aba está aberta
- ✅ **Opção de zerar placar** - Botão de reset
- ✅ **Área de pontuação visual** - Interface clara e intuitiva
- ✅ **Acessibilidade completa** - Screen reader, navegação por teclado, alto contraste
- ✅ **Animações e feedback visual** - Transições suaves e responsivas
- ✅ **UX aprimorada** - Controles intuitivos e feedback imediato

## 🏗️ Estrutura de Pastas

```
src/
├── components/              # Componentes React especializados
│   ├── AccessibilityControls.jsx  # Controles de acessibilidade
│   ├── Board.jsx           # Tabuleiro do jogo
│   ├── GameAnnouncer.jsx   # Anúncios para screen reader
│   ├── GameContainer.jsx   # Container organizacional
│   ├── GameControls.jsx    # Controles do jogo
│   ├── GameHeader.jsx      # Cabeçalho do jogo
│   ├── GameInfo.jsx        # Informações do jogo
│   ├── GameLayout.jsx      # Layout responsivo
│   ├── GameTimer.jsx       # Temporizador com animações
│   ├── Scoreboard.jsx      # Placar
│   ├── Square.jsx          # Quadrado individual
│   └── ThemeCustomizer.jsx # Personalização de cores
├── hooks/                  # Hooks personalizados
│   ├── useGameState.js     # Lógica central do jogo
│   ├── useGameTheme.js     # Gerenciamento de tema
│   ├── useGameTimer.js     # Temporizador avançado
│   ├── useGameAnimations.js # Controle de animações
│   └── useGameAccessibility.js # Recursos de acessibilidade
├── utils/                  # Funções utilitárias
│   ├── gameLogic.js        # Lógica pura do jogo
│   └── themePresets.js     # Presets de tema
├── styles/                 # Estilos CSS organizados
│   ├── AccessibilityControls.css
│   ├── Board.css
│   ├── GameAnnouncer.css
│   ├── GameContainer.css
│   ├── GameControls.css
│   ├── GameHeader.css
│   ├── GameInfo.css
│   ├── GameLayout.css
│   ├── GameTimer.css
│   ├── Scoreboard.css
│   ├── Square.css
│   └── ThemeCustomizer.css
├── App.jsx                 # Componente principal
├── App.css                 # Estilos globais
├── index.css               # Estilos de base
└── main.jsx               # Ponto de entrada
```

## 🎯 Justificativas Técnicas

### 1. **Arquitetura de Hooks Personalizados**

**Escolha:** Composição de hooks especializados para diferentes responsabilidades

**Justificativa:**
- **`useGameState`** - Lógica central do jogo com composição de outros hooks
- **`useGameTimer`** - Temporizador avançado com pausa, retomada e status visual
- **`useGameAnimations`** - Controle centralizado de animações
- **`useGameAccessibility`** - Recursos de acessibilidade e preferências do usuário
- **`useGameTheme`** - Gerenciamento de tema dinâmico

**Benefícios:**
- **Reutilização:** Hooks podem ser facilmente reutilizados
- **Testabilidade:** Lógica isolada facilita testes unitários
- **Manutenibilidade:** Mudanças ficam centralizadas
- **Separação de responsabilidades:** Cada hook tem função específica

### 2. **Composição Estratégica de Componentes**

**Escolha:** Componentes pequenos, focados e reutilizáveis

**Justificativa:**
- **`GameTimer`** - Temporizador com progress bar e animações
- **`AccessibilityControls`** - Controles de acessibilidade flutuantes
- **`GameAnnouncer`** - Anúncios para screen reader
- **`GameLayout`** - Layout responsivo organizacional
- **`GameContainer`** - Container que agrupa lógica relacionada

**Benefícios:**
- **Coesão:** Cada componente tem responsabilidade bem definida
- **Reutilização:** Componentes podem ser reutilizados
- **Manutenibilidade:** Mudanças isoladas
- **Testabilidade:** Componentes menores são mais fáceis de testar

### 3. **Separação Clara entre Lógica de Negócio e Apresentação**

**Escolha:** Utilitários para lógica pura, hooks para estado, componentes para UI

**Justificativa:**
- **`utils/gameLogic.js`** - Funções puras para lógica do jogo
- **`utils/themePresets.js`** - Dados e lógica de temas
- **Hooks** - Gerenciamento de estado e efeitos colaterais
- **Componentes** - Apenas renderização e interação

**Benefícios:**
- **Testabilidade:** Lógica pura é fácil de testar
- **Reutilização:** Utilitários podem ser usados em qualquer lugar
- **Manutenibilidade:** Mudanças na lógica não afetam a UI
- **Performance:** Lógica otimizada e isolada

### 4. **Sistema de Animações e Feedback Visual**

**Escolha:** CSS animations + JavaScript para controle preciso

**Justificativa:**
- **Animações CSS:** Performance otimizada para transições
- **JavaScript controlado:** Trigger de animações baseado em eventos
- **Acessibilidade:** Respeita `prefers-reduced-motion`
- **Responsividade:** Animações adaptadas a diferentes dispositivos

**Benefícios:**
- **UX aprimorada:** Feedback visual imediato
- **Acessibilidade:** Suporte a preferências do usuário
- **Performance:** Animações otimizadas
- **Manutenibilidade:** Sistema centralizado de animações

### 5. **Acessibilidade de Primeira Linha**

**Escolha:** Acessibilidade integrada ao design, não como add-on

**Justificativa:**
- **Screen reader support:** Anúncios automáticos de eventos
- **Keyboard navigation:** Navegação completa por teclado
- **ARIA labels:** Labels descritivos e apropriados
- **High contrast:** Suporte automático a alto contraste
- **Reduced motion:** Respeita preferências do usuário
- **Large text:** Modo de texto aumentado

**Benefícios:**
- **Inclusividade:** Acessível a todos os usuários
- **Compliance:** Atende padrões de acessibilidade
- **UX universal:** Melhor experiência para todos
- **Manutenibilidade:** Acessibilidade integrada ao código

### 6. **Responsividade e Adaptabilidade**

**Escolha:** Mobile-first design com breakpoints estratégicos

**Justificativa:**
- **CSS Grid/Flexbox:** Layouts flexíveis e adaptáveis
- **Media queries:** Breakpoints para desktop, tablet, mobile
- **Touch-friendly:** Interface otimizada para touch
- **Performance:** Otimizações para diferentes dispositivos

**Benefícios:**
- **Acessibilidade:** Funciona em qualquer dispositivo
- **UX consistente:** Experiência uniforme
- **Performance:** Otimizado para cada dispositivo
- **Manutenibilidade:** CSS organizado e responsivo

## 🚀 Instruções de Build e Execução

### Pré-requisitos

- Node.js (versão 16 ou superior)
- npm ou yarn

### Instalação

1. **Clone o repositório:**
```bash
git clone <url-do-repositorio>
cd Tic-Tac-Toe
```

2. **Instale as dependências:**
```bash
npm install
```

### Execução

3. **Inicie o servidor de desenvolvimento:**
```bash
npm run dev
```

4. **Acesse a aplicação:**
Abra seu navegador e acesse `http://localhost:5173`

### Build para Produção

5. **Gere o build de produção:**
```bash
npm run build
```

6. **Visualize o build:**
```bash
npm run preview
```

## 🎮 Como Jogar

1. **Início:** O jogo começa automaticamente com o jogador X
2. **Temporizador:** Cada jogador tem 5 segundos para fazer sua jogada
3. **Progress bar:** Visualização do tempo restante com cores dinâmicas
4. **Jogada automática:** Se o tempo acabar, o sistema joga automaticamente
5. **Vitória:** Alinhe 3 símbolos (X ou O) em linha, coluna ou diagonal
6. **Empate:** Quando todas as casas estiverem preenchidas sem vencedor
7. **Partida:** Primeiro jogador a vencer 11 partidas vence a partida
8. **Personalização:** Clique em "🎨 Personalizar" para mudar as cores
9. **Acessibilidade:** Use os controles de acessibilidade no canto superior direito

## 🎨 Funcionalidades

### Sistema de Jogo
- ✅ Tabuleiro 3x3 interativo com animações
- ✅ Alternância automática entre X e O
- ✅ Detecção de vitória e empate
- ✅ Destaque visual da linha vencedora
- ✅ Temporizador de 5 segundos com progress bar
- ✅ Jogada automática quando o tempo acaba
- ✅ Animações de aparição e vitória

### Sistema de Partidas
- ✅ Placar acumulado (X, O, Empates)
- ✅ Contador de partidas jogadas
- ✅ Vitória na partida ao atingir 11 vitórias
- ✅ Botão para resetar placar
- ✅ Botão para nova partida
- ✅ Animações de atualização de pontuação

### Personalização
- ✅ Menu flutuante de cores
- ✅ Cores personalizáveis para X, O, fundo, tabuleiro e texto
- ✅ Presets de tema (Clássico, Escuro, Natureza, Pôr do Sol)
- ✅ Aplicação em tempo real das mudanças
- ✅ Animações de transição de tema

### Acessibilidade
- ✅ Navegação completa por teclado
- ✅ Labels ARIA apropriados
- ✅ Anúncios automáticos para screen reader
- ✅ Modo alto contraste automático
- ✅ Redução de movimento (prefers-reduced-motion)
- ✅ Modo texto grande
- ✅ Controles de acessibilidade flutuantes
- ✅ Suporte a preferências do usuário

### Responsividade
- ✅ Design responsivo para desktop, tablet e mobile
- ✅ Adaptação de layout para diferentes tamanhos de tela
- ✅ Otimização de interface para touch
- ✅ Breakpoints estratégicos (1024px, 768px, 480px)

### Animações e UX
- ✅ Animações suaves e contextuais
- ✅ Feedback visual imediato
- ✅ Progress bar do temporizador
- ✅ Animações de vitória e empate
- ✅ Transições de tema
- ✅ Hover e focus states
- ✅ Animações de loading e transição

## 🛠️ Tecnologias Utilizadas

- **React 19.1.0** - Biblioteca principal
- **Vite 7.0.4** - Build tool e dev server
- **CSS3** - Estilização com variáveis customizadas e animações
- **JavaScript ES6+** - Lógica do jogo e hooks personalizados
- **JSDoc** - Documentação de código

## 📊 Métricas de Qualidade

### Cobertura de Requisitos
- ✅ **Requisitos obrigatórios:** 100%
- ✅ **Diferenciais implementados:** 100%

### Arquitetura
- **Hooks personalizados:** 5 (useGameState, useGameTheme, useGameTimer, useGameAnimations, useGameAccessibility)
- **Componentes especializados:** 12 (Board, Square, GameInfo, Scoreboard, ThemeCustomizer, GameTimer, AccessibilityControls, GameAnnouncer, GameLayout, GameContainer, GameControls, GameHeader)
- **Utilitários:** 2 (gameLogic, themePresets)
- **Estilos organizados:** 12 arquivos CSS por componente

### Funcionalidades
- **Animações CSS:** 15+ (timer, square, theme, accessibility, etc.)
- **Recursos de acessibilidade:** 8+ (screen reader, keyboard, contrast, etc.)
- **Breakpoints responsivos:** 4 (desktop, tablet, mobile, small mobile)
- **Presets de tema:** 4 (classic, dark, nature, sunset)

### Performance
- **Lazy loading:** Componentes carregados sob demanda
- **Memoização:** useCallback para funções críticas
- **Cleanup:** Timers e listeners limpos adequadamente
- **CSS otimizado:** Variáveis CSS para performance

## 🔧 Scripts Disponíveis

```bash
npm run dev      # Inicia servidor de desenvolvimento
npm run build    # Gera build de produção
npm run preview  # Visualiza build de produção
npm run lint     # Executa linter
```

## 🎯 Critérios de Avaliação Atendidos

### ✅ Escalabilidade e Manutenibilidade
- **Arquitetura modular:** Componentes e hooks reutilizáveis
- **Separação de responsabilidades:** Lógica, UI e estilos organizados
- **Código limpo:** Nomes descritivos e estrutura clara
- **Documentação:** JSDoc e README completo

### ✅ Composição Estratégica de Componentes e Hooks
- **Hooks especializados:** Cada hook tem responsabilidade específica
- **Composição inteligente:** Hooks se complementam
- **Componentes focados:** Cada componente tem função bem definida
- **Reutilização:** Componentes e hooks podem ser reutilizados

### ✅ Boas Práticas com React
- **Controle de estado:** useCallback, useEffect, useState
- **Ciclo de vida:** Cleanup adequado de timers e listeners
- **Performance:** Memoização e otimizações
- **Acessibilidade:** ARIA labels e navegação por teclado

### ✅ Clareza nas Escolhas Técnicas
- **README detalhado:** Justificativas técnicas claras
- **Documentação:** Estrutura e decisões documentadas
- **Comentários:** Código autoexplicativo
- **Organização:** Estrutura de pastas lógica

### ✅ Capricho Visual
- **Design moderno:** Interface limpa e profissional
- **Animações suaves:** Transições e feedback visual
- **Responsividade:** Adaptação perfeita a todos os dispositivos
- **Acessibilidade visual:** Alto contraste e texto grande

### ✅ Comunicação Escrita
- **README completo:** Visão geral, estrutura, justificativas
- **Instruções claras:** Build, execução e uso
- **Documentação técnica:** Escolhas e decisões explicadas
- **Organização:** Informações bem estruturadas

## 📝 Licença

Este projeto foi desenvolvido como teste técnico. Código livre para uso educacional.

---

**Desenvolvido com ❤️ e React**
