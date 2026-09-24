# Manual Oficial de Publicação: LPs Ebook & Obrigado INDAC
### "O Guia (Não Tão) Secreto Para Se Tornar Ator" · RD Station Marketing

Este manual orienta a publicação, parametrização do formulário, hospedagem de mídias e automação de marketing para a nova Landing Page de captura e a respectiva Landing Page de obrigado do **INDAC Escola de Atores** no **RD Station Marketing**.

Arquivos do ecossistema:
- LP de captura para o RD: [`rd_station_ebook_lp.html`](./rd_station_ebook_lp.html)
- LP de captura para teste local: [`index.html`](./index.html)
- LP de obrigado para o RD: [`rd_station_obrigado_lp.html`](./rd_station_obrigado_lp.html)
- LP de obrigado para teste local: [`obrigado.html`](./obrigado.html)

---

## 1. Visão Geral da Arquitetura

O processo de captura e entrega do ebook segue a metodologia oficial do INDAC:
- **LP de Captura**: Foco total na conversão. No mobile (telas ≤ 767px), o formulário é exibido logo no início da página (acima de 812px de altura).
- **Pós-conversão**: O formulário do RD Station Marketing redireciona o lead para uma **LP de obrigado separada**, onde mora o botão de download direto e o convite principal para o Quiz de Perfil Artístico. Não são utilizados scripts de interceptação de rede nem adivinhações via temporizadores.
- **Identidade Visual**: 45 anos de história, 70% preto de palco (`#141414`), 22% creme refletor (`#F5F1E8`) e vermelho cortina (`#D9342B`) restrito a ≤ 10% da tela. Sem sombras decorativas em cards ou botões.

---

## 2. Passo a Passo Parte A: Ações no Painel do RD Station

### A1. Ajuste do Formulário (Item 01 da Auditoria)
No formulário de identificador `mt-lp-ebook-guia-secreto-95bee7fc70bce7a08668`:
1. **Texto do Botão de Envio**:
   - Alterar o texto atual ("AGENDAR VISITA GRATUITA") para **"Quero meu guia gratuito"** (ou "Receba o guia"), alinhando o botão à oferta do ebook.
2. **Campos do Formulário**:
   - Manter os campos essenciais: Nome Completo, E-mail e Telefone/WhatsApp.
   - Avaliar o campo select *"Como você gostaria que o teatro entrasse na sua vida?"*: manter se a equipe comercial precisar da qualificação, ou remover para reduzir a fricção na conversão.
3. **Consentimento LGPD**:
   - Ativar a caixa de aceite dos termos de privacidade e LGPD diretamente no construtor de formulários do RD.
4. **Configuração de Pós-Conversão (Redirecionamento)**:
   - Na aba de ações do formulário, selecionar a opção de **Redirecionamento para URL**.
   - Inserir a URL pública da LP de obrigado criada no passo A3 (ex.: `https://lp.indacescoladeatores.com.br/guia-secreto-obrigado`).

### A2. Upload de Arquivos no Gerenciador de Mídias do RD
No painel do RD Station Marketing, acesse **Conteúdo > Gerenciador de Arquivos**:
1. **Ebook em PDF**:
   - Faça o upload do arquivo `Ebook_Guia_Secreto_Ator_Indac_Master.pdf`.
   - Copie a URL pública absoluta gerada (exemplo: `https://d335luupugsy2.cloudfront.net/medias/indac/Ebook_Guia_Secreto_Ator_Indac_Master.pdf`).
2. **Mockup do Ebook**:
   - Faça o upload do mockup otimizado em WebP ou JPEG (arquivo de imagem do projeto).
   - Copie a URL pública absoluta gerada.
3. **Fotografia Real de Palco**:
   - Faça o upload de uma foto real de espetáculo do INDAC (crédito: Allan Bravos).
   - Copie a URL pública absoluta gerada.

### A3. Criação e Publicação das Duas Landing Pages
Para cada uma das páginas (Captura e Obrigado):
1. Acesse **Converter > Landing Pages** e clique em **Criar Landing Page**.
2. Selecione a aba **Modelos do Sistema** e escolha o **Modelo em Branco**.
3. Exclua todos os elementos pré-existentes até restar apenas uma única seção.
4. Configure a seção com:
   - **Largura**: Fluida (100%).
   - **Padding / Margem**: Todos zerados (0).
   - **Cor de Fundo**: `#141414` ou transparente.
5. Arraste um componente **HTML (`</>`)** para dentro da seção.
6. Copie e cole o código correspondente:
   - Para a captura: cole o conteúdo de [`rd_station_ebook_lp.html`](./rd_station_ebook_lp.html).
   - Para o obrigado: cole o conteúdo de [`rd_station_obrigado_lp.html`](./rd_station_obrigado_lp.html).
7. Defina os títulos de página, slugs amigáveis e publique ambas.

### A4. Automação de E-mail de Entrega
Acesse **Relacionar > Automação de Marketing**:
1. Crie um fluxo de automação com o gatilho de entrada:
   - *Converteu no formulário: `mt-lp-ebook-guia-secreto-95bee7fc70bce7a08668`*.
2. Adicione o passo de envio de e-mail imediato:
   - **Assunto**: `Aqui está o seu Guia Para Se Tornar Ator 🎭`
   - **Conteúdo**: Mensagem de boas-vindas com o link absoluto para baixar o PDF e o convite para realizar o Quiz de Perfil Artístico.

---

## 3. Passo a Passo Parte B: Substituição de Placeholders no Código

Antes da publicação definitiva no componente HTML do RD, localize e substitua os placeholders marcados com comentários nos códigos-fonte:

### 1. Na LP de Captura (`rd_station_ebook_lp.html` e `index.html`):
- `<!-- TROCAR: URL do mockup em WebP no Gerenciador de Arquivos do RD -->`
  - Substituir a URL provisória da tag `<img>` do hero pela URL definitiva hospedada no CDN do RD.
- `<!-- TROCAR: URL da foto no RD -->`
  - Substituir o endereço da imagem na Seção 02 pela foto real de espetáculo do INDAC (crédito: Allan Bravos).

### 2. Na LP de Obrigado (`rd_station_obrigado_lp.html` e `obrigado.html`):
- `<!-- TROCAR: URL absoluta do PDF no Gerenciador de Arquivos do RD -->`
  - Substituir o valor do atributo `href` no botão de download pela URL pública absoluta gerada no Gerenciador de Arquivos do RD Station.
- `<!-- TROCAR: URL do mockup em WebP no Gerenciador de Arquivos do RD -->`
  - Inserir a URL definitiva do mockup no hero da página de agradecimento.

---

## 4. Padrão Canônico de Header e Rodapé

O header e o rodapé aplicados em todas as LPs são os modelos canônicos da escola, documentados e mantidos em:
👉 [`.agents/skills/indac-lp-rdstation/references/header-footer.html`](./.agents/skills/indac-lp-rdstation/references/header-footer.html)

Eles incluem:
- Imagem oficial da marca (`log.png`) com 36px no topo e 44px na base.
- Botão oficial de atendimento para WhatsApp (`https://wa.link/izisk6`) com glifo oficial em verde `#25D366`.
- Telefone oficial `(11) 94514-0140` e e-mail `secretaria.indac@gmail.com`.
- Links para as 5 redes institucionais (Instagram, TikTok, Facebook, LinkedIn, YouTube).
- Créditos fotográficos e de direção, além da assinatura do desenvolvedor.

---

## 5. Checklist de QA Pré-Publicação

Checklist copiado da especificação da skill em [`.agents/skills/indac-lp-rdstation/references/checklist.md`](./.agents/skills/indac-lp-rdstation/references/checklist.md):

### Marca
- [ ] A logo é a imagem `log.png` oficial no header (36px) e no rodapé (44px). Não é texto.
- [ ] Header e rodapé são idênticos a `header-footer.html`: WhatsApp (11) 94514-0140, e-mail, 5 redes, créditos, assinatura.
- [ ] Nenhum texto interno aparece na página.
- [ ] O tempo de história é "45 anos" em todas as ocorrências.

### Cor e forma
- [ ] Um único botão sólido vermelho por bloco. No mobile, nunca dois na mesma tela (a barra fixa some no bloco do quiz).
- [ ] As tags e rótulos dos cards não são todos vermelhos. O vermelho fica ≤10% da tela.
- [ ] Sem sombras decorativas em cards ou botões.
- [ ] Raios só `0` ou `999px`.
- [ ] Grafismo grande e sangrando pela borda, um por bloco, com opacidade ≥ 0,4.

### Tipografia e ícones
- [ ] O corpo tem ≥ 15px em todos os blocos, e nenhum texto de leitura tem < 14px.
- [ ] Anton só em caixa alta, Merriweather no editorial e Montserrat na interface.
- [ ] Nenhum GIF, emoji ou caractere fazendo papel de ícone. Os ícones são SVG.

### Conversão
- [ ] Em 375×812, o formulário começa acima de 812px.
- [ ] O texto real do botão do formulário renderizado combina com a oferta da LP.
- [ ] O formulário tem consentimento LGPD.
- [ ] Todo link de arquivo é absoluto (não termina em arquivo relativo).
- [ ] O pós-conversão redireciona para a LP de obrigado. Não há script de detecção de conversão.
- [ ] A LP de obrigado tem: download, aviso de e-mail, convite ao quiz e caminhos.

### Texto e fatos
- [ ] Cada afirmação sobre quiz, imersão, visita e conversa foi conferida na página real.
- [ ] O texto esclarece que a formação habilita o aluno a solicitar o registro profissional.
- [ ] Fala direta: sem adjetivos inflados ou jargões de marketing.
- [ ] Nenhum selo ou pílula quebra de linha a ponto de ficar por cima de outro elemento no mobile.

### Técnico
- [ ] Imagens otimizadas com `width`/`height` e `loading="lazy"` fora do hero.
- [ ] Hierarquia de títulos: uma `<h1>`, uma `<h2>` por seção, sem pular nível. O conteúdo fica em `<main>`.
- [ ] Tem `@media (prefers-reduced-motion: reduce)`. Hover só em elementos clicáveis.
- [ ] A barra fixa do mobile não cobre o rodapé (`padding-bottom` + `env(safe-area-inset-bottom)`).
- [ ] O corpo de `index.html` e de `rd_station_ebook_lp.html` é idêntico.
- [ ] Não há rolagem horizontal em 375px.
