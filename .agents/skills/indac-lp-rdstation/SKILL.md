---
name: indac-lp-rdstation
description: >-
  Constrói, corrige ou revisa landing pages do INDAC Escola de Atores para publicar no
  RD Station Marketing (captura de ebook, quiz, visita, imersão, conversa, LP de obrigado),
  aplicando o Design System e a identidade visual INDAC. Use esta skill sempre que o usuário
  pedir uma LP, página de captura, página de obrigado, seção, header, rodapé ou ajuste visual
  para o INDAC, mencionar RD Station, formulário RDStationForms, ebook, quiz de perfil artístico,
  ou pedir para "manter o padrão/identidade do INDAC".
---

# LPs do INDAC no RD Station

O INDAC já tem um sistema visual fechado. O seu trabalho é **aplicar** esse sistema, não reinterpretá-lo.
A LP de referência viva é `https://lp.indacescoladeatores.com.br/quiz-perfil-artisticov1`: quando houver dúvida
sobre header, rodapé, espaçamento ou tom, ela manda.

## Fluxo de trabalho

1. **Ler antes de escrever**:
   - [references/design-tokens.md](references/design-tokens.md): cores, tipografia, grafismos e componentes;
   - [references/header-footer.html](references/header-footer.html): header e rodapé canônicos. Copie, não recrie;
   - [references/rd-station.md](references/rd-station.md): como o HTML entra no RD, o formulário, a LP de obrigado e os arquivos.
2. **Confirmar os fatos da oferta** na página real antes de escrever o texto (duração, gratuidade, formato,
   número de perguntas). Nunca invente dado, prazo, endereço, número ou estrutura física.
3. **Montar a página** seguindo as regras abaixo.
4. **Rodar o checklist** [references/checklist.md](references/checklist.md): renderizar em 1440px e em 375×812,
   e só então entregar. Entregue também um relatório curto do que foi validado e do que depende de ação no painel do RD.

## Regras que não mudam

**Marca**
- Logo = imagem oficial `https://indacescoladeatores.com.br/wp-content/uploads/2025/10/log.png`
  (36px de altura no header, 44px no rodapé). **Nunca** escreva "INDAC" em Anton com pílula vermelha:
  isso é o cabeçalho do *documento* do Design System, não a logo.
- Header e rodapé: exatamente os de `references/header-footer.html` (WhatsApp (11) 94514-0140 / `wa.link/izisk6`,
  `secretaria.indac@gmail.com`, 5 redes, créditos de foto e direção, assinatura).
- Tempo de história: **45 anos**. Não use "50 anos", "mais de 50" nem "meio século".
- A escola **não emite** DRT. Ela oferece a formação profissionalizante que habilita o aluno a solicitar o registro.

**Cor**
- Preto `#141414` em ~70% da página, creme `#F5F1E8` em ~22%, vermelho `#D9342B` em **≤10%**.
- **Um** destaque vermelho e **um** botão sólido por bloco. Tags, rótulos e hovers secundários ficam em creme ou filete.
- Seção creme de respiro: no máximo **uma** por página. Faixa vermelha cheia: no máximo **uma** por página, curta, só para CTA.

**Forma**
- Raios: `0` ou `999px`. Nada entre esses dois valores.
- **Sem sombras** (`box-shadow`) em cards e botões, e sem brilho vermelho. Profundidade vem de filete (`rgba(245,241,232,.14)`) e de fundo `#1c1c1c`.
- Botão com altura mínima de 48px, Montserrat 800, caixa alta, `letter-spacing .14em`.

**Tipografia**
- Anton para manchetes (caixa alta, entrelinha ~0.9). Merriweather para subtítulo, citação e respiro. Montserrat para corpo e interface.
- Corpo com **15–17px**. Rótulos com 10–12px, só em caixa alta com tracking. Nunca use corpo menor que 14px, nem em LGPD e legenda.

**Ícones e mídia**
- Ícones em SVG inline com stroke. **Sem GIF, sem emoji e sem caracteres** como "✓", "→" ou "★" fazendo papel de ícone.
- WhatsApp: use o glifo oficial preenchido em `#25D366`. O verde aparece **só** no ícone.
- Fotografia real de palco do INDAC (créditos a Allan Bravos) é parte da identidade. Prefira uma foto real a uma ilustração.
- Imagens: WebP ou JPEG otimizado (até ~250 KB), com `width`/`height`, `loading="lazy"` fora do hero e hospedadas no RD.

**Grafismos**
- Raios, arcos aninhados e ondas entram **grandes, sangrando pela borda, um por bloco**, com opacidade de 0,4 a 0,9.
  Nunca pequenos e apagados, nunca repetidos como textura de fundo, nunca com texto por cima da área cheia.

**Movimento**
- Hover só em elementos clicáveis. Nada de zoom em imagem estática, nem card que sobe sem ser link.
- Sempre inclua `@media (prefers-reduced-motion: reduce)` desligando animações e transições.

**Texto (fala direta)**
- Segunda pessoa, verbo no presente, títulos curtos. Sem adjetivo inflado ("no mais alto nível", "exclusivo"),
  sem jargão de marketing ("conteúdo estratégico", "alta conversão", "PDF master"), sem promessa de fama.
- Nomes internos de arquivo, de sistema ou de identidade visual nunca aparecem na página.

**Conversão**
- No mobile, o formulário precisa aparecer na **primeira tela** (375×812): título → uma linha de apoio → formulário → mídia.
- Pós-conversão = **LP de obrigado separada**, com o formulário do RD redirecionando para ela.
  Não intercepte XHR/fetch nem escute `postMessage`, e não use timeouts para "adivinhar" a conversão.
- Link de arquivo sempre **absoluto** (Gerenciador de Arquivos do RD). Caminho relativo dá 404 dentro do RD.
- Na seção do quiz, a barra fixa do mobile some (dois botões sólidos na mesma tela é proibido).

## Antipadrões já cometidos (não repetir)

Estes erros saíram na LP do ebook "Guia (Não Tão) Secreto" (auditoria de 23/09/2026):

- logo feita em texto Anton;
- rodapé inventado, com número de WhatsApp errado e o texto "Identidade Visual Oficial · Palco, Vermelho e Creme" visível;
- formulário do RD reaproveitado de outra LP, com o botão "Agendar visita gratuita" numa LP de ebook;
- download apontando para `arquivo.pdf` relativo;
- script de detecção de conversão com falsos positivos;
- tags de todos os cards em vermelho, sombras vermelhas, corpo de 13px;
- pílula com texto longo que quebra e cobre o título no mobile;
- fatos errados: quiz de "2 minutos, resultado imediato" (o correto é 8 perguntas, 3 minutos, diagnóstico por e-mail), "50 anos", "emissão do DRT", "coordenação pedagógica" (a conversa é com um especialista);
- guia MD com links `file:///C:/...` e checklist marcado como feito sem verificação.
