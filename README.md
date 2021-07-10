Comandos Linux
==============

<img src = "https://logosmarcas.net/wp-content/uploads/2020/09/Linux-Logo.png" alt = "Linux">

+ obs: Algumas imagens e descrições foi usado como base do site <a href = "https://diolinux.com.br/"> Diolinux</a>, que é o meu site favorito sobre linux. 😁

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

<img src = "img/Ubuntu_logoib.svg" width = "200" alt = "Ubuntu"> <img src = "img/logo-mint.png" width = "200" alt = "Linux Mint"> <img src = "img/logo-debian.png" width = "200" alt = "Debian"> 

### Obs: Os comandos citados aqui serve tanto para o Ubuntu, quanto para o Linux Mint e o Debian, ou qualquer outra distro baseada no Debian ou Ubuntu.

Aqui vamos passar alguns comando do Ubuntu(a distro linux mais famosa), mas oque vamos mais passar aqui vai ser alguns programas para instalar no Ubuntu.

Caso você seja iniciante no linux, quando você acaba de instalar o Ubuntu(ou qualquer outra distro linux), primeiramente antes de instalar qualquer coisa, devemos atualizar o sistema, e para isso é bem simples, basta digitar:

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

## Unity Tweak Tool

<img src = "img/unity+tweak+tool.png" alt = "Unity Tweak Tool">

O Unity Tweak Tool é uma das melhores ferramentas para fazer ajustes na interface Unity (se não for a melhor), com ele você conseguirá, inclusive, mover facilmente a barra lateral do Unity para a parte de baixo da tela, que é uma das novidades dessa versão. Para instalar o Unity Tweak Tool digite o comando:

```
sudo apt install unity-tweak-tool
```

## Gufw
<img src = "img/informe-gufw.jpg" alt = "Gufw">

Gufw é o firewall padrão do Ubuntu, Linux. Atua com interface gráfica para o Uncomplicated Firewall (ufw), que roda nas camadas mais básicas do Linux. Sem muitos mistérios e de fácil configuração, o Gufw permite que usuários criem regras, gerenciem perfis de uso para a ferramenta, liguem ou desliguem o firewall, tenham acessos a logs e monitorem o comportamento de aplicativos em tempo real, observando que portas cada um deles acessam para se comunicar com a Internet.

O Gufw facilita o controle do firewall iptables, embutido nas fundações do Linux: sem o Gufw, o controle do firewall teria que ser realizado via linhas de comando que não é exatamente acessível a todos os usuários. Com interface que inspira simplicidade, o Gufw reserva funções e recursos que são suficientes para que o usuário doméstico garanta sua segurança e privacidade enquanto navega pela Internet.

Para instalar o gufw basta digitar:

```
sudo apt install gufw
```

## Synaptic
<img src = "img/synaptic-no-ubuntu.webp" alt = "Synaptic">

O Synaptic é um programa de computador com uma interface gráfica amigável desenvolvido em GTK+ para o sistema de gerenciamento de pacotes APT, utilizado no Debian GNU/Linux e em outras distribuições que utilizam o APT.

Para instalá-lo basta digitar:

```
sudo apt install synaptic
```

## VLC

<img src = "img/vlc-header.jpg" alt = "VLC">
O VLC é um reprodutor de Vídeo e Áudio, sendo usado tanto para reproduzir músicas quanto vídeos.

Para instalar ele, basta digitar:

```
sudo apt install vlc
```

## GParted

<img src = "img/gparted-interface-grafica.png" alt = "GParted">

GParted (ou Gnome Partition Editor) é o aplicativo GNOME para edição de partições. ... É usado para criar espaço para novos sistemas operacionais (operativos em Portugal), reorganizar o uso do disco rígido, copiar dados e "espelhar" uma partição em outra.

```
sudo apt install gparted
```

## Obs Studio
<img src = "img/obs.jpg" alt = "Obs Studio">

O OBS é uma suíte de software gratuita e de código aberto para gravação e transmissão ao vivo. Escrito em C e C ++, o OBS fornece captura de fonte e dispositivo em tempo real, composição de cena, codificação, gravação e transmissão. ... O áudio pode ser codificado usando os codecs MP3 ou AAC.

Para instalá-lo basta digitar:

```
sudo apt install obs-studio
```

## Alacarte
<img src = "img/alacarte.png" alt = "Alacarte">

Talvez você não conhece o nome Alacarte ( que é o nome real do programa ) mas conheça descrição dele, editor de Menu Principal.

Com ele você pode editar os menus do Ubuntu e do Linux Mint, o próprio Mint traz essa ferramenta com o sistema, onde você pode acrescentar itens, remover itens, exibir ou ocultar programas e categorias, trocar os ícones dos programas, trocar o endereço do executável, etc.

Para instalar basta digitar:

```
sudo apt install alacarte
```

## Gimp

<img src = "img/gimp.jpg" alt = "Gimp">

GIMP é um programa de edição e criação de imagens para Windows, Mac e Linux. Ele é uma boa alternativa gratuita ao Photoshop e conta com uma série de ferramentas e recursos, como pincéis e efeitos para fotografias. O editor ganhou interface única, permitindo ao usuário abrir várias janelas distintas.

Para instalá-lo basta digitar:

```
sudo apt install gimp
```

## Krita

<img src = "img/krita.jpg" alt = "Krita">

Krita é uma ferramenta de criação de ilustrações, concept art, histórias em quadrinhos, pinturas digitais, animações, possibilitando também ser usado como um programa de retoques e manipulação de fotografia, conversor de formatos, suportando vários modelos de cores e pintura HDR. Ele é também uma alternativa ao Gimp, mas você pode usar os dois se quiser.

Para instalá-lo basta digitar:

```
sudo apt install krita
```

## Inkscape

<img src = "img/inkscape.png" alt = "Inkscape">

Inkscape é um software livre para editoração eletrônica de imagens e documentos vetoriais, com base numa versão mais avançada do antigo Sodipodi no qual teve origem. Trata-se assim de um fork considerado de sucesso.

Para instalá-lo basta digitar:

```
sudo apt install inkscape
```

## Winff

<img src = "img/winff-screenshot.jpg" alt = "Winff">

WinFF possibilita que os usuários interajam com FFmpeg utilizando os botões , menus, campos de formulários e listas em vez de usar a linha de comando. A tela padrão permite aos usuários criar uma lista de arquivos para a conversão e para especificar configurações diferentes para cada arquivo. WinFF pode reproduzir arquivos em fila e visualizar as configurações de conversão diferentes , lançando ffplay , um media player baseado em FFmpeg que vem com o programa. WinFF pode transcodificar entre qualquer um dos formatos de vídeo na biblioteca libavformat multimídia, incluindo MPEG, H.261 cru, H.263 e H.264 , PMP , AVI e MOV. WinFF está disponível para Windows e Linux.

Para instalá-lo basta digitar:

```
sudo apt install winff
```

## Ranger

<img src = "img/ranger_code.png" alt = "Ranger">

O Ranger é um gestor de arquivos de linha de comando (CLI), escrito em Python. O programa possui todas as funções presentes nos gestores mais usados, como o Nautilus, no Ubuntu.

```
sudo apt install ranger
```

## NCDU

<img src = "img/ncdu2.png" alt = "NCDU">

Ncdu é uma utilitário de comando de linha, que ajudará a avaliar o espaço em disco no UNIX e distribuições LINUX. Ncdu é um analisador de uso de disco com uma interface ncurses que pode ser utilizada principalmente em terminais texto.

Para instalá-lo basta digitar:

```
sudo apt install ncdu
```

## Neofetch

<img src = "img/neofetch1.jpg" alt = "Neofetch">

Neofetch é uma ferramenta desenvolvida para criar protetores de tela de console que mostram informações sobre o sistema, hardware e software.

Para instalá-lo basta digitar:

```
sudo apt install neofetch
```

## Screenfetch

<img src = "img/screenfetch.png" alt = "Screenfetch">

screenFetch: Informações do sistema e algumas firulas via terminal. screenFetch é um script que desenha a logo da sua distribuição em formato ASCII no terminal, trazendo também as informações básicas do computador, como por exemplo, sistema operacional, Kernel, processador, memoria ram e etc.

Para instalá-lo basta digitar:

```
sudo apt install screenfetch
```

## LibreOffice

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

## Mudar o Terminal

Se você instalou algum outro terminal no linux e quer mudar o terminal, ou quer voltar para o terminal padrão(gnome-terminal), caso o que tenha sido instalado mudou para ele automaticamente, basta digitar:


```
sudo update-alternatives --config x-terminal-emulator
```

Vai aparecer uma lista com todos os terminais instalados, e basta selecionar qual você quer.

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