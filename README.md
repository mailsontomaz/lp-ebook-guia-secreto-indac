# Landing Page: Ebook "O Guia (Não Tão) Secreto Para Se Tornar Ator"
### INDAC Escola de Atores · RD Station Marketing

Landing Page de captura e Landing Page de agradecimento desenvolvidas para publicação no **RD Station Marketing**, em estrita conformidade com a identidade visual do **INDAC Escola de Atores**.

---

## 🎭 Sobre o Projeto

Este projeto tem como objetivo a captura qualificada de pessoas interessadas na formação teatral oferecida pelo **INDAC Escola de Atores**, disponibilizando gratuitamente o ebook:
> **"O Guia (Não Tão) Secreto Para Se Tornar Ator: Tudo o que não te contam, mas que muda tudo. Sua jornada autêntica do zero ao DRT."**

### Principais Características da Arquitetura:
- **Hero de Conversão Otimizado**: No mobile (telas ≤ 767px), o formulário é exibido na primeira dobra (acima de 812px de altura).
- **Pós-Conversão em LP de Obrigado Separada**: Após o envio dos dados, o formulário do RD Station Marketing redireciona o lead para uma página de agradecimento dedicada, onde o arquivo PDF é disponibilizado para download direto junto ao convite principal para o Quiz de Perfil Artístico.
- **Ecossistema Integrado**: Links diretos para as experiências institucionais do INDAC:
  - [Imersão Cênica](https://lp.indacescoladeatores.com.br/imersao-cenica)
  - [Visite o INDAC](https://lp.indacescoladeatores.com.br/visiteoindac)
  - [Agendar Conversa](https://lp.indacescoladeatores.com.br/agendar-conversa-v1)
  - [Quiz de Perfil Artístico](https://lp.indacescoladeatores.com.br/quiz-perfil-artisticov1)
- **Header e Rodapé Canônicos**: Logotipo oficial em imagem (`log.png`), WhatsApp oficial via wa.link, e-mail da secretaria, 5 redes sociais, créditos de fotografia (Allan Bravos) e direção (Cris Urbinatti).
- **100% Livre de GIFs**: Todos os ícones e grafismos são vetoriais (SVG inline), garantindo máxima nitidez e conformidade técnica.

---

## 🎨 Design System INDAC

- **Cores Oficiais**:
  - Preto de Palco (`#141414`): fundo principal (~70%)
  - Preto Suave (`#1C1C1C`): cartões e inputs
  - Vermelho Cortina (`#D9342B`): ação e ênfase (≤ 10%)
  - Vermelho Hover (`#A8231D`): hover dos botões
  - Creme Refletor (`#F5F1E8`): tipografia sobre preto e bloco editorial de respiro (~22%)
  - WhatsApp (`#25D366`): restrito ao glifo oficial
- **Tipografia**:
  - *Anton*: títulos principais e manchetes em caixa alta
  - *Merriweather*: citações, respiro editorial e subtítulos
  - *Montserrat*: corpo de texto (≥ 15px), interfaces e rótulos
- **Raios de Borda**: Estritamente `0` (cantos retos) ou `999px` (pílulas completas).

---

## 📁 Estrutura de Arquivos

```text
├── index.html                                  # LP de captura (cópia idêntica para teste local)
├── rd_station_ebook_lp.html                    # LP de captura para colar no componente HTML do RD
├── obrigado.html                               # LP de obrigado (cópia idêntica para teste local)
├── rd_station_obrigado_lp.html                 # LP de obrigado para colar no componente HTML do RD
├── RD_STATION_GUIA.md                          # Manual oficial de configuração e publicação no RD
├── PROMPT_CORRECAO_ANTIGRAVITY.md              # Especificação das correções e auditoria
├── .agents/skills/indac-lp-rdstation/          # Skill de design e regras canônicas da escola
├── Ebook_Guia_Secreto_Ator_Indac_Master.pdf    # Arquivo PDF oficial do Ebook
├── Book_and_smartphone_displaying_d...jpeg     # Mockup oficial em alta resolução
├── Design System INDAC.dc.html                 # Especificações do Design System
├── identidade visual INDAC.pdf                 # Diretrizes de marca
├── Proposta IDV - Indac.pdf                    # Proposta de Identidade Visual
└── _MANUAL DE MARCA ( INDAC ) 2025.pdf         # Manual de Marca consolidado
```

---

## 🚀 Como Publicar no RD Station Marketing

Consulte o passo a passo completo no manual [`RD_STATION_GUIA.md`](./RD_STATION_GUIA.md):
1. No painel do RD, ajuste os textos e LGPD do formulário `mt-lp-ebook-guia-secreto-95bee7fc70bce7a08668`.
2. Configure o pós-conversão do formulário para redirecionar à LP de obrigado.
3. Suba o arquivo PDF e o mockup no Gerenciador de Arquivos do RD.
4. Crie as duas Landing Pages em modelo em branco e cole os respectivos códigos HTML.
5. Configure a automação de e-mail de entrega do material.
