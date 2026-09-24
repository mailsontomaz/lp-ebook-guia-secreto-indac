# Publicar LPs do INDAC no RD Station Marketing

## 1. Como o HTML entra no RD

- Crie a LP no RD em **Modelo em branco** e deixe **uma** seção, com largura fluida, padding 0 e fundo `#141414`.
- Arraste **um** bloco HTML (`</>`) para dentro dela.
- Cole só o **conteúdo** da página, sem `<!DOCTYPE>`, `<html>`, `<head>` ou `<body>` (o RD já gera esses):
  1. o `<link>` do Google Fonts;
  2. o `<style>`;
  3. a marcação;
  4. os `<script>`.
- Mantenha o arquivo-fonte em duas versões no repositório:
  - `index.html`: documento completo, para teste local;
  - `rd_station_*.html`: mesmo conteúdo, pronto para colar.
  - As duas devem ficar **idênticas** no corpo.
- Neutralize os wrappers do RD **uma vez**, no topo do `<style>`:

```css
#bricks-page-wrapper, .bricks-page-section, .bricks-page-section > div, .bricks-component,
.rd-section, .rd-row, .rd-column, .bricks--section, .bricks--row, .bricks--column > div {
  padding: 0 !important; margin: 0 !important; max-width: 100% !important;
  width: 100% !important; background-color: transparent !important; border: none !important;
}
```

## 2. Formulário (RDStationForms)

- Use o snippet que o RD gera **para esta LP**:

```html
<div role="main" id="<ID-DO-FORM>"></div>
<script src="https://d335luupugsy2.cloudfront.net/js/rdstation-forms/stable/rdstation-forms.min.js"></script>
<script>new RDStationForms('<ID-DO-FORM>', 'null').createForm();</script>
```

- **Os campos, o texto do botão e o pós-conversão vêm do painel do RD, não do HTML.** Antes de entregar, renderize a
  página e leia o texto real do botão. Se o formulário tiver sido duplicado de outra LP, o botão chega com o texto antigo
  (por exemplo, "Agendar visita gratuita" numa LP de ebook). Reporte isso como tarefa manual.
- O texto do botão deve dizer o que o lead recebe: "Quero meu guia gratuito", "Quero fazer o teste",
  "Agendar minha visita", e assim por diante.
- O formulário precisa ter consentimento LGPD.
- Os campos que o INDAC usa como padrão são nome, e-mail e telefone. Um select de qualificação só entra se o time comercial pedir.
- Estilize pelo ID do contêiner (`#<ID-DO-FORM> input`, `button`, `label`), usando `!important`, porque o RD injeta
  CSS próprio com IDs `#rd-form-*` e botão `#f4141d` (esse vermelho não é o da marca, sobrescreva para `#d9342b`).

## 3. Pós-conversão = LP de obrigado

- Crie uma **segunda LP** no RD (ex.: `/<slug>-obrigado`) com o mesmo header, rodapé e tokens.
- No formulário da LP de captura, configure o pós-conversão para **redirecionar** à LP de obrigado.
- A LP de obrigado contém:
  1. uma confirmação curta;
  2. o botão de download com a **URL absoluta** do arquivo;
  3. o aviso de que o lead também recebe o arquivo por e-mail, para baixar quando e onde quiser;
  4. o convite para o quiz (bloco principal);
  5. os caminhos secundários (imersão, visita, conversa).
- **Não** detecte conversão com JavaScript (interceptar XHR/fetch, `postMessage`, `MutationObserver`, timeout).
  Isso gera falsos positivos e esconde o formulário.
- A LP de obrigado também é o lugar certo para pixels e eventos de conversão (Meta, Google Ads, GA4).

## 4. Arquivos (PDF, imagens)

- Suba tudo em **Conteúdo › Gerenciador de Arquivos** do RD e use a URL pública absoluta
  (`https://d335luupugsy2.cloudfront.net/...`).
- Caminho relativo (`arquivo.pdf`) dá 404 dentro do RD.
- O atributo `download` é ignorado quando o arquivo está em outro domínio. Use `target="_blank"` e um texto claro no botão.
- Otimize as imagens antes de subir: WebP ou JPEG de até ~250 KB, sempre com `width` e `height`.

## 5. Entrega por e-mail (automação)

- **Relacionar › Automação**:
  - gatilho: "Converteu no formulário <ID-DO-FORM>";
  - ação: enviar e-mail.
- O e-mail leva o link absoluto do arquivo e o convite para o quiz.
- A promessa "você também recebe por e-mail" só pode aparecer na LP se essa automação existir.

## 6. Links fixos do ecossistema

| Página | URL | O que é (conferido nas páginas) |
|---|---|---|
| Quiz de Perfil Artístico | https://lp.indacescoladeatores.com.br/quiz-perfil-artisticov1 | Gratuito · 8 perguntas · 3 minutos · diagnóstico enviado por e-mail |
| Imersão Cênica | https://lp.indacescoladeatores.com.br/imersao-cenica | Vivência gratuita de 2 dias (19h–22h30), com oficinas e feedback profissional |
| Visite o INDAC | https://lp.indacescoladeatores.com.br/visiteoindac | Agendamento de visita gratuita à escola |
| Agendar Conversa | https://lp.indacescoladeatores.com.br/agendar-conversa-v1 | Bate-papo online, individual e gratuito com um especialista em formação artística; retorno em até 24h úteis pelo WhatsApp |

Antes de escrever o texto sobre qualquer uma delas, abra a página e confirme se esses dados continuam valendo.

## 7. Guia MD que acompanha cada LP

- Links **relativos** (`[arquivo](./arquivo.html)`), nunca `file:///C:/...`.
- Passos do painel do RD separados dos passos de código.
- Checklist com `[ ]`, marcado só depois de verificar de verdade.
