# Prompt de correção: LP Ebook "Guia (Não Tão) Secreto" (para colar no Antigravity)

> Abra a pasta `LP Ebook - Guia Secreto` no Antigravity e cole tudo o que está abaixo da linha.
> A numeração (02–28) é a mesma da auditoria visual. O item 01 é tarefa manual no painel do RD e está no fim.

---

Você vai corrigir a landing page do ebook "O Guia (Não Tão) Secreto Para Se Tornar Ator" do INDAC Escola de Atores,
que será publicada dentro do RD Station Marketing.

**Antes de tudo**, carregue e siga a skill do workspace `.agents/skills/indac-lp-rdstation/`: leia o `SKILL.md` e os
quatro arquivos em `references/`. As regras dela têm prioridade sobre qualquer decisão estética sua. O header e o rodapé
devem ser copiados de `references/header-footer.html`, não recriados.

## Arquivos
- Editar: `rd_station_ebook_lp.html` e, depois, fazer `index.html` virar cópia idêntica dele.
- Criar: `rd_station_obrigado_lp.html` (LP de obrigado) e `obrigado.html` (cópia para teste local).
- Reescrever: `RD_STATION_GUIA.md` e `README.md`.
- Não alterar: o PDF, o mockup, os PDFs de marca e `Design System INDAC.dc.html`.

## Decisões já tomadas (não reabrir)
- O pós-conversão vai para uma **LP de obrigado separada**, com o formulário do RD redirecionando para ela.
- O tempo de história é **45 anos** em todo lugar.
- O mockup `Book_and_smartphone_displaying_d…_2K_20260923191228.jpeg` continua sendo a imagem do hero.

## Correções na LP de captura (`rd_station_ebook_lp.html`)

### Conversão
- **02**: Remover o bloco `#bloco-pos-conversao` inteiro, o botão de download e a variável `PDF_DOWNLOAD_HREF`. O download passa a morar só na LP de obrigado.
- **03**: Apagar todo o script de detecção de conversão (as estratégias A a E: interceptação de XHR e fetch, `MutationObserver`, listener de submit com timeout de 3,2 s, `postMessage` e custom events, `sessionStorage`). Manter só o `createForm()` e a lógica que esconde o skeleton quando o formulário renderiza.
- **06**: No mobile (≤ 767px), reordenar o hero para: selo → título → **uma** linha de apoio → **card do formulário** → mockup. O parágrafo longo ("Esqueça fórmulas mágicas…") sai do hero e vira o lead da seção 01. Critério de aceite: em 375×812, o topo do card do formulário precisa ficar acima de 812px.
- **07**: A pílula do quiz passa a dizer "Teste gratuito · 8 perguntas · 3 min", com `flex-wrap: wrap`, `line-height` adequado e texto que não quebra por cima do título.

### Marca
- **04**: Substituir a logo em texto (pílula + "INDAC" em Anton + "Escola de Atores") pela imagem oficial `log.png`, no header e no rodapé, exatamente como em `references/header-footer.html`.
- **05**: Substituir o rodapé inteiro pelo rodapé canônico da skill. Isso remove:
  - o WhatsApp (11) 99616-0533;
  - o "Instituto de Arte e Ciência";
  - o texto "Identidade Visual Oficial · Palco, Vermelho e Creme".

  E acrescenta o e-mail, as 5 redes, os créditos e a assinatura.
- **15**: Substituir o header pelo canônico (glifo oficial do WhatsApp em `#25D366`, texto "Falar no WhatsApp", link `https://wa.link/izisk6`).

### Identidade visual
- **08**: Vermelho em ≤ 10% da página e um destaque por bloco:
  - as tags dos cards (`.card-top-tag`, `.pathway-badge`) passam a creme 60% com rótulo em caixa alta;
  - o hover dos cards de conteúdo sai (eles não são links);
  - a barra fixa do mobile some quando a seção `#secao-quiz` está visível.
- **09**: Remover todos os `box-shadow` de botões, cards, card de captura e imagem. O hover dos botões fica só com `background:#a8231d` + `translateY(-2px)`.
- **10**: Corpo com 15–17px:
  - `.card-text`, `.pathway-desc`, `.hero-desc`, `.footer-*` e `.capture-subtitle` ficam com ≥ 15px;
  - o texto de LGPD do formulário fica com ≥ 13px e o `line-height` é 1.6.
- **11**: Os raios do hero passam a ter as 22 linhas completas (SVG em `references/design-tokens.md`), com opacidade ~0,5, maiores e sangrando pela borda direita.
- **12**: Na seção 02 (respiro creme) **ou** na seção de caminhos, usar **uma** foto real de palco do INDAC. Use um placeholder claramente marcado (`<!-- TROCAR: URL da foto no RD -->`) com `alt` descritivo e o crédito "Foto: Allan Bravos". Não use banco de imagens.
- **13**: Trocar os caracteres "✓" dos benefícios do quiz por um ícone SVG de check com stroke.
- **14**:
  - remover o zoom no hover de `.hero-media-wrap img`;
  - remover o `translateY` de `.content-card:hover`;
  - adicionar `@media (prefers-reduced-motion: reduce)` zerando `animation` e `transition`.

### Texto (fala direta, segunda pessoa, sem adjetivo inflado)
- **16**: "mais de 50 anos", "50 anos", "Meio Século de Tradição" e "Há meio século" passam todos a usar **45 anos**.
- **17**: Seção do quiz e demais menções:
  - "8 perguntas · 3 minutos · diagnóstico enviado por e-mail";
  - remover "Resultado imediato" e "2 minutos".
- **18**: Cards de caminhos fiéis às páginas reais (confira abrindo cada URL antes de escrever):
  - **Imersão Cênica**: vivência gratuita de 2 dias, com oficinas de corpo, voz e interpretação e feedback profissional. Não é um "workshop intensivo".
  - **Agendar Conversa**: bate-papo online, individual e gratuito com um especialista em formação artística, com retorno em até 24h úteis pelo WhatsApp. Não é a "coordenação pedagógica".
  - **Visite o INDAC**: só o que a página promete (visita gratuita à escola na Rua Clélia, 658). Remova "casarão histórico, teatros e acervo".
- **19**: Trocar "emissão do DRT profissional" por um texto correto: a formação profissionalizante que habilita o aluno a solicitar o DRT.
- **20**: Remover o jargão:
  - "Conteúdo Estratégico" → "O que tem no guia";
  - "Acesso Exclusivo e Imediato" → "Ebook gratuito";
  - "PDF Master Digital" → "Ebook em PDF";
  - "no mais alto nível" → sai;
  - "Download Imediato" → "Receba no seu e-mail".
  - O título do card de captura passa a ser "Receba o guia".

### Técnico e acessibilidade
- **21**: Imagem do hero:
  - `src` com placeholder `<!-- TROCAR: URL do mockup em WebP no Gerenciador de Arquivos do RD -->` (mantenha a URL atual do S3 como valor provisório);
  - adicionar `width="1920" height="1080"` (confira a proporção real);
  - remover o `onerror`.
- **22**: Hierarquia de títulos:
  - o `.section-label` deixa de ser `<h2>` e vira `<p>`, deixando uma `<h2>` por seção;
  - o conteúdo fica envolto em `<main>`;
  - o rodapé segue o arquivo canônico.
- **23**: Barra fixa do mobile:
  - `padding-bottom` no wrapper igual à altura da barra + `env(safe-area-inset-bottom)`;
  - ela entra com `transform` e sai quando o hero está visível **ou** quando `#secao-quiz` está visível;
  - o link continua apontando para `#card-captura`.

## LP de obrigado (`rd_station_obrigado_lp.html`)
Mesmo `<style>` base, header e rodapé canônicos e tokens da skill. Estrutura, de cima para baixo:
1. **Hero curto**:
   - selo "Cadastro confirmado";
   - título Anton "Seu guia está pronto";
   - uma linha em Merriweather;
   - **um** botão sólido "Baixar o guia (PDF)" com `href="<!-- TROCAR: URL absoluta do PDF no Gerenciador de Arquivos do RD -->"` e `target="_blank" rel="noopener"`;
   - o mockup ao lado no desktop e abaixo no mobile.
2. **Aviso de e-mail**: filete lateral com ícone SVG de envelope. Texto: "Também enviamos o link para o seu e-mail, para você baixar quando e onde quiser. Não chegou? Olhe a caixa de promoções e o spam."
3. **Convite ao quiz** (bloco principal, com arcos aninhados sangrando):
   - "Qual é o seu perfil artístico?";
   - "8 perguntas · 3 minutos · diagnóstico enviado por e-mail";
   - botão sólido para `https://lp.indacescoladeatores.com.br/quiz-perfil-artisticov1`.
4. **Caminhos**: os 3 cards (Imersão, Visita, Conversa) com botão de contorno e os textos corrigidos no item 18.
5. **Rodapé** canônico. Sem barra fixa no mobile, porque o botão de download já está na primeira tela.

## Documentação
- **24–28**: Reescrever `RD_STATION_GUIA.md`:
  - links **relativos**;
  - remover a instrução sobre `PDF_DOWNLOAD_HREF` e toda a seção "Arquitetura do Script de Detecção";
  - passo a passo em duas partes: **(A) painel do RD** (item 01 abaixo, upload do PDF e do mockup no Gerenciador de Arquivos, publicação das duas LPs, redirecionamento do formulário para a LP de obrigado, automação de e-mail) e **(B) código** (onde trocar os placeholders `TROCAR:`);
  - seção "Padrão de header e rodapé" apontando para `.agents/skills/indac-lp-rdstation/references/header-footer.html`;
  - checklist copiado de `references/checklist.md`, **todo desmarcado**.
- Atualizar o `README.md`: estrutura de arquivos (incluir as duas LPs, a pasta `.agents/skills/` e este prompt) e remover as afirmações que não são mais verdadeiras.

## Verificação obrigatória antes de dizer que terminou
1. Abrir as duas LPs no navegador em 1440×900 e em 375×812 e tirar screenshots.
2. Passar o `references/checklist.md` inteiro nas duas LPs. Marcar só o que foi visto na tela.
3. Confirmar que `diff index.html rd_station_ebook_lp.html` não mostra diferença de corpo e que `obrigado.html` bate com `rd_station_obrigado_lp.html`.
4. Buscar nos quatro `.html` das LPs, no `RD_STATION_GUIA.md` e no `README.md` (não na pasta `.agents/`, que cita esses termos de propósito) e confirmar zero ocorrências de: `50 anos`, `99616`, `Instituto de Arte`, `Identidade Visual Oficial`, `PDF Master`, `✓`, `box-shadow`, `file:///`, `PDF_DOWNLOAD_HREF`, `emissão do DRT`.
5. Entregar um relatório curto com: o que mudou por item (02–28), os placeholders `TROCAR:` que restaram e as tarefas manuais do RD.

## Tarefa manual (não é código; listar no relatório para o usuário)
- **01**: No painel do RD, o formulário `mt-lp-ebook-guia-secreto-95bee7fc70bce7a08668` está com o botão
  "AGENDAR VISITA GRATUITA" e o select "Como você gostaria que o teatro entrasse na sua vida?". O usuário precisa:
  - trocar o botão para "Quero meu guia gratuito";
  - decidir se o select fica (qualificação) ou sai (menos atrito);
  - incluir o consentimento LGPD;
  - configurar o pós-conversão para redirecionar à LP de obrigado.
