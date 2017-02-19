= O que fazer?

  - Client
    - Minificar arquivos
    - Melhorar imagens do site
      - Usar imagens já do tamanho correto, tamanho necessário a mais.
      - Remover METADADOS http://kraken.io http://tynpng.com https://jakearchibald.github.io/svgomg/
        - **lossless** | Não perde qualidade das imagens apenas remover informacoes desnecesarias METADADOS
        - **lossy** | Reescreve o arquivo perde qualidade porém fica menor


  - Server
    - Habilitar compress (gzip)
    - Usar **cache**

  - Diminuir numeros de REQUEST
  - Criar **SPRITES** http://imagemmagick.com
    - convert origem -append destino
  - **SVG**
    - https://jonathantneal.github.io/svg4everybody/
  - **Inline** com JS importantes e pequenos
  - **Paralelizar** REQUEST, mude o hostname


= Comandos / Ferramentas
  - UglifyJS
    - npm install uglifyjs -g
      - uglifyjs file.js -o outout.js
  - Automação de tarefa GULP
    - gulp copy | copia arquivos
    - imgmin
  - Gulpuseref
  - Spritesmith
  - Sprity
  - Svg-sprite
  - gulp imagemin
  - gulp minify
  - gulp useref
  - Inlinesource
  - REV | coloca versao do arquivo no nome do arquivo para cache eh bom

= Obsvervações

  - Tamanho arquivo pesa o site
  - Servidor HTTP com **nginx**
    - nginx -s reload | recarrega arquivo de configuracao
    - gzip on; / Bom para arquivos de texto
    - Só comprime HTML por padrao, tem que mudar com o comando
      - gzip_types application/javascript

    - location /assets{expires 1d;} | Habilitar tempo de cache para determinado local de arquivos
  - Servidor HTTP Google App Engine SDK for PHP
  - HTTP ARCHIVE | Site mostra performance de varios sites
  - SVG é vetorial, redimencionar apenas que sao bitmap
  - Remover METADADOS das fotos usando http://kraken.io http://tynpng.com
  - **SVG** eh um arquivo XML
    - <svg<defs><symbol id=""></symbol></defs></svg>
    - https://jonathantneal.github.io/svg4everybody/
  - Ferramentas
    - **Imageoption** faz otimizacao lossless
    - **jpegtran** -optimize -progressive origem > destino
    - **pngcrush**
    - **svgo**
      - npm install svgo -g
    - Pagespeed | Performance do site
    - WebPageTest | Performance do site
  - HTTP fa apenas **6** _REQUEST_ simultaneos
  - Baixar um unico arquivo atrapalha no CACHE
  - Colocar no HTML os js que sao PEQUENOS e que podem se importantes para o conteudo
  - **HTML** deve ter menos que **14kbs** minificado e com todos os recursos, por causa dos 10 segmentos TCP
  - Trabalhar com 3 HOSTS NAMES no maximo
  - Servidor fala para o navegador fazer cache com HEADER HTTP
    - Cache-control | Tempo em segundos
      - SE adicionar **public** qualquer intermediaria pode fazer o cache
  - Wpostats da casos de performance
