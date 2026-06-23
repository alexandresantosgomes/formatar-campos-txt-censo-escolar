 # Formatar Campos — Arquivo TXT do Censo Escolar

  Ferramenta web **standalone** (um único arquivo `.html`) para inspecionar os arquivos `.txt`
  gerados pelo Censo Escolar (Educacenso), que são pipe-delimited (`|`) e têm dezenas/centenas de
  campos por linha. Ela facilita **descobrir a posição de cada campo** sem precisar contar os `|` na mão.

  ## Para que serve
  Cada linha do arquivo começa com o tipo de registro (`00`, `10`, `20`, `30`, `40`, `50`, `60`...)
  seguido dos campos separados por `|`. A ferramenta quebra cada linha, agrupa por registro e mostra
  os valores em tabela, com o número da posição (`001`, `002`, ...) no cabeçalho.

  ## Funcionalidades
  - **Entrada flexível:** cole o conteúdo no campo de texto **ou** carregue/arraste o arquivo `.txt`.
  - **Abas por registro:** uma aba para cada tipo (`00`, `10`, `20`, ...), com a contagem de linhas e a
    faixa de linhas de origem (ex.: `Linhas: 3 a 52`).
  - **Tabela posicional:** nº da linha de origem na 1ª coluna e a posição de cada campo (`001`, `002`,
    ...) no cabeçalho; cabeçalho e 1ª coluna fixos (sticky) ao rolar.
  - **Destaque cruzado (crosshair):** ao passar o mouse, a coluna e a linha correspondentes são
    realçadas — como localizar uma coordenada de "xadrez".
  - **Clicar para copiar:** clique em qualquer célula para copiar o valor (com confirmação visual).
  - **Detector de linhas fora do padrão:** marca em vermelho (⚠) as linhas cujo número de campos
    difere do padrão do registro, ajudando a achar linhas corrompidas/truncadas.
  - **Performático:** renderização sob demanda por aba, lida bem com arquivos grandes (milhares de linhas).

  ## Como usar
  1. Cole o conteúdo do `.txt` ou clique em **Carregar arquivo .txt** (ou arraste o arquivo).
  2. Clique em **Processar** e navegue pelas abas dos registros.

  ## Tecnologia
  - HTML, CSS e JavaScript (jQuery) — **sem backend**, todo o processamento é local no navegador.
  - jQuery e Bootstrap 5 carregados via CDN.
