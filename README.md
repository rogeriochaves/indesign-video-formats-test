## Testes de Formatos com vídeo do InDesign

Fiz alguns testes com texto e vídeo simples no InDesign pra ver como ele se comportaria em diferentes formatos e dispositivos. O objetivo é que esses vídeos funcionem a partir de um link externo, pra que os arquivos não fiquem com vários megas ou gigas de tamanho.

Com PDF não ficou muito legal, o vídeo só funciona se você abrir o PDF no Adobe Reader, e tiver o Flash Player instalado. O vídeo simplesmente não aparece no PDF se abrir ele com o Chrome ou o leitor de PDF padrão do Mac.

O arquivo final ficou com apenas 76kb, e no Adobe Reader ficou assim:

![Vídeo no PDF](/screenshots/mac-adobe-reader.gif)

Já em epub o resultado foi mais legal. Um problema é que a exportação padrão do InDesign remove os vídeos externos ao gerar o arquivo, tive que reinseri-lo direto no código fonte do epub.

Mas o arquivo final ficou com apenas 75kb, e rodou perfeitamente no iBooks do Mac:

![Vídeo em epub](/screenshots/mac-ibooks.gif)
