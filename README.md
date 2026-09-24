# Landing Page — Ebook "O Guia (Não Tão) Secreto Para Se Tornar Ator"
### INDAC Escola de Atores · RD Station Marketing

Landing Page de captura de alta conversão desenvolvida para ser hospedada dentro do **RD Station Marketing**, em estrita conformidade com a **Identidade Visual INDAC 2025**.

---

## 🎭 Sobre o Projeto

Esta LP tem como objetivo a captura de leads qualificados interessados na formação teatral do **INDAC - Escola de Atores**, oferecendo gratuitamente o ebook master:
> **"O Guia (Não Tão) Secreto Para Se Tornar Ator: Tudo o que não te contam, mas que muda tudo. Sua Jornada Autêntica do Zero ao DRT."**

### Principais Funcionalidades:
- **Hero de Alta Conversão**: Título de impacto em *Anton*, imagem de mockup oficial com fallback inteligente e formulário nativo do RD Station Marketing com *Skeleton Loader*.
- **Fluxo Pós-Conversão Transparente (JS)**: Sem recarregar a página, detecta o envio bem-sucedido via interceptação AJAX (`XMLHttpRequest` e `fetch`), exibindo botão direto para download do PDF (`Ebook_Guia_Secreto_Ator_Indac_Master.pdf`), aviso de envio por e-mail e convite para responder ao Quiz.
- **Seção "Conheça Outros Caminhos no INDAC"**: Cards institucionais com links para [Imersão Cênica](https://lp.indacescoladeatores.com.br/imersao-cenica), [Visite o INDAC](https://lp.indacescoladeatores.com.br/visiteoindac) e [Agendar Conversa](https://lp.indacescoladeatores.com.br/agendar-conversa-v1).
- **Última Sessão — Convite ao Quiz**: Destaque teatral em fundo escuro com arcos aninhados convidando o lead a descobrir seu perfil artístico em [Quiz de Perfil Artístico](https://lp.indacescoladeatores.com.br/quiz-perfil-artisticov1).
- **Rodapé Oficial INDAC**: Identidade institucional com endereço da sede histórica (Barra Funda/SP), canal direto de atendimento no WhatsApp e links rápidos.
- **100% Livre de GIFs**: Todos os ícones e grafismos são vetoriais (SVG inline), garantindo máxima performance, nitidez e alinhamento com a marca.

---

## 🎨 Design System INDAC 2025

- **Cores Oficiais**:
  - `Preto de Palco`: `#141414` (Fundo principal)
  - `Preto Suave / Cards`: `#1C1C1C` / `#202020`
  - `Vermelho Cortina`: `#D9342B` (Ação, destaque e badges)
  - `Vermelho Hover`: `#A8231D`
  - `Creme Refletor`: `#F5F1E8` (Texto principal e fundo de respiro)
  - `WhatsApp`: `#25D366`
- **Tipografia**:
  - *Anton* (Display / Títulos)
  - *Merriweather* (Editorial / Manifesto)
  - *Montserrat* (Interface e leitura)
- **Raios de Borda**: Estritamente `0` (cantos vivos) ou `999px` (pílulas).

---

## 📁 Estrutura de Arquivos

```text
├── index.html                                  # Versão pronta para teste local ou GitHub Pages
├── rd_station_ebook_lp.html                    # Código-fonte para copiar no componente HTML do RD Station
├── RD_STATION_GUIA.md                          # Manual passo a passo oficial de publicação no RD Station
├── Ebook_Guia_Secreto_Ator_Indac_Master.pdf    # Arquivo PDF master oficial do Ebook
├── Book_and_smartphone_displaying_d...jpeg     # Mockup oficial em alta resolução
├── Design System INDAC.dc.html                 # Especificações do Design System da marca
├── identidade visual INDAC.pdf                 # Diretrizes de marca
├── Proposta IDV - Indac.pdf                    # Proposta de Identidade Visual
└── _MANUAL DE MARCA ( INDAC ) 2025.pdf         # Manual de Marca consolidado
```

---

## 🚀 Como Publicar no RD Station Marketing

Consulte o passo a passo detalhado no arquivo **[`RD_STATION_GUIA.md`](./RD_STATION_GUIA.md)**:

1. Crie uma Landing Page usando o **Modelo em Branco**.
2. Configure a seção como **Fluida (100%)**, padding 0 e fundo `#141414`.
3. Arraste o componente **HTML (`</>`)** para a seção.
4. Cole o código de `rd_station_ebook_lp.html`.
5. No formulário do RD Station, configure a ação pós-conversão para **"Permanecer na página e exibir mensagem"**.
6. Salve e publique!
