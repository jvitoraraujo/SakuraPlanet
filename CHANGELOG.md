# Changelog

## 1.2.4 — Novembro de 2026

### Correções
- Cartão em branco na sidebar do celular: vinha dos gadgets de anúncio (`AdSense1` e `HTML9 – Publicidade`), que ficavam como cartão vazio quando o anúncio não carregava. Agora eles só aparecem como cartão quando há anúncio; sem anúncio ficam recolhidos.
- O recolhimento usa altura zero, e não `display:none`, para que o AdSense continue conseguindo preencher o espaço.

## 1.2.3 — Novembro de 2026

### Correções
- Removido o gadget HTML4, um gadget vazio com `<br />` usado só como espaçador abaixo do menu. No celular ele aparecia como um cartão em branco junto aos gadgets da sidebar.
- O espaço entre o menu e o corpo do blog agora é feito por CSS (`.main-inner`), igual no computador e no celular.
- Os gadgets técnicos sem conteúdo visível (botão de voltar ao topo e script do AddToAny) não geram mais cartões vazios na sidebar. O botão continua funcionando.

## 1.2.2 — Novembro de 2026

### Revisão do arquivo exportado do Blogger
- Incorporadas as alterações feitas no Blogger: nova imagem do cabeçalho (1024×417, `logo-sakura-planet-2026.png`) e cores dos links do gadget alinhadas à paleta (`#1175a4`).
- Corrigida a origem da barra de navegação, que o export deixou como `localhost` em vez de `https://www.blogger.com`.
- A logo do cabeçalho passou a usar as dimensões reais da imagem configurada (`data:width` e `data:height`), e não mais 1100×430 fixos.
- Adicionado `rel="noopener"` ao link de feed.
- Mantidas as normalizações feitas pelo Blogger (`version='1'`, estilos `shrinkToFit`, tags autofechadas).

## 1.2.1 — Novembro de 2026

### Celular
- **Logo realmente responsiva.** O banner era um `background-image` com altura mínima fixa de 430 px e largura de 1100 px, por isso não encolhia. O cabeçalho agora usa uma `<img>` real, que escala com a tela (até 340 px de largura em telas de até 480 px).
- O título e a descrição do blog continuam no HTML, ocultos visualmente (acessibilidade e SEO).
- Removidos os limites de altura da versão 1.2.0, que não surtiam efeito.

## 1.2.0 — Novembro de 2026

### Celular
- Margens negativas do cabeçalho removidas no celular.
- Menu de pílulas substituído por um **menu suspenso** (botão "☰ Menu") em telas de até 860 px. Fecha ao tocar num item, fora do menu ou com Esc.
- Sem JavaScript, o menu continua em pílulas.

## 1.1.0 — Novembro de 2026

### Layout
- Sidebar alinhada à área de posts: mesmo topo, mesmo espaçamento (`--sp-gap`) e mesmo raio e sombra de cartão.
- A data do post deixou de flutuar sobre o cartão e não desloca mais o primeiro post.
- Colunas reescritas com flexbox: posts flexíveis e sidebar de 300 px; abaixo de 860 px, a sidebar vai para baixo dos posts.

### Celular
- O celular passou a usar o mesmo layout do site, no lugar do modelo simplificado do Blogger.
- Viewport único (`width=device-width`) e script de reserva que troca `?m=1` por `?m=0`.
- Menu em duas colunas, paginação compacta, comentários e rodapé empilhados.
- Imagens, iframes e tabelas dentro de posts e widgets limitados à largura da tela.
- Cabeçalho (logo) sem a versão de texto simplificada.

## 1.0.0 — Novembro de 2026

### Identidade visual
- Paleta rosa, azul e branco centralizada em variáveis CSS (`--sp-*`).
- Removidas as cores fora da identidade: verde, amarelo, roxo, magenta, bege e vermelho escuro.
- Menu em pílulas rosa sólidas, com hover azul.
- Títulos da sidebar em rosa sólido, sem a imagem do Imgur.
- Posts, citações, comentários, rodapé e botão de voltar ao topo recoloridos.
- Tipografia unificada: Trebuchet no texto e Sofia, Playball e Cookie nos títulos.
- Logo recolorida para a paleta, com a ilustração intacta.

### Novo
- Paginação numerada própria, com alternativa nativa do Blogger.
- Botão de voltar ao topo em JavaScript puro.

### Correções
- CSS inválido: regra quebrada em `.content-inner`, chave solta, comentários `//`, `font-style: bold` e `font: century gothic`.
- Condicional de navegação com dois `<b:else/>` seguidos.
- Link "Leia mais" com `<a>` aninhado.
- Atributo `async` sem valor no `<script>`, que quebrava a leitura do XML.

### Desempenho e segurança
- Removido jQuery 1.3.2 em `http://`.
- Script do AdSense carregado uma vez, com o parâmetro `client`.
- Três chamadas de fontes unidas numa só.
- Links e imagens migrados para `https` e para `sakuraplanetscc.blogspot.com`.
- Removidos o botão do Google+, o bloqueio do botão direito do mouse e o CSS morto (qTip, Photobucket).
- `rel="noopener"` em links externos com `target="_blank"`.

### Conteúdo
- Rodapé com ano automático.
- Texto da sidebar atualizado para "há mais de 15 anos".
