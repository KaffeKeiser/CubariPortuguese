# Disclaimers: 
* Não tenho ligação alguma com os responsáveis pelo site.
* Esta documentação tem o intuito de tornar o cubari mais acessível e prático.
* Fontes: [Como hospedar uma série do imgur com o cubari](https://www.reddit.com/r/manga/comments/mcicbp/sl_how_to_host_a_series_on_imgur_with_guyamoe/); [Lista de sites/apps que usam a API do Mangadex](https://www.reddit.com/r/mangadex/comments/nn584s/list_of_appssites_that_currently_use_the_mangadex/); muitos usuários que me ajudaram a entender melhor como tudo é feito (menção honrosa) e meus conhecimentos próprios.

# [O que é o Cubari?](https://cubari.moe/)
* É um site que espelha imagens de outros sites e as exibe em um formato adequado para ler mangás, com uma interface personalizada. 
+ Sites compativeis: [Imgur](https://imgur.com/), [GoogleDrive](https://www.google.com/intl/pt/drive/), [AmazonWebServices](https://aws.amazon.com/pt/), [Mangadex](https://mangadex.org/), [Mangasee](https://mangasee123.com/) e [NHentai](https://nhentai.net/).
* Você encontrará alguns textos em inglês nas páginas do site, eles estão traduzidos [aqui](https://github.com/SrW0nka/CubariPortuguese/wiki). 


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

Nota¹: Usarei o [Imgur](https://imgur.com/) de exemplo (é o mais fácil de trabalhar), contudo pode ser feito com qualquer dos sites mencionados acima.

Nota²: * Visite um exemplo funcional [aqui](https://cubari.moe/read/gist/GatinhosExtremamenteFofosPtBR/) (códidgo do exemplo: [Gatinhos extremamentes fofos](https://github.com/SrW0nka/CubariPortuguese/blob/main/GatinhosExtremamenteFofosPtBR)).

**1 Passos inicias**
* Crie uma conta no [GitHub](https://github.com/) (Obrigatório para: Imgur, GD e AWS) e no [Imgur](https://imgur.com/).

**2 Upando para a nuvem**

Nota¹: Utitlize um Desktop/Notebook.

Nota²: Se você ja tem os álbuns imgur que quer utilizar pule para o passo 3
* Coloque o capítulo em uma pasta qualqer (Tenha certeza que os arquivos estão na ordem correta).
* Vá para o [Imgur](https://imgur.com/) e clique no botão [NewPost](https://imgur.com/upload). Em seguida, clique no botão **Choose Photo/Video** e navegue até a pasta em que suas imagens estão.
* Uma janela do explorador de arquivos deve ter aparecido. Selecione a última imagem do capítulo, segure shift e clique na primeira imagem do capítulo.
* Clique em **abrir** e aguarde o upload dos arquivos (não saia da página, um CAPTCHA pode ser solicitado). 
* Nomeie seu álbum (nome de sua preferência) e a publique como **Hidden/Privado**.
* Repita isso para todos os capítulos que desejar (cada capítulo deve ter seu próprio álbum).

**3 Configurando o GitHub + 4 Criando a página da obra**
* Na [página inicial](https://github.com/) clicque em **[New](https://github.com/new)** (canto superior esquerdo), nomeie o repositório, certifique-se de que a opção **Public** esteja marcada e clique em **Create repository** (Se desejar marque a opção **Add a README file**).
<a href="https://imgur.com/GL7whho"><img src="https://i.imgur.com/GL7whho.png" title="source: imgur.com" /></a>
* Clique em **Add File** e em **Create new file** na página principal do repositório. Dê ao arquivo o nome que você quiser, tenha certeza de que o nome seja algo que você não irá alterar (toda vez que você alterar o nome o link do cubari precisará ser refeito).
* No página do **Create new file** cole o [ModeloIMGUR](https://github.com/SrW0nka/CubariPortuguese/blob/main/ModeloIMGUR).
* Preencha todos os campos que as setas **< e >** circundam com as informações que deseja (se lembre de removê-las).

Nota¹: Para o campo **< id imgur >**, pegue o link imgur do álbum que deseja adicionar e selecione a cadeia alfanumérica após **imgur.com/a/** na url. 

Nota²: Para o campo **< hora que foi upado >**, use o site [UnixTimeStamp](https://www.unixtimestamp.com/) e utilize o Unix Timestamps do horáro atual (você também pode pegar um Unix Timestamp de um dia anterior mais abaixo no mesmo site).

* Uma vez feito isso, clique em **commit new file**.
* Na página do aquivo, clique em **raw** e copie a url mostrada na barra de endereços. 

Nota: Agora você terá duas opções, criar uma url aleatória ou uma personalizada (dica: comece por uma aleatória).

* **Aleatória:** Vá até [git.io](https://git.io/), cole a url do aquivo "**https://raw....**" e encurte-a. Copie a url encurtada e cole-a na caixa de busca do [Cubari](https://cubari.moe/) (esse vai ser o link link fixo para página cubari da obra).
* **Personalizada:** Pege a ulr do aquivo "**https://raw....**" e em seguida edite-a com esté comando: "**curl https://git.io/ -i -F "url=url_do_arquivo" -F "code=url_personalizada**". Após editar cole o comando no **terminal/cmd** e aperte enter.
<a href="https://imgur.com/soz3jX2"><img src="https://i.imgur.com/soz3jX2.png" title="source: imgur.com" /></a>

Nota¹: Essa URl é única, ou seja não há outra igual, escolha com sabedoria (use: **NomeDaObraPtBR**, assim outra pessoa poderá criar uma url pareceida, ex: **NomeDaObraEng**).

Nota²: Se você ja fez uma url aleatória ou quer mudar o link personalizado, altere o nome do arquivo, assim você conseguirá criar uma nova url (personalizada ou aleatória).

* Pegue sua url personalizada (destacada em azul) e cole-a na caixa de busca do [Cubari](https://cubari.moe/) esse vai ser o link link fixo para página cubari da obra.

 **5 Adicioando novos capítulos**
* Volte para o arquivo github que você criou anteriormente e edite-o (ícone do lápis).
* Copie o texto do capítulo anterior.

<a href="https://imgur.com/sfvjkUj"><img src="https://i.imgur.com/sfvjkUj.png" title="source: imgur.com" /></a>

* Adicione uma "**,**" na chave abaixo de **"last_updated"** (destacado em vermelho).
* Aperte **Shift+Enter** e cole o que você copiou.
* Altere as informações necessárias (destacado em roxo).

<a href="https://imgur.com/ma1cnoS"><img src="https://i.imgur.com/ma1cnoS.png" title="source: imgur.com" /></a>
* Uma vez terminadas todas as alterações, clique em **commit changes**.

**6 Adicionais**
* Para os sites: [Mangadex](https://mangadex.org/), [Mangasee](https://mangasee123.com/) e [NHentai](https://nhentai.net/)  basta apenas pegar o ID das obras (encontre ele no link da mesmas) e colar na caixa de busca do cubari. 
* Para os sites: [GoogleDrive](https://www.google.com/intl/pt/drive/) e [AmazomWebServices](https://aws.amazon.com/pt/) o processo é o mesmo que o do [Imgur](https://imgur.com/), contudo algumas partes tem que ser modificadas (Visite: [ModeloGD](https://github.com/SrW0nka/CubariPortuguese/blob/main/ModeloGD) ou [ModeloAWS](https://github.com/SrW0nka/CubariPortuguese/blob/main/ModeloAWS)).
* Caso precise de ajuda visite o [meu servidor do discord](https://discord.gg/qdZ7tbJxjV)
