Comandos Linux
==============

<img src = "https://logosmarcas.net/wp-content/uploads/2020/09/Linux-Logo.png" alt = "Linux">

+ obs: Algumas imagens e descrições foi usado como base do site <a href = "https://diolinux.com.br/"> Diolinux</a>, que é o meu site favorito sobre linux. 😁

<a href = "#ubuntu"> Ubuntu </a>
<a href = "#fedora"> Fedora </a>
<a href = "#arch"> Arch Linux </a>
<a href = "#snap"> Snap </a>
<a href = "#flatpak"> Flatpak </a>
***
Se voce gosta de usar o terminal para tudo, tem um comando que você pode usar para baixar as coisas que você quiser, basta digitar:

```
wget urlexemplo
```

Exemplo:

```
wget https://redirector.gvt1.com/edgedl/android/studio/ide-zips/4.2.2.0/android-studio-ide-202.7486908-linux.tar.gz
```

Neste link de exemplo estaremos baixando o Android Studio. Se você estiver baixando um arquivo grande, e tiver medo de dar algum problema como a energia acabar, ou a internet dar algum problema, basta usar um "-c" para fazer com que caso o download pare, ele continue de onde parou, por exemplo:

```
wget -c https://redirector.gvt1.com/edgedl/android/studio/ide-zips/4.2.2.0/android-studio-ide-202.7486908-linux.tar.gz
```

Bastando apenas você colocar o mesmo comando novamente, caso tenha tido algum problema no download que ele vai continuar de onde parou.

E se você também quer compactar ou descompactar arquivos ou pastas pelo terminal é bem simples, vou colocar uma lista com todos os formatos de arquivos que o Linux suporta e como compactar e descompactar cada um.

# Compactar e Descompactar arquivos e pastas:

## Formato .zip

Todos conhecem o formato .zip né? Ele é padrão em todos os Sistemas Operacionais, e aqui vai como compactar e descompactar pelo terminal arquivos .zip:

### Compactar:

Para compactar é bem simples basta digitar:

```
zip -r nomedoarquivo.zip nomedapasta/
```

Sendo o "nomedoarquivo.zip" o arquivo .zip que sera gerado, e o "nomedapasta/" é a pasta que será compactada. Por exemplo:

```
zip -r fontes.zip Fontes/
```

O nome do arquivo ".zip" você pode colocar o nome que quiser para identificar oque é aquele arquivo ".zip". 

Se você quer compactar vários arquivos ou pastas dentro de apenas um arquivo .zip, basta digitar:

```
zip -r nomedoarquivo.zip arquivo1 arquivo2 arquivo3
```

Exemplo:

```
zip -r fontes.zip Fontes/ Fontes-Sans-serifas/ Fontes-Personalizadas
```

Ele vai gerar um arquivo .zip com todos os arquivos que você escolheu ou com todas as pastas escolhidas sem precisar criar uma nova pasta e colocar tudo dentro de apenas uma pasta para compactar todos juntos.

Se você quer compactar alguma pasta e colocar uma senha, também é bem simples, basta digitar:

```
zip -P senha -r nomedoarquivo.zip pasta/
```

Exemplo:

```
zip -P zipando -r  fontes.zip Fontes/
```

E na hora que você ou outra pessoa for descompactar, vai pedir essa senha que você colocou, no meu caso a senha foi "zipando".
### Descompactar:

Para descompactar um arquivo ".zip" é mais simples ainda do que compactar, basta digitar:

```
unzip nomedoarquivo.zip
```

Exemplo:

```
unzip fontes.zip
```

Se você quer descompactar para outra pasta, basta digitar:

```
unzip nomedoarquivo.zip -d caminho/da/pasta
```

Exemplo:

```
unzip fontes.zip -d /home/gabriel/Downloads
```

E o arquivo será descompactado na pasta Downloads. Se você deseja ver os arquivos que tem dentro do arquivo.zip, basta digitar:

```
unzip -l nomedoarquivo.zip
```

Exemplo:

```
unzip -l fontes.zip
```

E ele vai mostrar todos os arquivos que tem dentro do arquivo.zip.

## Formato .rar

Assim como o formato ".zip" é bastante conhecido, o formato ".rar" provávelmente é mais conhecido ainda, pois a maioria das pessoas usam o famoso Winrar.
### Compactar:

Para compactar é bem simples, basta digitar:

```
rar a nomedoarquivo.rar pasta/
```

Exemplo:

```
rar fontes.rar Fontes/
```

Se você quer compactar vários arquivos ou pastas dentro de apenas um arquivo .rar, basta digitar:

```
rar a nomedoarquivo.rar arquivo1 arquivo2 arquivo3
```

Exemplo:

```
rar a fontes.rar Fontes/ Fontes-Sans-serifas/ Fontes-Personalizadas
```

Ele vai gerar um arquivo .rar com todos os arquivos que você escolheu ou com todas as pastas escolhidas sem precisar criar uma nova pasta e colocar tudo dentro de apenas uma pasta para compactar todos juntos.

Se você quer compactar alguma pasta e colocar uma senha, também é bem simples, basta digitar:

```
rar a nomedoarquivo.rar pasta/ -p
```

Exemplo:

```
rar a fontes.rar Fontes/ -p
```

E ele vai pedir para você digitar uma senha para o arquivo.

### Descompactar:

Para descompactar é bem simples também, basta digitar:

```
unrar x nomedoarquivo.rar
```

Exemplo:

```
unrar x fontes.rar
```

Para descompactar em outra pasta basta digitar:

```
unrar x nomedoarquivo.rar caminho/
```

Exemplo:

```
unrar x fontes.rar /home/gabriel/Downloads
```

E o arquivo será descompactado na pasta Downloads. Se você deseja ver os arquivos que tem dentro do arquivo.rar, basta digitar:

```
unrar l nomedoarquivo.rar
```

Exemplo:

```
unrar l fontes.rar
```

E ele vai mostrar todos os arquivos que tem dentro do arquivo.rar.

## Formato .tar

TAR ou tar (abreviatura de Tape ARchive), é um formato de arquivamento de arquivos (ficheiros). Apesar do nome "tar" ser derivado de "tape archive", o seu uso não se restringe a fitas magnéticas. Ele se tornou largamente usado para armazenar vários arquivos em um único, preservando informações como datas e permissões. Normalmente é produzido pelo comando "tar". Apesar de ser mais comum em sistemas Unix-Like, este formato é suportado pela maioria dos descompactadores para Windows, como por exemplo o 7-zip.

tar também é o nome de um programa de arquivamento desenvolvido para armazenar e extrair arquivos de um arquivo tar (que contém os demais) conhecido como tarfile ou tarball. O primeiro argumento para tar deve ser uma das seguintes opções: Acdrtux, seguido por uma das seguintes funções adicionais. Os argumento finais do tar são os nomes dos arquivos ou diretórios nos quais eles podem ser arquivados. O uso de um nome de diretório, implica sempre que os subdiretórios sob ele, serão incluídos no arquivo.

### Compactar:

Para compactar é bem simples, basta digitar:

```
tar -cvf nomedoarquivo.tar pasta/
```

Exemplo:

```
tar -cvf fontes.tar Fontes/
```

Se você quer compactar vários arquivos ou pastas dentro de apenas um arquivo .tar, basta digitar:

```
tar -cvf nomedoarquivo.tar arquivo1 arquivo2 arquivo3
```

Exemplo:

```
tar -cvf fontes.tar Fontes/ Fontes-Sans-serifas/ Fontes-Personalizadas
```

Ele vai gerar um arquivo .tar com todos os arquivos que você escolheu ou com todas as pastas escolhidas sem precisar criar uma nova pasta e colocar tudo dentro de apenas uma pasta para compactar todos juntos.

### Descompactar:

Para descompactar um arquivo ".tar", basta digitar:

```
tar -xvf nomedoarquivo.tar
```

Exemplo:

```
tar -xvf fontes.tar
```

Para descompactar em outro pasta:

```
tar -xvf nomedoarquivo.tar -C caminho/da/pasta/
```

Exemplo:

```
tar -xvf fontes.tar -C /home/gabriel/Downloads
```

E o arquivo será descompactado na pasta Downloads. Se você deseja ver os arquivos que tem dentro do arquivo.tar, basta digitar:

```
tar -tvf nomedoarquivo.tar
```

Exemplo:

```
tar tvf fontes.tar
```

ou

```
tar tf fontes.tar
```

E ele vai mostrar todos os arquivos que tem dentro do arquivo.tar.

## Formato .tar.gz

Os formatos TGZ e TBZ (ou tar.gz e tar.bz2, respectivamente) são usados para a compressão e descompressão de arquivos em sistemas Unix. No Linux, esses formatos são reconhecidos de forma nativa e os arquivos podem ser facilmente extraídos - como acontece com o .ZIP, no Windows.

### Compactar:

Para compactar um arquivo para ".tar.gz", basta digitar:

```
tar -cz nomedapasta > arquivo.tar.gz
```

Exemplo

```
tar -cz Fontes/ > fontes.tar.gz
```

ou

```
tar -zcvf arquivo.tar.gz nomedapasta/ 
```

Exemplo

```
tar -zcvf fontes.tar.gz  Fontes/
```

Se você quer compactar vários arquivos ou pastas dentro de apenas um arquivo .tar.gz, basta digitar:

```
tar -zcvf nomedoarquivo.tar.gz arquivo1 arquivo2 arquivo3
```

Exemplo:

```
tar -zcvf fontes.tar.gz Fontes/ Fontes-Sans-serifas/ Fontes-Personalizadas
```

Ele vai gerar um arquivo .tar.gz com todos os arquivos que você escolheu ou com todas as pastas escolhidas sem precisar criar uma nova pasta e colocar tudo dentro de apenas uma pasta para compactar todos juntos.

### Descompactar:

Para descompactar um arquivo ".tar", basta digitar:

```
tar -zxvf nomedoarquivo.tar.gz
```

Exemplo:

```
tar -zxvf fontes.tar.gz
```

Ou

```
tar -vzxf fontes.tar.gz
```

Ou

```
tar -xz Fontes/ < fontes.tar.gz
```

Aqui o "Fontes/" sendo o nome da pasta que será gerado após descompactar.

Ou

```
tar -czf fontes.tar.gz Fontes/
```

Como no exemplo anterior, "Fontes/" é o nome da pasta que será gerado após descompactar o arquivo.

Ou

```
tar -xzf fontes.tar.gz
```

Ou

```
tar -xf fontes.tar.gz
```

Ou

```
tar -vczf fontes.tar.gz Fontes/
```

Como em outros exemplos, "Fontes/" é o nome da pasta que será gerado após descompactar o arquivo.

Ou

```
tar -vxf fontes.tar.gz
```

Para descompactar em outro pasta:

```
tar -zxvf nomedoarquivo.tar.gz -C caminho/da/pasta/
```

Exemplo:

```
tar -zxvf fontes.tar.gz -C /home/gabriel/Downloads
```

E o arquivo será descompactado na pasta Downloads. Se você deseja ver os arquivos que tem dentro do arquivo.tar.gz, basta digitar:

```
tar -ztvf nomedoarquivo.tar.gz
```

Ou

```
tar -tvf nomedoarquivo.tar.gz
```

Ou

```
tar -tf nomedoarquivo.tar.gz
```

E ele vai mostrar todos os arquivos que tem dentro do arquivo.tar.gz.

## Formato .bz2

O formato de arquivo BZ2 é compatível com o software que pode ser instalado na plataforma do sistema Linux, Mac OS, Windows. Arquivos com extensão BZ2 são categorizados como arquivos Arquivos comprimidos. O subconjunto Arquivos comprimidos compreende 230 vários formatos de arquivo.

### Compactar:

Para compactar um arquivo para .bz2, tem quer ser so arquivos com alguma extensão mesmo, como por exemplo: "arquivo.tar", que ficará: "arquivo.tar.bz2", e para adicionar essa extensão ".bz2", basta digitar:

```
bzip2 -z nomedoarquivo.extensao
```

Exemplo:

```
bzip2 -z fontes.tar
```

Que se tornará um arquivo "fontes.tar.bz2".

### Descompactar:

Para descompactar um arquivo .bz2 é bem simples, basta digitar:

```
bunzip nomedoarquivo.bz2
```

Ou 

```
bunzip2 nomedoarquivo.bz2
```

Exemplo:

```
bunzip2 fontes.bz2
```

Ou qualquer arquivo que termine com ".bz2", no caso ele so vai remover a extensão ".bz2".

## Formato .tar.bz2

Os formatos TGZ e TBZ (ou tar.gz e tar.bz2, respectivamente) são usados para a compressão e descompressão de arquivos em sistemas Unix. No Linux, esses formatos são reconhecidos de forma nativa e os arquivos podem ser facilmente extraídos - como acontece com o .ZIP, no Windows.

### Compactar:

Para compactar um arquivo ou pasta para ".tar.bz2", basta digitar:

```
tar -jcvf nomedoarquivo.tar.bz2 pasta/
```

Exemplo:

```
tar -jcvf fontes.tar.bz2 Fontes/
```

Se você quer compactar vários arquivos ou pastas dentro de apenas um arquivo .tar.bz2, basta digitar:

```
tar -jcvf nomedoarquivo.tar.bz2 arquivo1 arquivo2 arquivo3
```

Exemplo:

```
tar -jcvf fontes.tar.bz2 Fontes/ Fontes-Sans-serifas/ Fontes-Personalizadas
```

Ele vai gerar um arquivo ".tar.bz2" com todos os arquivos que você escolheu ou com todas as pastas escolhidas sem precisar criar uma nova pasta e colocar tudo dentro de apenas uma pasta para compactar todos juntos.

### Descompactar:

Para descompactar um arquivo ".tar.bz2", basta digitar:

```
tar -jxvf nomedoarquivo.tar.bz2
```

Exemplo:

```
tar -jxvf fontes.tar.bz2
```

Para descompactar em outra pasta, basta digitar:

```
tar -jxvf nomedoarquivo.tar.bz2 -C caminho/da/pasta
```

Exemplo:

```
tar -jxvf fontes.tar.bz2 -C /home/gabriel/Downloads
```

E o arquivo será descompactado na pasta Downloads. Se você deseja ver os arquivos que tem dentro do arquivo.tar.bz2, basta digitar:

```
tar -jtvf nomedoarquivo.tar.bz2
```

Exemplo:

```
tar -jtvf fontes.tar.bz2
```

Ou

```
tar -tvf fontes.tar.bz2
```

Ou

```
tar -tf fontes.tar.bz2
```

E ele vai mostrar todos os arquivos que tem dentro do arquivo.tar.bz2.

## 7-Zip

7-Zip é um compactador de arquivos open-source para o sistema operacional Microsoft Windows e Linux. O programa, desenvolvido por Igor Pavlov, é distribuído sobre a licença GNU LGPL, e compete diretamente com os programas de código-fechado WinZip e WinRAR. 

Com ele você pode usar para compactar para qualquer formato listado anteriormente, e até mesmo para o formato .7z.

### Compactar:

Para compactar é bem simples, basta digitar:

```
7z a nomedoarquivo.extensao pasta/
```

Exemplo:

```
7z a fontes.7z Fontes/
```

Ou

```
7z a fontes.tar Fontes/
```

Ou

```
7z a fontes.zip Fontes/
```

Ou qualquer outro formato que você queira.

### Descompactar:

Para descompactar um arquivo com o 7-Zip, basta digitar:

```
7z e arquivo.extensao
```

Exemplo:

```
7z a fontes.7z
```

Ou

```
7z a fontes.tar
```

Ou

```
7z a fontes.zip
```

A desvantagem de descompactar usando o 7-Zip, é que ele não vai descompactar da mesma forma que os outros comandos, criando uma pasta com o mesmo nome da pasta que tinha sido compactada ou o mesmo nome do arquivo so que sem o ".extensao", ele vai descompactar tudo que tem dentro do arquivo na pasta atual que você está. Mesmo que você compacte uma pasta ou arquivo com o 7-Zip, se você usar o formato de decompactação padrão da extensão que você escolheu, ele vai descompactar normal criando uma pasta para descompactar tudo, diferente do 7-Zip.

## Mudar a senha do root:
Se você tentou usar o comando "su", para entrar no modo superuser, e deu que a senha do root está errada, tem como mudar a senha dele, é bem simples, para mudar a senha do root, primeiros usaremo o comando:

```
sudo passwd root
```

Depois de digitar e confirmar a nova senha, temos que desbloquear o uso dela:

```
sudo passwd -u root
```
****

<p id = "ubuntu">

<img src = "img/Ubuntu_logoib.svg" width = "200" alt = "Ubuntu"> <img src = "img/logo-mint.png" width = "200" alt = "Linux Mint"> <img src = "img/logo-debian.png" width = "200" alt = "Debian"> 

### Obs: Os comandos citados aqui serve tanto para o Ubuntu, quanto para o Linux Mint e o Debian, ou qualquer outra distro baseada no Debian ou Ubuntu.

Aqui vamos passar alguns comando do Ubuntu(a distro linux mais famosa), mas oque vamos mais passar aqui vai ser alguns programas para instalar no Ubuntu.

Caso você seja iniciante no linux, quando você acaba de instalar o Ubuntu(ou qualquer outra distro linux), primeiramente antes de instalar qualquer coisa, devemos atualizar o sistema, o apt é o gerenciador de pacotes do Ubuntu, Debian, Linux Mint e outras distros baseadas no Ubuntu ou Debian, e para atualizar o sistema é bem simples, basta digitar:

```
sudo apt-get update
```

Depois que você de enter, ele vai baixar todas as atualizações do Ubuntu, e depois para instalar as atualizações basta digitar:

```
sudo apt-get upgrade
```

Depois disso ele vai instalar as atualizações, e ele vai perguntar se você deseja ou não instalá-las, basta digitar "y"(sem as aspas) e dar enter, o y é para yes, e o n para no em inglês.

Caso você queira fazer os dois de uma vez só, tem como fazer isso, basta digitar:

```
sudo apt-get update && sudo apt-get upgrade -y
```

Ele vai rodar o comando update primeiro, e depois que ele terminar vai rodar o comando upgrade em seguida, o "-y" serve para ele responder "yes(sim)" para todas as perguntas automaticamente.

Se você deseja ver se tem mais alguma atualização no Ubuntu, basta digitar:

```
apt list --upgradable
```

E ele vai listar os programas que precisam ser atualizados, se aparecer apenas "Listining...Done", é porque não tem atualização, mas se aparecer um tanto de programas(provávelmente escritos em verde), é so rodar o comandos citados anteriormente para atualizar o sistema.
# Agora vamos colocar aqui uma lista de alguns programas que você possa se interessar:

## <p id = "playonlinux"> Playonlinux
<img src = "img/playonlinux-no-linux.webp" alt = "Gufw">

O playonlinux é um programa para instalar programas do Windows no Linux, ele é bastante famoso, pois da pra usar alguns programas do windows no próprio linux, mas as vezes o programa que você ques instalar pode não funcionar, então não fique bravo caso não funcione, porque não é um programa que funciona e instalar qualquer programa do Windows perfeitamente como se fosse no próprio Windows. Para instalar o playonlinux digite:

```
sudo apt-get install playonlinux wine winbind p7zip-full
```

Ele vai instalar o playonlinux junto com o wine, que é o o programa que simula a virtualização do Windows no Linux.
</p>


## <p id = "codecs"> Codecs Multimídia
<img src = "img/codecs.jpg" alt = "Codecs Multimídia">


Por questões de legislação, o Ubuntu não pode incluir determinados codecs multimídia, como os de MP3, para poder ser distribuído em alguns países, entre outros formatos. Qualquer pessoa que já formatou o computador com Windows sabe que tem que instalar alguns codecs para que todos os tipos de arquivos rodem no sistema, no Windows é bem comum utilizar o pack “K-Lite”, no Ubuntu, temos o Ubuntu Restricted Extras, ele está na Central de Programas, mas também pode ser baixado pelo terminal:

```
sudo apt install ubuntu-restricted-extra
```
</p>

## <p id = "unity-tweak"> Unity Tweak Tool

<img src = "img/unity+tweak+tool.png" alt = "Unity Tweak Tool">

O Unity Tweak Tool é uma das melhores ferramentas para fazer ajustes na interface Unity (se não for a melhor), com ele você conseguirá, inclusive, mover facilmente a barra lateral do Unity para a parte de baixo da tela, que é uma das novidades dessa versão. Para instalar o Unity Tweak Tool digite o comando:

```
sudo apt install unity-tweak-tool
```
</p>

## <p id = "gufw"> Gufw
<img src = "img/informe-gufw.jpg" alt = "Gufw">

Gufw é o firewall padrão do Ubuntu, Linux. Atua com interface gráfica para o Uncomplicated Firewall (ufw), que roda nas camadas mais básicas do Linux. Sem muitos mistérios e de fácil configuração, o Gufw permite que usuários criem regras, gerenciem perfis de uso para a ferramenta, liguem ou desliguem o firewall, tenham acessos a logs e monitorem o comportamento de aplicativos em tempo real, observando que portas cada um deles acessam para se comunicar com a Internet.

O Gufw facilita o controle do firewall iptables, embutido nas fundações do Linux: sem o Gufw, o controle do firewall teria que ser realizado via linhas de comando que não é exatamente acessível a todos os usuários. Com interface que inspira simplicidade, o Gufw reserva funções e recursos que são suficientes para que o usuário doméstico garanta sua segurança e privacidade enquanto navega pela Internet.

Para instalar o gufw basta digitar:

```
sudo apt install gufw
```
</p>

## <p id = "synaptic"> Synaptic
<img src = "img/synaptic-no-ubuntu.webp" alt = "Synaptic">

O Synaptic é um programa de computador com uma interface gráfica amigável desenvolvido em GTK+ para o sistema de gerenciamento de pacotes APT, utilizado no Debian GNU/Linux e em outras distribuições que utilizam o APT.

Para instalá-lo basta digitar:

```
sudo apt install synaptic
```

</p>

## <p id = "vlc"> VLC

<img src = "img/vlc-header.jpg" alt = "VLC">

O VLC é um reprodutor de Vídeo e Áudio, sendo usado tanto para reproduzir músicas quanto vídeos.

Para instalar ele, basta digitar:

```
sudo apt install vlc
```

</p>

## <p id = "audacious"> Audacious

<img src = "img/audacious.jpg" alt = "audacious">

Audacious é um tocador de mídia livre com foco em baixa utilização de recursos, alta qualidade de áudio e suporte a uma ampla variedade de formatos. É desenvolvido primariamente para sistemas POSIX como Linux e unix-like, com suporte limitado ao Microsoft Windows.

Para instalar ele, basta digitar:

```
sudo apt install audacious
```

</p>

## <p id = "qbittorrent"> qBittorrent

<img src = "img/qbittorrent.jpg" alt = "qbittorrent">

qBittorrent é um aplicativo cliente P2P multiplataforma, gratuito e de código aberto para a rede BitTorrent. O programa utiliza a biblioteca libtorrent-rasterbar para comunicação em rede. qBittorrent está escrito na linguagem de programação C++, também utiliza a biblioteca Qt.

Para quem usa o utorrent mesmo no linux, pode usar o qBittorrent no linux. 
Para instalar ele, basta digitar:

```
sudo apt install qbittorrent
```
</p>

## <p id = "flameshot"> Flameshot

<img src = "img/flameshot.webp" alt = "Flameshot">

Conheça o melhor app de captura de telas para Linux. Acredite, capturar telas no Linux vai ser uma tarefa simples com esta ferramenta open source. Flameshot possui um conjunto útil de ferramentas de marcação e seleção, incluindo desenho à mão livre, linhas, setas, caixas, círculos, realces, desfoque.

Para instalar ele, basta digitar:

```
sudo apt install flameshot
``` 

É bem provável que após instalá-lo, você vai procurar e clicar no ícone do aplicativo, e bem provável também que não vai acontecer nada, mas não fique chateado, pois para ele funcionar digite o seguinte comando no terminal:

```
flameshot gui
``` 

Se aparecer uma tela meio escura e uma mensagem explicando como usar o flameshot, é porque funcionou, ele é bem parecido com o lighshot pra quem usa o Windows, e ainda tem algumas ferramentas a mais, você pode adicionar um atalho de teclado para ele simplesmende indo em configurações > teclado > atalhos personalizados, e depois so clicar em "+", e colocar um nome para saber o atalho que é, e o comando colocar "flameshot gui", sem as aspas, igual colocou no terminal e depois colocar um atalho, se quiser pode colocar o botão PRTSC e substituir o salvamento padrão dos prints do linux.

Se você quiser também entrar nas configurações do flameshot, basta digitar:

```
flameshot config
```
<img src = "img/flameshot-config.png" alt = "Flameshot">

Ele vai abrir essa tela de configurção do flameshot.

</p>

## <p id = "gParted"> GParted

<img src = "img/gparted-interface-grafica.png" alt = "GParted">

GParted (ou Gnome Partition Editor) é o aplicativo GNOME para edição de partições. ... É usado para criar espaço para novos sistemas operacionais (operativos em Portugal), reorganizar o uso do disco rígido, copiar dados e "espelhar" uma partição em outra.

```
sudo apt install gparted
```
</p>

## <p id = "obs-studio"> Obs Studio
<img src = "img/obs.jpg" alt = "Obs Studio">

O OBS é uma suíte de software gratuita e de código aberto para gravação e transmissão ao vivo. Escrito em C e C ++, o OBS fornece captura de fonte e dispositivo em tempo real, composição de cena, codificação, gravação e transmissão. ... O áudio pode ser codificado usando os codecs MP3 ou AAC.

Para instalá-lo basta digitar:

```
sudo apt install obs-studio
```
</p>

## <p id = "alacarte"> Alacarte
<img src = "img/alacarte.png" alt = "Alacarte">

Talvez você não conhece o nome Alacarte ( que é o nome real do programa ) mas conheça descrição dele, editor de Menu Principal.

Com ele você pode editar os menus do Ubuntu e do Linux Mint, o próprio Mint traz essa ferramenta com o sistema, onde você pode acrescentar itens, remover itens, exibir ou ocultar programas e categorias, trocar os ícones dos programas, trocar o endereço do executável, etc.

Para instalar basta digitar:

```
sudo apt install alacarte
```
</p>

## <p id = "gimp"> Gimp

<img src = "img/gimp.jpg" alt = "Gimp">

GIMP é um programa de edição e criação de imagens para Windows, Mac e Linux. Ele é uma boa alternativa gratuita ao Photoshop e conta com uma série de ferramentas e recursos, como pincéis e efeitos para fotografias. O editor ganhou interface única, permitindo ao usuário abrir várias janelas distintas.

Para instalá-lo basta digitar:

```
sudo apt install gimp
```
</p>

## <p id = "krita"> Krita

<img src = "img/krita.jpg" alt = "Krita">

Krita é uma ferramenta de criação de ilustrações, concept art, histórias em quadrinhos, pinturas digitais, animações, possibilitando também ser usado como um programa de retoques e manipulação de fotografia, conversor de formatos, suportando vários modelos de cores e pintura HDR. Ele é também uma alternativa ao Gimp, mas você pode usar os dois se quiser.

Para instalá-lo basta digitar:

```
sudo apt install krita
```
</p>

## <p id = "inkscape"> Inkscape

<img src = "img/inkscape.png" alt = "Inkscape">

Inkscape é um software livre para editoração eletrônica de imagens e documentos vetoriais, com base numa versão mais avançada do antigo Sodipodi no qual teve origem. Trata-se assim de um fork considerado de sucesso.

Para instalá-lo basta digitar:

```
sudo apt install inkscape
```
</p>

## <p id = "steam"> Steam

<img src = "img/steam.png" alt = "Steam">

Steam é um software de gestão de direitos digitais criado pela Valve Corporation ou Valve L.L.C., de plataformas digitais como jogos e aplicativos de programação e fornece serviços facilitados como atualização automática de jogos, e preços acessíveis aos usuários.

Sabia que tem Steam para Linux? Isso mesmo. A famosa Steam também está neste sistema. Para quem dizia que não haviam jogos para Linux, estavam enganados. 

Para instalá-lo basta digitar:

```
sudo apt install steam
```

Mas infelizmente tem poucos jogos nativos para Linux comparado com o que tem para o Windows

</p>

## <p id = "lutris"> Lutris

<img src = "img/lutris.png" alt = "lutris">

Lutris é um gestor de jogos livre e de código aberto para sistemas operacionais baseados em Linux, desenvolvido e mantido por Mathieu Comandon e pela comunidade,listado sob a Licença Pública Geral GNU. O Lutris possibilita a instalação de diversos jogos a partir de seu site, com um único clique, e também se integra ao site do Steam. Scripts de instalação estão disponíveis para alguns jogos difíceis de ser executados na plataforma, que rodam por meio da camada WINE, como o popular League of Legends. Jogos adquiridos por meio da GOG e da Humble Bundle podem ser adicionados por meio de seus próprios lançadores no Lutris. Os jogos são executados em suas respectivas plataformas, como WINE, Steam e emuladores, e podem ser iniciados com a mediação do aplicativo Lutris. Mais de 20 emuladores são suportados, incluindo DOSbox, ScummVM, Atari 800, Snes9x, Dolphin, PCSX2 e PPSSPP.

Para instalá-lo primeiramente adicione o PPA do Lutris no seu Ubuntu com o comando abaixo:

```
sudo add-apt-repository ppa:lutris-team/lutris
```
Agora atualize os repositórios da sua distro com o comando abaixo:

```
sudo apt-get update
```
E por último, instale o Lutris com o comando:

```
sudo apt-get install lutris
```

</p>

## <p id = "winff"> Winff

<img src = "img/winff-screenshot.jpg" alt = "Winff">

WinFF possibilita que os usuários interajam com FFmpeg utilizando os botões , menus, campos de formulários e listas em vez de usar a linha de comando. A tela padrão permite aos usuários criar uma lista de arquivos para a conversão e para especificar configurações diferentes para cada arquivo. WinFF pode reproduzir arquivos em fila e visualizar as configurações de conversão diferentes , lançando ffplay , um media player baseado em FFmpeg que vem com o programa. WinFF pode transcodificar entre qualquer um dos formatos de vídeo na biblioteca libavformat multimídia, incluindo MPEG, H.261 cru, H.263 e H.264 , PMP , AVI e MOV. WinFF está disponível para Windows e Linux.

Para instalá-lo basta digitar:

```
sudo apt install winff
```
</p>

## <p id = "ranger"> Ranger

<img src = "img/ranger_code.png" alt = "Ranger">

O Ranger é um gestor de arquivos de linha de comando (CLI), escrito em Python. O programa possui todas as funções presentes nos gestores mais usados, como o Nautilus, no Ubuntu.

```
sudo apt install ranger
```
</p>

## <p id = "ncdu"> NCDU

<img src = "img/ncdu2.png" alt = "NCDU">

Ncdu é uma utilitário de comando de linha, que ajudará a avaliar o espaço em disco no UNIX e distribuições LINUX. Ncdu é um analisador de uso de disco com uma interface ncurses que pode ser utilizada principalmente em terminais texto.

Para instalá-lo basta digitar:

```
sudo apt install ncdu
```
</p>

## <p id = "neofetch"> Neofetch

<img src = "img/neofetch1.jpg" alt = "Neofetch">

Neofetch é uma ferramenta desenvolvida para criar protetores de tela de console que mostram informações sobre o sistema, hardware e software.

Para instalá-lo basta digitar:

```
sudo apt install neofetch
```
</p>

## <p id = "screenfetch"> Screenfetch

<img src = "img/screenfetch.png" alt = "Screenfetch">

screenFetch: Informações do sistema e algumas firulas via terminal. screenFetch é um script que desenha a logo da sua distribuição em formato ASCII no terminal, trazendo também as informações básicas do computador, como por exemplo, sistema operacional, Kernel, processador, memoria ram e etc.

Para instalá-lo basta digitar:

```
sudo apt install screenfetch
```
</p>

## <p id = "libreoffice"> LibreOffice

<img src = "img/libreoffice-2.png" alt = "LibreOffice">


O LibreOffice é um pacote de programas para uso profissional ou pessoal. O serviço traz opções para criar e editar textos, tabelas, apresentações, desenhos, fórmulas matemáticas e até organizar um banco de dados. Ele é uma alternativa do Microsoft Office, e é gratuito.

Se você fez a instalação mínima no Ubuntu e você quer instalar todo o pacote LibreOffice, basta digitar:

```
sudo apt-get install libreoffice
```

Se você quiser instalar apenas algum em específico como o LibreOffice Writer(Parecido com o Word), ou o LibreOffice Calc(Parecido com o Excel), ou o LibreOffice Impres(Parecido com o PowerPoint), basta digitar:

LibreOffice Writer:

```
sudo apt-get install libreoffice-writer
```

LibreOffice Calc:

```
sudo apt-get install libreoffice-calc
```

LibreOffice Impress:

```
sudo apt-get install libreoffice-impress
```

Caso deseja remvoer algum dos LibreOffice, como por exemplo o LibreOffice Impress, basta digitar:

```
sudo apt-get --purge remove libreoffice-impress
```

Ou basta colocar o nome de qual você quer remover no lugar do "impress".

</p>

## Remover programas

Para remover qualquer um dos programas que listamos anteriormente(exceto o LibreOffice que já está explicado como remover algum dos pacotes offices), é bem simples também, basta digitar:

```
sudo apt remove nomedoprograma
```

Exemplo:

```
sudo apt remove gimp
```

Ele vai remover o editor de imagens Gimp. Bem fácil não é?

## Mudar o Terminal

Se você instalou algum outro terminal no linux e quer mudar o terminal, ou quer voltar para o terminal padrão(gnome-terminal), caso o que tenha sido instalado mudou para ele automaticamente, basta digitar:

```
sudo update-alternatives --config x-terminal-emulator
```

Vai aparecer uma lista com todos os terminais instalados, e basta selecionar qual você quer.
</p>

***

<p id = "fedora">

<img src = "img/fedora.png" width = "300" alt = "fedora">

Da mesma forma que no Ubuntu/Debian ou qualquer outra distro Linux, devemos sempre atualizar o sistema antes de instalar qualquer programa, e para atualizar o Fedora basta digitar:

```
sudo dnf update -y
```

Assim como o "apt" é o gerenciador de pacotes do Ubuntu, o "dnf" é o gerenciador de pacotes do Fedora. Se deseja verificar se tem mais alguma atualização no Fedora, basta digitar:

```
dnf check-update
```
ou

```
dnf list updates
```


</p>

***
## Instalando linguagens de programação

### Java
Para instalar o Java no Ubuntu e derivados basta digitar:

```
sudo apt-get install openjdk-11-jdk
```

Caso você queira instalar outra versão do Java, basta substituir o "11" pelo número da versão que deseja, exemplo:

```
sudo apt-get install openjdk-8-jdk
```

### php

Para instalar o php no Ubuntu é mais simples ainda do que o Java, basta apenas digitar:

```
sudo apt-get install php
```

### Python 3

Caso o python 3 não venha como padrão no Ubuntu e sim o Python 2, para instalá-lo é bem simples também, basta digitar:

```
sudo apt-get install python3
```

E para colocar ele como padrão para debugar o código, basta digitar:

```
sudo rm /usr/bin/python
```

Que ele vai remover o python 2 do link do Path, e depois digitar:

```
sudo ln -s python3 /usr/bin/python
```

Que ele vai criar um novo link no Path apontando para o Pythn 3.

### NodeJs

Para instalar o node no Ubuntu ou Fedora basta seguir o link para a instalação do  <a href="https://github.com/nodesource/distributions/blob/master/README.md"> NodeJs</a>, que vai ter um README no github com todas as distros e como instalar via package manager.

### TypeScript

Se você está aprendendo TypeScript e quer instlar ele, depois de ter instalado o NodeJs, basta digitar:

```
sudo npm install -g typescript 
```

O "-g" serve para instalar ele de forma global no seu Sistema, sendo assim, não vai precisar ficar instlando ele toda vez que for criar uma pasta nova.

Para rodar o TypeScritp para saber se o código está funcionando corretamente, tem uma forma que é pelo Node igual com o JavaScript, só que não diretamente com o mesmo Node que o JavaScript usa, e sim com o Typescript Node, para instalá-lo é bem simples:

```
sudo npm install -g ts-node
```

Para importar bibiliotecas do TypeScript basta instalar o typescript-require:

```
sudo npm install -g typescript-require
```
e
```
sudo npm install -g @types/node 
```
