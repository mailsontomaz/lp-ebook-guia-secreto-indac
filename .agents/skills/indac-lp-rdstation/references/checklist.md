# Checklist de QA: LP INDAC antes de entregar

Renderize a página no navegador em **1440×900** e em **375×812**. Marque só o que você viu.

## Marca
- [ ] A logo é a imagem `log.png` oficial no header (36px) e no rodapé (44px). Não é texto.
- [ ] Header e rodapé são idênticos a `header-footer.html`: WhatsApp (11) 94514-0140, e-mail, 5 redes, créditos, assinatura.
- [ ] Nenhum texto interno aparece ("Identidade Visual Oficial", "PDF Master", nome de arquivo, nome de token).
- [ ] O tempo de história é "45 anos" em todas as ocorrências.

## Cor e forma
- [ ] Um único botão sólido vermelho por bloco. No mobile, nunca dois na mesma tela (a barra fixa some no bloco do quiz).
- [ ] As tags e rótulos dos cards não são todos vermelhos. O vermelho fica ≤10% da tela.
- [ ] Nenhum `box-shadow` em card ou botão.
- [ ] Raios só `0` ou `999px`.
- [ ] Grafismo grande e sangrando pela borda, um por bloco, com opacidade ≥ 0,4.

## Tipografia e ícones
- [ ] O corpo tem ≥ 15px em todos os blocos, e nenhum texto de leitura tem < 14px.
- [ ] Anton só em caixa alta, Merriweather no editorial e Montserrat na interface.
- [ ] Nenhum GIF, emoji ou caractere ("✓", "→") fazendo papel de ícone. Os ícones são SVG.

## Conversão
- [ ] Em 375×812, o formulário começa **acima** de 812px.
- [ ] O texto real do botão do formulário renderizado combina com a oferta da LP.
- [ ] O formulário tem consentimento LGPD.
- [ ] Todo link de arquivo é absoluto (não termina em `arquivo.pdf` relativo).
- [ ] O pós-conversão redireciona para a LP de obrigado. Não há script de detecção de conversão.
- [ ] A LP de obrigado tem: download, aviso de e-mail, convite ao quiz e caminhos.

## Texto e fatos
- [ ] Cada afirmação sobre quiz, imersão, visita e conversa foi conferida na página real (ver `rd-station.md` §6).
- [ ] O texto não diz que a escola "emite" DRT.
- [ ] Fala direta: sem "exclusivo", "no mais alto nível", "conteúdo estratégico", "alta conversão".
- [ ] Nenhum selo ou pílula quebra de linha a ponto de ficar por cima de outro elemento no mobile.

## Técnico
- [ ] Imagens ≤ ~250 KB, com `width`/`height` e `loading="lazy"` fora do hero.
- [ ] Hierarquia de títulos: uma `<h1>`, uma `<h2>` por seção, sem pular nível. O conteúdo fica em `<main>`.
- [ ] Tem `@media (prefers-reduced-motion: reduce)`. Hover só em elementos clicáveis.
- [ ] A barra fixa do mobile não cobre o rodapé (`padding-bottom` + `env(safe-area-inset-bottom)`).
- [ ] O corpo de `index.html` e de `rd_station_*.html` é idêntico.
- [ ] Não há rolagem horizontal em 375px.
