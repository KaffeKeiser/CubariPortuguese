# Disclaimers: 
* Não tenho ligação alguma com os responsáveis pelo site.
* Esta documentação tem o intuito de tornar o cubari mais acessível e prático.
* Fontes: [Como hospedar uma serie do imgur com o cubari](https://www.reddit.com/r/manga/comments/mcicbp/sl_how_to_host_a_series_on_imgur_with_guyamoe/); [Lista de sites/apps que usam a API do Mangadex](https://www.reddit.com/r/mangadex/comments/nn584s/list_of_appssites_that_currently_use_the_mangadex/); muitos usuarios que me ajudaram a entender melhor como tudo é feito (menção honrossa) e meus conhecimentos próprios.

# [O que é o Cubari?](https://cubari.moe/)
* É um site que espelha imagens de outros sites e as exibe em um formato adequado para ler mangás, com uma interface personalizada. 
+ Sites compativeis: [Imgur](https://imgur.com/), [GoogleDrive](https://www.google.com/intl/pt/drive/), [AmazomWebServices](https://aws.amazon.com/pt/), [Mangadex](https://mangadex.org/), [Mangasee](https://mangasee123.com/) e [NHentai](https://nhentai.net/).
* Você encontrará alguns textos em inglês nas páginas do site, esles estão traduzidos [aqui](https://github.com/SrW0nka/CubariPortuguese/wiki). 


# Por quê usar o Cubari? 
* Independência. Com o Cubari você não fica refém dos grandes sites, faça edições, modificações e ajustes nas imagens a qualquer hora.
* Velocidade.
* Não necessita de um site/servidor dedicado. 
* Processo totalmente gratuito.
* Sincronização entre dispositivos (Utilizando o [5apps](https://5apps.com/storage), mais detalhes [aqui](https://github.com/SrW0nka/CubariPortuguese/wiki/7-Sincroniza%C3%A7%C3%A3o-de-dados)).
* [Extensão no tachiyomi](https://tachiyomi.org/extensions/#all.cubari), com suporte oficial dos criadores. 
* Livre de anúncios.
* Projeto de código aberto.

# Como criar uma página no Cubari? 
?Passos iniciais
* Crie uma conta no [Imgur](https://imgur.com/) e no [GitHub](https://github.com/)

?Upando para o Imgur (Suporta GoogleDirve, AmazonServers e Mangadex também)
* Coloque o capítulo em uma pasta qualuqer (Tenha certeza que os arquivos estão na ordem correta)
* Vá para o [Imgur](https://imgur.com/) e clique no botão [NewPost](https://imgur.com/upload). Em seguida, clique no botão "Choose Photo/Video" e navegue até a pasta em que suas imagens estão.
* Uma janela do explorador de arquivos deve ter aparecido. Selecione a última imagem do capítulo, segure shift e clique na primeira imagem do capítulo
* Clique em "abrir" e aguarde o upload dos arquivos. Depois de fazer isso, nomeie sua galeria (Você pode escolher entre "community" (Público) ou "hidden" (Privado), Nota adicional: Recomedo "hidden")
* Repita isso para todos os capítulos que desejar
<a href="https://imgur.com/rFYxonU"><img src="https://i.imgur.com/rFYxonU.png" title="source: imgur.com" /></a>
Ps. No fim você vai ter algo como isso (Nota adicional: Os nomes dessas galerias não precisam ser iguais ao do script)

?Configurando o GitHub
* Em seguida, vá para o github e pressione o botão verde "New" no canto superior esquerdo. Em seguida, nomeie o repositório e certifique-se de que seja público e crie o repositório (Nele você vai botar todas as suas páginas Cubari)
<a href="https://imgur.com/tVO4WTa"><img src="https://i.imgur.com/tVO4WTa.png" title="source: imgur.com" /></a>
* Em seguida, clique em “Add File>Create new file” na seção de configuração rápida. Dê ao arquivo o nome que você quiser, mas certifique-se de que o nome seja algo que você não irá alterar (toda vez que você alterar o nome, o link do url será alterado) Nota adicional: Você terá que refazer o link do cubari caso mude o nome
* No campo “Edit new file” cole o codigo que está [nestá página](https://github.com/SrW0nka/CubariPortuguese/blob/main/Exemplo)
* Em seguida, preencha todos os campos que os <> circundam (Nota adicional: Você também deve remover as chaves "<" e ">"). 
* OBS: Para o campo "id imgur", vá para o imgur e pegue o Imgur ID (a cadeia alfanumérica após imgur.com/a/ na url) do capítulo que você deseja hospedar e cole-o. Uma vez feito isso, clique em "commit new file".
* Em seguida, volte para o arquivo, clique em "raw" e depois copie a url. Vá até [git.io](https://git.io/), cole a url e encurte-a. Copie a url encurtada e cole-a na caixa de busca do [Cubari](https://cubari.moe/). Esta será a url permanente para a página Cubari criada (desde que você não mude o nome do arquivo no github)
* OBS: Se você deseja uma url personalizada você deve pegar a url do aquivo (Com o /raw), em seguida edite esté comando "curl https://git.io/ -i -F "url=link do github" -F "code=url personalizada" (Após isso copie e cole no terminal/cmd e aperte enter) (Você deve mudar o nome do arquivo no github, para poder gerar um novo link. Nota adicional: Apenas faça isso se você ja encurtou o link no git.io) 
<a href="https://imgur.com/BxBUhin"><img src="https://i.imgur.com/BxBUhin.png" title="source: imgur.com" /></a>
Ps. Essa URl é fixa, ou seja não há outra igual, escolha com sabedoria. (Dica: faça seus testes com uma url aleatória, do git.io, e so depois use uma personalizada)

 ?Adicioando novos capítulos
* Volte para o código github que você escreveu anteriormente e edite-o (ícone do lápis).
* Copie o texto do capítulo anterior

<a href="https://imgur.com/5XSheby"><img src="https://i.imgur.com/5XSheby.png" title="source: imgur.com" /></a>
* Cole abaixo do ultimo capitulo adicionado (Não se esqueça de adicionar a virgula (Vermelho) e mudar as inforações caso necessário (Verde))

<a href="https://imgur.com/uOCyOqR"><img src="https://i.imgur.com/uOCyOqR.png" title="source: imgur.com" /></a>
* Uma vez terminados todos os capítulos, clique em "commit changes".
* OBS: Se você quiser adicionar informações sobre a hora do upload, substitua "hora que foi upado" por um unixtimestamp do [UnixTimeStamp](https://www.unixtimestamp.com/)

?Adicionais
* Caso precise de ajuda visite: https://discord.gg/dgA3zdkfSX
