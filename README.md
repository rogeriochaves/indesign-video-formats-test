## Testes de Formatos com vídeo do InDesign

Fiz alguns testes com texto e vídeo simples no InDesign pra ver como ele se comportaria em diferentes formatos e dispositivos. O objetivo é que esses vídeos funcionem a partir de um link externo, pra que os arquivos não fiquem com vários megas ou gigas de tamanho.

Com PDF não ficou muito legal, o vídeo só funciona se você abrir o PDF no Adobe Reader, e tiver o Flash Player instalado. O vídeo simplesmente não aparece no PDF se abrir ele com o Chrome ou o leitor de PDF padrão do Mac.

O arquivo final ficou com apenas 76kb, e no Adobe Reader ficou assim:

![Vídeo no PDF](/screenshots/mac-adobe-reader.gif)

Já em epub o resultado foi mais legal. Um problema é que a exportação padrão do InDesign remove os vídeos externos ao gerar o arquivo, tive que reinseri-lo direto no código fonte do epub, pra isso tive que abrir o arquivo epub, editar e depois fechar de novo.

Mas o arquivo final ficou com apenas 75kb, e rodou perfeitamente no iBooks do Mac:

![Vídeo em epub no Mac](/screenshots/mac-ibooks.gif)

### iPhone ###

Porém, quando fui rodar no iBooks do iOS, o vídeo não abria, então descobri que estava faltando uma propriedade no XML de metadados do epub, pra funcionar direito, temos que colocar uma propriedade sendo mais explícitos que os vídeos são externos. Liz Castro explica melhor [neste post](http://www.pigsgourdsandwikis.com/2013/05/linking-to-external-video-and-audio-in.html)

E agora sim, funcionou perfeitamente também no iPhone:

<img alt="Vídeo em epub no iPhone" src="/screenshots/iphone-ibooks1.png" width="320" />
<img alt="Vídeo em epub no iPhone" src="/screenshots/iphone-ibooks2.png" width="320" />

### Android ###

Fui então tentar rodar o ePub do Android, mas não tenho nenhum android real então usei um emulador de tablet Android. Não consegui abrir o ePub no Google Play Books, que parece ser o leitor mais comum pra usuários android, o arquivo dá erro ao fazer upload, tentei também direto pelo google play books na web, sem sucesso.

Mas existem outros leitores de ebook no android, o [Moon+ Reader](https://play.google.com/store/apps/details?id=com.flyersoft.moonreader) funcionou bem:

![Vídeo no Moon+](/screenshots/android-moon+.png)

### Outros ###

Ainda não sei como o livro ficaria no Kindle, que tem um formato próprio (.mobi), mas seria legal tentar usar uma ferramenta como [Calibre](http://calibre-ebook.com/) e ver o que acontece, mas não tenho um Kindle pra testar. [Pelo que parece](https://en.wikipedia.org/wiki/Comparison_of_e-book_formats) a maioria dos Kindles não suporta, apenas o app do kindle pra iOS.

Testei também dois leitores web, pra abrir o epub direto do Chrome, e tanto o [MagicScroll](http://www.magicscroll.net/) quanto o [Readium](http://readium.org/) funcionaram perfeitamente.

### Resumindo: ###

O formato epub parece bem promissor, já que pode ser criado facilmente com InDesign e é um formato bem abrangente com um padrão bem sólido, é questão de tempo até todos os leitores passarem a reproduzir o formato ePub3 corretamente com todas as funcionalidades.

Uma boa ideia então é produzir seu livro em epub, pra atingir o maior número de plataformas, e colocar sempre embaixo dos videos o link dele, caso o dispositivo não tenha suporte ou algum problema ao reproduzir o vídeo.

Além disso, você pode ainda pode transformar o epub em html para ser lido de qualquer lugar que tenha um browser, e talvez até colocar esse html dentro de um app android e um iOS para vender no Google Play e Apple Store :)
