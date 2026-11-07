# Changelog

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
