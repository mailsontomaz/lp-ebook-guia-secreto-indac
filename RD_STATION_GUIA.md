# Manual Oficial de Publicação — Landing Page Ebook INDAC
### "O Guia (Não Tão) Secreto Para Se Tornar Ator" · RD Station Marketing

Este guia contém as instruções definitivas para publicação, configuração de formulário, hospedagem de arquivo e automação de marketing da nova Landing Page de captura do **INDAC Escola de Atores** dentro do **RD Station Marketing**.

O código-fonte pronto para cópia e colagem está no arquivo:
👉 **[`rd_station_ebook_lp.html`](file:///c:/Users/mails/OneDrive/Área%20de%20Trabalho/INDAC/LP%20Ebook%20-%20Guia%20Secreto/rd_station_ebook_lp.html)**

---

## 1. Visão Geral da Landing Page e Design System

A página foi construída em estrita conformidade com as diretrizes do **Design System INDAC 2025** documentadas em [`Design System INDAC.dc.html`](file:///c:/Users/mails/OneDrive/Área%20de%20Trabalho/INDAC/LP%20Ebook%20-%20Guia%20Secreto/Design%20System%20INDAC.dc.html):

| Elemento | Padrão INDAC | Aplicação na LP |
| :--- | :--- | :--- |
| **Cores Principais** | Preto de Palco (`#141414`), Vermelho Cortina (`#D9342B`), Creme Refletor (`#F5F1E8`) | 70% Preto, 22% Creme, 8% Vermelho (ação e ênfase) |
| **Cores de Apoio** | Preto Suave (`#1C1C1C`), Vermelho Hover (`#A8231D`), WhatsApp (`#25D366`) | Cards de conteúdo, estados de hover e ícones |
| **Tipografia** | **Anton** (Display / Títulos), **Merriweather** (Editorial / Manifesto), **Montserrat** (Interface / Corpo) | Carregamento otimizado via Google Fonts em requisição única |
| **Raios de Borda** | **Estritamente 0 (reto) ou 999px (pílula)** | Zero cantos intermediários (sem 4px, 8px, 12px) |
| **Ícones & Mídia** | **100% Vetoriais em SVG** | **Zero GIFs**, animações CSS sutis e performáticas |

### Arquitetura de Seções:
1. **Header Fixo / Proporcional**:
   - Marca oficial INDAC com pílula vermelha vertical (`14px x 28px`), tipografia em *Anton* e subtítulo *"Escola de Atores"*.
   - Botão direto para atendimento no WhatsApp oficial (`(11) 99616-0533`).
2. **Hero de Alta Conversão**:
   - Título principal: *"O Guia (Não Tão) Secreto Para Se Tornar Ator: Tudo o que não te contam, mas que muda tudo. Sua Jornada Autêntica do Zero ao DRT"*.
   - Imagem de mockup oficial em alta resolução (`Book_and_smartphone_displaying_d…_2K_20260923191228.jpeg`) com fallback automático livre de recursão.
   - Card dramático com Skeleton Loader e formulário incorporado do RD Station (`mt-lp-ebook-guia-secreto-95bee7fc70bce7a08668`).
3. **Fluxo Pós-Conversão Inteligente (JavaScript)**:
   - Ao preencher e enviar o formulário, a página transiciona automaticamente sem recarregar a tela:
     - Botão de **download imediato** do arquivo PDF (`Ebook_Guia_Secreto_Ator_Indac_Master.pdf`).
     - Alerta visual garantindo que o lead **também recebeu uma cópia por e-mail** para acessar quando e onde quiser.
     - Chamada de destaque convidando para responder ao **Quiz de Perfil Artístico**.
4. **Seção 01 — Conteúdo Estratégico do Ebook**:
   - 4 pilares: A verdade sobre o DRT e exigências do SATED; A preparação de voz, corpo e cena; O mercado real de audições e castings; e a tradição dos 50 anos do INDAC formando o ator-criador.
5. **Seção 02 — Respiro Creme (Manifesto Teatral)**:
   - Seção editorial em fundo Creme (`#F5F1E8`) e tipografia *Merriweather* para quebrar o peso escuro e conectar o visitante com a filosofia cênica da escola.
6. **Seção 03 — Conheça Outros Caminhos no INDAC**:
   - Cards com links diretos para as experiências presenciais e de atendimento:
     - **Imersão Cênica**: [https://lp.indacescoladeatores.com.br/imersao-cenica](https://lp.indacescoladeatores.com.br/imersao-cenica)
     - **Visite o INDAC**: [https://lp.indacescoladeatores.com.br/visiteoindac](https://lp.indacescoladeatores.com.br/visiteoindac)
     - **Agendar Conversa**: [https://lp.indacescoladeatores.com.br/agendar-conversa-v1](https://lp.indacescoladeatores.com.br/agendar-conversa-v1)
7. **Seção 04 — Última Sessão: Destaque do Quiz de Perfil Artístico**:
   - Chamada de impacto com grafismo teatral em arcos aninhados: *"Qual é o seu perfil artístico?"*, convidando o lead a descobrir seus pontos fortes em 2 minutos com link para:
     - [https://lp.indacescoladeatores.com.br/quiz-perfil-artisticov1](https://lp.indacescoladeatores.com.br/quiz-perfil-artisticov1)
8. **Rodapé Oficial INDAC**:
   - Padrão oficial com endereço da sede histórica na Rua Clélia, 658 — Barra Funda, São Paulo, links de navegação rápida, telefone/WhatsApp clicável e direitos reservados.
9. **Barra Fixa Inferior Mobile**:
   - Em smartphones (telas ≤ 767px), ao rolar a página para além do formulário, uma barra flutuante discreta oferece o botão *"Baixar Ebook Gratuito"*, que após a conversão se transforma automaticamente em *"Baixar Ebook (PDF)"*.

---

## 2. Passo a Passo de Publicação no RD Station Marketing

### Passo 1: Criar a Landing Page
1. No painel do **RD Station Marketing**, acesse o menu **Converter > Landing Pages**.
2. Clique no botão **Criar Landing Page** (canto superior direito).
3. Na galeria de modelos, selecione a aba **Modelos do Sistema** e escolha **Modelo em Branco**.
4. Dê um nome à sua Landing Page (exemplo: `LP - Ebook Guia Secreto do Ator`).

### Passo 2: Configurar a Seção Base (Largura Fluida / Edge-to-Edge)
1. No editor visual do RD Station, exclua todos os blocos e linhas padrões até sobrar apenas **uma única seção vazia**.
2. Clique sobre a seção para abrir a barra lateral de propriedades (à direita):
   - **Largura da Seção**: Selecione **Fluida (100%)** ou **1600 px** (o código já possui resets completos com `!important` para preencher 100% da viewport e eliminar margens indesejadas).
   - **Espaçamento / Padding**: Defina todos os valores como **0**.
   - **Cor de Fundo**: Defina como `#141414` ou transparente.

### Passo 3: Inserir o Bloco HTML
1. No menu de componentes à esquerda do RD Station, localize o bloco **HTML** (ícone `</>`).
2. Arraste o bloco HTML para dentro da seção configurada.
3. Abra o arquivo **`rd_station_ebook_lp.html`** no seu editor de código, copie **todo o conteúdo (Ctrl+A e Ctrl+C)**.
4. Cole todo o código dentro do editor do componente HTML no RD Station.
5. Clique em **Aplicar** ou **Salvar**.

### Passo 4: Configurar o Formulário no RD Station Form Builder (CRÍTICO)
No formulário de identificador `mt-lp-ebook-guia-secreto-95bee7fc70bce7a08668`:
1. **Campos Recomendados**:
   - Nome Completo (`name`) — Obrigatório
   - E-mail (`email`) — Obrigatório
   - Telefone / WhatsApp (`phone`) — Obrigatório
   - Caixa de Consentimento LGPD (`privacy_policy`) — Recomendado
2. **Ação Pós-Conversão (Atenção Máxima)**:
   - Na aba **Ações do Formulário / Conversão**, configure:
   - ✅ **Ação pós-conversão: "Permanecer na página e exibir mensagem"** (ou mensagem personalizada de confirmação).
   - ⚠️ **NÃO escolha "Redirecionar para URL externa"**, pois o redirecionamento forçado impediria o visitante de ver o botão direto de download do PDF e o convite do Quiz que já estão implementados no card pós-conversão!

### Passo 5: Metadados e Publicação
1. Na etapa de **Configurações**:
   - **Título da Página**: `O Guia (Não Tão) Secreto Para Se Tornar Ator | INDAC`
   - **Descrição da Página (SEO)**: `Baixe gratuitamente o guia definitivo do INDAC Escola de Atores sobre o ofício cênico, preparação vocal e corporal, audições e a jornada real para o DRT.`
   - **URL da Página**: `lp.indacescoladeatores.com.br/guia-secreto-ator` (ou slug de preferência).
2. Clique em **Publicar**!

---

## 3. Como Vincular o Arquivo PDF do Ebook

O arquivo PDF master oficial do ebook é o **`Ebook_Guia_Secreto_Ator_Indac_Master.pdf`** (localizado na pasta do projeto).

### Opção A: Hospedagem direta no RD Station (Altamente Recomendado)
1. No RD Station Marketing, acesse **Conteúdo > Gerenciador de Arquivos**.
2. Faça o upload do arquivo `Ebook_Guia_Secreto_Ator_Indac_Master.pdf`.
3. Copie a URL pública gerada pelo RD Station (exemplo: `https://d335luupugsy2.cloudfront.net/medias/indac/Ebook_Guia_Secreto_Ator_Indac_Master.pdf`).
4. No arquivo `rd_station_ebook_lp.html`, localize o botão com `id="btn-download-pdf"` e substitua o valor de `href`:
   ```html
   <a href="https://d335luupugsy2.cloudfront.net/.../Ebook_Guia_Secreto_Ator_Indac_Master.pdf" download="Ebook_Guia_Secreto_Ator_Indac_Master.pdf" target="_blank" rel="noopener noreferrer" class="btn-download-ebook" id="btn-download-pdf">
     Baixar Ebook Agora (PDF)
   </a>
   ```
5. Atualize também a variável de configuração no topo do `<script>`:
   ```javascript
   var PDF_DOWNLOAD_HREF = "https://d335luupugsy2.cloudfront.net/.../Ebook_Guia_Secreto_Ator_Indac_Master.pdf";
   ```

### Opção B: Envio Automático por E-mail (Fluxo de Automação RD Station)
Para cumprir a promessa visual exibida no aviso *"Enviamos uma cópia para o seu e-mail"*:
1. No menu **Relacionar > Automação de Marketing** do RD Station:
2. Crie um novo fluxo de automação com o gatilho:
   - **Condição de Entrada**: *Converteu no evento: Formulário da LP do Ebook (`mt-lp-ebook-guia-secreto-95bee7fc70bce7a08668`)*.
3. Ação: **Enviar E-mail**.
4. Configure o e-mail de entrega:
   - **Assunto**: `Aqui está o seu Guia Secreto Para Se Tornar Ator 🎭`
   - **Corpo do e-mail**: Mensagem acolhedora com botão de download do PDF e um link convidando o aluno a fazer o **Quiz de Perfil Artístico** (`https://lp.indacescoladeatores.com.br/quiz-perfil-artisticov1`).

---

## 4. Arquitetura do Script de Detecção Pós-Conversão

O script embutido em `rd_station_ebook_lp.html` foi construído com múltiplos níveis de contingência para garantir que a tela de download e convite ao Quiz seja exibida com 100% de confiabilidade:

1. **Monitoramento Nativo de XMLHttpRequest / Fetch**:
   - Intercepta requisições de envio direcionadas às APIs do RD Station (`rdstation`, `rd.services`, `conversions`).
   - Dispara a transição de sucesso no exato momento em que o servidor do RD Station retorna status `200 OK`, eliminando temporizadores arbitrários.
2. **`MutationObserver` Inteligente**:
   - Monitora alterações no DOM do contêiner `#mt-lp-ebook-guia-secreto-95bee7fc70bce7a08668`.
   - Ignora palavras-chave durante o carregamento inicial dos campos (evitando falsos positivos).
   - Detecta o desaparecimento do formulário ou a aparição de classes como `.rd-form-success`, `.bricks-form__success` e `.submitted`.
3. **Listener de `submit` com Verificação de Erros**:
   - Registra o início da submissão e, caso o formulário não apresente mensagens de erro de validação (`.error`), fornece uma transição suave de contingência.
4. **Listeners de Custom Events e `postMessage`**:
   - Compatível com implementações em iframe e eventos customizados (`rdstation:conversion`, `rdstation.form.success`).
5. **Persistência de Sessão**:
   - Salva o estado convertido em `sessionStorage` para que, caso o lead recarregue a página, ele permaneça na tela de sucesso com acesso direto ao download.

---

## 5. Checklist de Verificação Pré-Publicação

- [x] **Identidade Visual**: Fiel ao Design System INDAC (`#141414`, `#D9342B`, `#F5F1E8`).
- [x] **Tipografia**: Anton (Display), Merriweather (Editorial) e Montserrat (UI).
- [x] **Sem GIFs**: Uso exclusivo de SVGs inline de alta performance.
- [x] **Raios de Borda**: Restritos rigorosamente a 0 (reto) ou 999px (pílula).
- [x] **Hero Image**: Mockup oficial configurado com fallback local à prova de loops recursivos.
- [x] **Formulário RD Station**: ID oficial `mt-lp-ebook-guia-secreto-95bee7fc70bce7a08668` com script estável.
- [x] **Pós-Conversão**: Download direto do PDF, aviso de cópia por e-mail e convite ao Quiz.
- [x] **Seção de Outros Caminhos**: Links funcionais para Imersão Cênica, Visite o INDAC e Agendar Conversa.
- [x] **Última Seção da LP**: Bloco destacado com arcos aninhados para o Quiz de Perfil Artístico.
- [x] **Rodapé Oficial**: Padrão INDAC com endereço da Rua Clélia e WhatsApp clicável.
- [x] **Mobile Sticky Bar**: Barra flutuante exclusiva para telas móveis com alternância pós-conversão.
