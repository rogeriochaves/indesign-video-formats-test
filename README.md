## Testes de Formatos com vídeo do InDesign

Fiz alguns testes com texto e vídeo simples no InDesign pra ver como ele se comportaria em diferentes formatos e dispositivos. O objetivo é que esses vídeos funcionem a partir de um link externo, pra que os arquivos não fiquem com vários megas ou gigas de tamanho.

Com PDF não ficou muito legal, o vídeo só funciona se você abrir o PDF no Adobe Reader, e tiver o Flash Player instalado. O vídeo simplesmente não aparece no PDF se abrir ele com o Chrome ou o leitor de PDF padrão do Mac.

O arquivo final ficou com apenas 76kb, e no Adobe Reader ficou assim:

![Vídeo no PDF](/screenshots/mac-adobe-reader.gif)

Já em epub o resultado foi mais legal. Um problema é que a exportação padrão do InDesign remove os vídeos externos ao gerar o arquivo, tive que reinseri-lo direto no código fonte do epub, pra isso tive que abrir o arquivo epub, editar e depois fechar de novo.

Mas o arquivo final ficou com apenas 75kb, e rodou perfeitamente no iBooks do Mac:

![Vídeo em epub no Mac](/screenshots/mac-ibooks.gif)

Porém, quando fui rodar no iBooks do iOS, o vídeo não abria, então descobri que estava faltando uma propriedade no XML de metadados do epub, pra funcionar direito, temos que colocar uma propriedade sendo mais explícitos que os vídeos são externos. Liz Castro explica melhor [neste post](http://www.pigsgourdsandwikis.com/2013/05/linking-to-external-video-and-audio-in.html)

E agora sim, funcionou perfeitamente também no iPhone:

<img alt="Vídeo em epub no iPhone" src="/screenshots/iphone-ibooks1.png" width="320" />
<img alt="Vídeo em epub no iPhone" src="/screenshots/iphone-ibooks2.png" width="320" />

Ainda preciso testar se funciona no Android, não tenho como fazer isso.
