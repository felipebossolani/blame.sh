# blame.sh — Prompts

## 1. Game (Claude Code — primeiro commit)

Crie um projeto web single-file (HTML/CSS/JS) chamado **blame.sh**.
O arquivo `excuses.json` já existe na raiz do projeto — leia ele para montar a matriz de desculpas.

### Estrutura do excuses.json
```
excuses.json
└── excuses
    └── [persona]        → ex: "PM/PO", "CTO/Manager", ...
        └── [situação]   → ex: "CI/CD falhou", ...
            └── tecnica  → string
            └── vaga     → string
            └── dramatica → string
```

Carregue o JSON via `fetch('./excuses.json')` na inicialização do app.

### Conceito
Gerador de desculpas técnicas para desenvolvedores. O usuário seleciona quem está perguntando e o que aconteceu, e recebe 3 desculpas prontas para usar — cada uma num tom diferente.

### Fluxo de interação
1. Tela inicial com o nome "blame.sh" e subtítulo
2. Step 1: selecionar **quem está perguntando** (botões, seleção única)
3. Step 2: selecionar **o que aconteceu** (botões, seleção única)
4. Botão "Generate Excuse" — exibe 3 desculpas lado a lado
5. Cada desculpa tem botão "Copy" que copia pro clipboard
6. Botão "Reset" para recomeçar

### Quem está perguntando (7 opções)
- PM/PO
- CTO/Manager
- CEO/Founder
- Cliente/Stakeholder
- Outro dev do time
- Dev Sênior Irritado
- Auditor/Compliance

### O que aconteceu (12 opções)
- Subiu em prod e quebrou outra coisa
- CI/CD falhou
- Bug antigo voltou
- Estimativa estourou
- Feature atrasou
- Ambiente caiu
- PR parado há dias
- Test coverage caiu
- Deploy na sexta às 17h
- Rollback falhou também
- Dados duplicados em prod
- Alguém deletou o banco

### Os 3 tons de desculpa
- **Técnica** — jargão pesado, convincente, intimida quem não é dev
- **Vaga** — corporativa, ninguém entende nada mas soa profissional
- **Dramática** — exagerada, quase uma tragédia grega

### Idioma
Bilíngue. PT-BR como default. Botão de toggle PT | EN no header. Todas as 252 desculpas devem existir nas duas línguas.

### Design — Terminal Moderno
- Fundo: `#0D1117` (GitHub dark)
- Texto primário: `#E6EDF3`
- Acento verde: `#3FB950` (GitHub green)
- Acento azul: `#58A6FF` (GitHub blue)
- Erro/drama: `#F85149` (GitHub red)
- Fonte display: `JetBrains Mono` ou `Fira Code` via Google Fonts
- Fonte corpo: mesma monospace, peso variado
- Botões de seleção: estilo "chip" com borda sutil, highlight ao selecionar
- Cards de desculpa: fundo `#161B22`, borda `#30363D`, padding generoso
- Header da desculpa mostra o tom com cor própria (verde/azul/vermelho)
- Animação de "digitando" quando as desculpas aparecem (typewriter effect)
- Prompt do terminal no topo: `$ blame --who="PM/PO" --incident="CI/CD falhou"`
- Layout responsivo, mobile-friendly
- Nenhum gradiente pastel, nenhuma rounded card genérica

---

## 2. Logo (Gemini Imagen)

Create a square logo for a developer tool called "blame.sh".

Concept: a 16-bit pixel art character — a nerdy but cocky developer doing a shrug.
One eyebrow raised. Shoulders up, palms out. The universal expression of
"not my fault, not my problem."

Character details:
- Male-presenting, glasses, hoodie
- 16-bit sprite style — more detailed than NES, less smooth than modern art
- Visible pixels, clean edges, no anti-aliasing
- Full body or half-body, centered in a square canvas

Color palette:
- Background: #0D1117 (dark, almost black)
- Skin tone: warm pixel-art standard
- Hoodie: dark gray or muted green — dev aesthetic
- Glasses: bright accent, #58A6FF or #3FB950
- Use maximum 8-10 colors total — pixel art constraint

Mood: ironic, unbothered, slightly smug.
This character has seen production go down before. He will see it again.

Square format. No text. No background elements. Just the character.

---

## 3. Assets & Meta Integration (Claude Code)

The project already has logo.png and favicon.png in the root.
Integrate both and finalize the production setup:

### Favicon & Icons
- Link favicon.png as browser tab icon
- Add apple-touch-icon for iOS

### Open Graph / Social Meta Tags
- og:title → "blame.sh"
- og:description → "Pick who's asking. Pick what broke. Get your excuse."
- og:image → logo.png
- og:type → website
- Twitter Card: summary_large_image

### Page title
- `<title>` → "blame.sh — Developer Excuse Generator"

### Logo on start screen
- Display logo.png no header ao lado do nome "blame.sh"
- Manter estética terminal — logo deve parecer parte do prompt, não decoração

### Share button
No card de cada desculpa, além do botão "Copy", adicionar botão "Share" que copia:
`I used blame.sh to explain why [o que aconteceu] to [quem perguntou]. It worked. blame.sh`

### Footer
`$ echo "built with caffeine and plausible deniability"` — monospace, baixa opacidade

### Bonus
- Adicionar `manifest.json` básico para PWA (nome, ícone, cor de tema `#0D1117`)
- Meta `theme-color` para colorir a barra do browser no mobile
