# Design System INDAC: tokens e componentes

Fontes: `Design System INDAC.dc.html` (v1.0, 2026), a Proposta de IDV e a LP de referência `quiz-perfil-artisticov1`.

## Cores

```css
:root {
  --ink:          #141414;   /* Preto de palco: fundo padrão */
  --ink-suave:    #1c1c1c;   /* cards, inputs */
  --ink-elevated: #242424;
  --acento:       #d9342b;   /* Vermelho cortina: ação, grafismo, ênfase */
  --acento-fundo: #a8231d;   /* hover do vermelho */
  --papel:        #f5f1e8;   /* Creme refletor: texto sobre preto, fundo de respiro */
  --papel-sombra: #e8e2d4;
  --filete:       rgba(245,241,232,.14);
  --filete-suave: rgba(245,241,232,.08);
  --filete-forte: rgba(245,241,232,.28);
  --texto-2:      rgba(245,241,232,.70);
  --texto-muted:  rgba(245,241,232,.45); /* só para texto ≥ 14px e secundário */
  --font-display: 'Anton', system-ui, sans-serif;
  --font-serif:   'Merriweather', Georgia, serif;
  --font-body:    'Montserrat', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
  --max-w: 1600px;
}
```

- **Proporção**: 70% preto, 22% creme, 8% vermelho. "Se o vermelho estiver em tudo, não marca nada."
- **WhatsApp `#25D366`**: só no ícone.
- **No creme**: o texto vai para `#141414` e o vermelho continua sendo só o acento.
- **Cores de apoio da IDV** (verde, amarelo, marrom, azul, cinza): só para projetos especiais. Não use em LP de captura.

## Tipografia

Uma única requisição:

```html
<link href="https://fonts.googleapis.com/css2?family=Anton&family=Merriweather:ital,wght@0,400;0,700;1,400&family=Montserrat:wght@400;500;600;700;800&display=swap" rel="stylesheet">
```

| Estilo | Família | Tamanho | Entrelinha |
|---|---|---|---|
| Display | Anton 400, caixa alta | 64–116px (mobile ≥ 36px) | 0.88 |
| Título 1 | Anton 400, caixa alta | 40–56px | 0.95 |
| Título 2 | Merriweather 700 | 26–34px | 1.35 |
| Corpo | Montserrat 400 | **15–17px** | 1.65 |
| Rótulo | Montserrat 800, caixa alta | 10–12px, `letter-spacing .18em` | 1.2 |

- "Anton grita, Merriweather narra, Montserrat organiza."
- A IDV também aceita Chunk Five e Horizon como fontes de destaque, mas nas LPs use só as três acima.

## Grafismos

Duas famílias:
- **Geométrica** (chapado vermelho): pílula dupla, cantoneira, listra degradê, ampulheta.
- **Orgânica** (traço): raios e arcos aninhados em três espessuras (1 / 2 / 4).

**Pode**
- Usar em escala grande, sangrando pela borda.
- Usar um por bloco, como âncora da composição.
- Vermelho sobre preto, ou preto sobre creme.
- Girar, espelhar e recortar em máscara de foto.

**Não pode**
- Ladrilhar como textura.
- Aplicar gradiente, sombra ou contorno.
- Espremer ou inclinar em ângulo aleatório.
- Colocar texto por cima da área cheia.

Raios completos (hero):

```html
<svg viewBox="0 0 200 200" fill="none" aria-hidden="true"><g stroke="#d9342b" stroke-width="1.1"><line x1="100" y1="100" x2="100" y2="6"/><line x1="100" y1="100" x2="124" y2="9"/><line x1="100" y1="100" x2="147" y2="20"/><line x1="100" y1="100" x2="166" y2="39"/><line x1="100" y1="100" x2="180" y2="63"/><line x1="100" y1="100" x2="191" y2="88"/><line x1="100" y1="100" x2="194" y2="112"/><line x1="100" y1="100" x2="186" y2="139"/><line x1="100" y1="100" x2="168" y2="162"/><line x1="100" y1="100" x2="143" y2="182"/><line x1="100" y1="100" x2="118" y2="192"/><line x1="100" y1="100" x2="100" y2="194"/><line x1="100" y1="100" x2="76" y2="191"/><line x1="100" y1="100" x2="53" y2="180"/><line x1="100" y1="100" x2="34" y2="161"/><line x1="100" y1="100" x2="20" y2="137"/><line x1="100" y1="100" x2="9" y2="112"/><line x1="100" y1="100" x2="6" y2="88"/><line x1="100" y1="100" x2="14" y2="61"/><line x1="100" y1="100" x2="32" y2="38"/><line x1="100" y1="100" x2="57" y2="18"/><line x1="100" y1="100" x2="82" y2="8"/></g></svg>
```

Arcos aninhados (bloco de quiz ou CTA):

```html
<svg viewBox="0 0 200 200" fill="none" stroke="#d9342b" aria-hidden="true"><path d="M4 200 V96 A96 78 0 0 1 196 96 V200" stroke-width="1"/><path d="M36 200 V100 A64 54 0 0 1 164 100 V200" stroke-width="2"/><path d="M68 200 V104 A32 30 0 0 1 132 104 V200" stroke-width="4"/></svg>
```

## Componentes

- **Botão sólido**:
  - `background:#d9342b; color:#f5f1e8; padding:16px 30px; border-radius:999px;`
  - `font:800 12px Montserrat; letter-spacing:.14em; text-transform:uppercase;`
  - hover: `background:#a8231d; transform:translateY(-2px)`, **sem sombra**.
- **Botão contorno**:
  - `border:1px solid rgba(245,241,232,.35); background:transparent;`
  - hover: `border-color:#f5f1e8; background:rgba(245,241,232,.07)`.
- **Link de texto**: vermelho, com `border-bottom:2px solid #d9342b`. No hover, fica creme.
- **Selos**:
  - pílula vermelha cheia ("Inscrições abertas");
  - pílula de contorno com ponto vermelho de 5px ("2 minutos");
  - etiqueta creme reta ("Vagas limitadas");
  - filete lateral vermelho de 3px ("Curso livre");
  - texto **curto**, que não quebra no mobile.
- **Cartão**:
  - `background:#1c1c1c; border:1px solid var(--filete)` + barra superior de 6px em `#d9342b`;
  - rótulo vermelho de 10px, título em Anton 30px, corpo de 14–15px com 65% de opacidade e link de texto;
  - hover (só se clicável): borda vermelha + `translateY(-3px)`.
- **Formulário**:
  - rótulo Montserrat 800 de 10px, caixa alta, 60% de opacidade;
  - input `background:#1c1c1c; border:1px solid rgba(245,241,232,.2); padding:15px 16px; font-size:15px`;
  - foco com borda `#d9342b`;
  - raio 0.
- **Depoimento**: `border-left:3px solid #d9342b`, Merriweather itálico 20px, rodapé em rótulo.
- **Seção**: eyebrow com número em Anton vermelho de 14px + rótulo Montserrat 800 de 13px e `.22em`, depois o título em Anton.
  Use o rótulo como `<p>`/`<span>` e deixe **uma** `<h2>` por seção.
