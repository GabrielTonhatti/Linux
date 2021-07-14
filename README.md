Comandos Linux
==============

<img src = "https://logosmarcas.net/wp-content/uploads/2020/09/Linux-Logo.png" alt = "Linux">

+ obs: Algumas imagens e descrições foi usado como base do site <a href = "https://diolinux.com.br/"> Diolinux</a>, que é o meu site favorito sobre linux. 😁

<a href = "#ubuntu"> Ubuntu </a>
<a href = "#fedora"> Fedora </a>
<a href = "#arch-linux"> Arch Linux </a>
<a href = "#snap"> Snap </a>
<a href = "#flatpak"> Flatpak </a>

***
## Mudar a senha do root:
Se você tentou usar o comando "su", para entrar no modo superuser, e deu que a senha do root está errada, tem como mudar a senha dele, é bem simples, para mudar a senha do root, primeiros usaremo o comando:

```
sudo passwd root
```

Depois de digitar e confirmar a nova senha, temos que desbloquear o uso dela:

```
sudo passwd -u root
```
***

# Comandos básicos do Linux:

## CD

O comando "cd" serve para você navegar dentro dos diretórios pelo terminal, o comando "cd nomedapasta" é para você entrar na pasta que você quer, e "cd .." para voltar uma pasta, exemplo:

```
cd Documentos
```

Ele vai entrar no diretório "Documentos", e caso você queira voltar uma pasta, basta digitar:

```
cd ..
```

Que ele vai voltar para a pasta anterior da pasta "Documentos", que normalmente é a pasta principal, que fica o usuário, que seria a pasta "/home/nomedousuario".

## PWD

O comando pwd vai mostar em qual diretório você está, passando o caminho completo, por exemplo digamos que você esteja na pasta Fontes, que está dentro da pasta Downloads, se você digitar o comando:

```
pwd
```

Ele vai mostrar "/home/nomedousuario/Downloads/Fontes", sendo "/" o diretório principal do Linux, e "/home" onde fica os usuários.

## LS

O comando "ls", serve para você listar os arquivos dentro de um diretório(pastas) em que você está, ou outro diretório, passando o caminho completo. Por exemplo, digamos que você está na pasta "Documentos", se você digitar um "ls" e der Enter, ele vai mostrar todos os arquivos que tem na pasta "Documentos", exemplo:

```
ls
```

Se você quer ver todos os arquivos do diretório, incluindo os arquivos ocultos(que começam com ".", exemplo: ".git"), basta digitar:

```
ls -a
```

Se você quer ver os arquivos em formato de lista, e com as data de modificação e tamaho de cada pasta/arquivo, basta digitar:

```
ls -l
```

E se você quer ver das duas últimas formas juntas, basta digitar:

```
ls -la
```

Ele vai mostrar todos os arquivos em formato de lista, incluindo os arquivos ocultos.

E se você quer ver oque tem em outro diretório sem ter que entrar nele, basta digitar o "ls" seguido do caminho do diretório, exemplo:

```
ls /home/gabriel/Downloads
```

Ele vai listar todos os arquivos dentro do diretório Downloads, e "gabriel" é o nome de usuário.

## MKDIR

O comando "mkdir" serve para você criar um novo diretório, basta digitar:

```
mkdir nomedapasta
```

Exemplo:

```
mkdir Pasta-de-Exemplo
```

Se você quer separar o nome da pasta por espaço, basta digitar usando "\" para separar os nomes, por exemplo:

```
mkdir nome\ da\ pasta
```

Exemplo:

```
mkdir Pasta\ de\ Exemplo
```

Se você não colocar a "\", ele vai criar várias pastas cada uma com um nome que foi separado pelo espaço. Caso você queira criar uma pasta em outro diretório basta passar o caminho completo de onde você quer criar a pasta:

```
mkdir nome\ da\ pasta /home/nomedeusuario/Documentos
```

Exemplo:

```
mkdir Pasta\ de\ Exemplo /home/gabriel/Documentos
```

## Touch

O comando "touch" é parecido com o "mkdir", so que ele é para criar arquivos e não diretórios, por exemplo para criar um arquivo de bloco de notas, basta digitar:

```
touch arquivo.txt
```

Exemplo:

```
touch comandos-linux.txt
```

Depois do "." você sempre coloca a extensão do arquivo que você quer criar, .txt para arquivos de texto comum, que é os de bloco de notas, .js para arquivos JavaScript e etc.

## RMDIR

O comando "rmdir" server para você excluir permanentemente diretórios vazios, ele não exclui diretórios que contenham arquivos dentro. Para usá-lo basta digitar:

```
rmdir nomedapasta
```

Exemplo:

```
rmdir Pasta\ de\ Exemplo
```

## RM

O comando "rm" é parecido com o "rmdir", ele também exclui permanentemente, ele é mais usado para excluir arquivos, mas também tem como usá-lo para excluir diretórios que estejam cheios, então TOME BASTANTE CUIDADO quando for usá-lo. Para usá-lo para excluir algum arquivo basta digitar:

```
rm nomedoarquivo
```

Exemplo

```
rm comandos-linux.txt
```

Para excluir um diretório usando o "rm", basta adicionar um "-r" depois do "rm", por exemplo:

```
rm -r nomedapasta
```

Exemplo

```
rm -r Pasta\ de\ Exemplo
```

Ele vai excluir permanentemente o arquivo/pasta, então tome cuidado quando for usá-lo para não apagar algum arquivo ou diretório que não queira.

## NANO

O comando "nano" é um editor de arquivos pelo terminal, ele serve para você editar o arquivo pelo próprio terminal sem ter que abrir algum outro programa de edição de texto, exemplo:


```
nano nomedoarquivo.extensao
```

Exemplo

```
nano comandos-linux.txt
```

Para salvar oque foi editado pelo "nano", basta apertar as teclas "Crtl + S", e para sair basta apertar "Ctrl + X".

## MV

O comando "mv" serve para você mover arquivos ou pastas para outro diretório, mas tome cuidado ao usar, pois se você não passar o caminho corretamente você pode perder o arquivo ou pasta, ou se mover para algum diretório que tenha algum arquivo/pasta com o mesmo nome, ele vai sobrescrever o arquivo. Para usá-lo basta digitar:

```
mv nomedoarquivo caminhoparaondequermover
```

Exemplo:

```
mv comandos-linux.txt /home/gabriel/Imagens
```

Se você quer mover vários arquivos ou pasta de uma vez, basta digitar o nome de todos os arquivos ou pastas antes do caminho, separados por espaço. Exemplo:

```
mv comandos-linux.txt Estudos/ fontes.zip /home/gabriel/Imagens
```

Ele vai mover todos os arquivos e pastas digitados para o diretório "Imagens".

## CP

O comando "cp" é parecido com o comando "mv", a diferença que ele é para copiar e não para mover, mas caso você copie para um diretório que tenha algum arquivo/pasta com o mesmo nome, ele também vai sobrescrever com o "mv" faz. Para usá-lo basta digitar:


```
cp nomedoarquivo caminhoparaondequermover
```

Exemplo:

```
cp comandos-linux.txt /home/gabriel/Imagens
```

Se você quer copiar vários arquivos de uma vez, basta digitar o nome de todos os arquivos ou pastas antes do caminho, separados por espaço. Exemplo:

```
cp comandos-linux.txt fontes.zip /home/gabriel/Imagens
```

Ele vai copiar todos os arquivos digitados para o diretório "Imagens". Para copiar alguma pasta com o comando "cp", basta colocar um "-r" depois do "cp" para ele copiar o diretório. Exemplo:

```
cp -r Linux/ Estudos/ fontes/ /home/gabriel/Imagens
```

## Wget

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

Antes de ensinar como compactar e descompactar, vamos ensinar como instalar alguns formatos de compactação que não vem padrão no Linux.

## 7-Zip:

Para instalar o 7-Zip no Ubuntu basta digitar:

```
sudo apt install p7zip-full
```

No Fedora basta digitar:

```
sudo dnf install p7zip
```

No Arch Linux basta digitar:

```
sudo pacman -S p7zip
```

## RAR:

Para instalar o formato rar no Ubuntu, basta digitar:

```
sudo apt install rar unrar
```

## Gzip e Bzip:

Para instalar o formato .gz e .bz2 no Arch Linux, basta digitar:

```
sudo pacman -S gzip bzip2
```

Ele vai instalar  os dois pacotes juntos, o gzip e o bzip já vem como padrão no Ubuntu e Fedora, e para qualquer outro programa que você queira instalar, você pode instalar vários de uma vez só, basta digitar o comando de gerenciador de pacotes da distro, no caso do Ubuntu o apt, o Fedora o dnf, e o Arch Linux o pacman, e install com o nome dos pacotes separados por espaço, no caso do Arch é um pouco diferente, no lugar de "install", é "-S", que seria referente a "install", das outras distros,  exemnplos:

Ubuntu:

```
sudo apt install gimp krita inkscape obs-studio
```

Fedora:

```
sudo dnf install gimp krita inkscape obs-studio
```

Arch Linhx:

```
sudo pacman -S gimp krita inkscape obs-studio
```

Nos três exemplos será instalado o Gimp, o Krita, o Inkscape e o Obs Studio.

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

****

<p id = "ubuntu">

<img src = "img/Ubuntu_logoib.svg" width = "200" alt = "Ubuntu"> <img src = "img/logo-mint.png" width = "200" alt = "Linux Mint"> <img src = "img/logo-debian.png" width = "200" alt = "Debian"> 

Ubuntu é um sistema operacional (pt-BR) ou sistema operativo (pt-PT) de código aberto, construído a partir do núcleo Linux, baseado no Debian e utiliza GNOME como ambiente de desktop de sua mais recente versão com suporte de longo prazo (LTS). É desenvolvido pela Canonical Ltd.

Geralmente é executado em computadores pessoais e também é popular em servidores de rede, geralmente executando a versão Ubuntu Server, com recursos de classe empresarial. Até 2017, o Ubuntu também estava disponível para tablets e smartphones, com a edição Ubuntu Touch.

A proposta do Ubuntu é oferecer um sistema que qualquer pessoa possa utilizar sem dificuldades, independentemente de nacionalidade, nível de conhecimento ou limitações físicas. O sistema deve ser constituído principalmente por software livre e deve também ser isento de qualquer taxa.

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

<p id = "arquivos.">
E caso você tenha se perguntado, "E para instalar o Google Chrome?" ou o Discord, ou qualquer outro programa famoso que não está nessa lista, é bem simples, porque alguns programas não fica junto de outros programas do gerenciador de pacotes do Ubuntu/Debian, e para instalar esse programas é bem simples, digamos que você queira instalar o Google Chrome, o mais querido navegador de todos(e ao mesmo tempo "odiado" por usar muita memória RAM), para isso basta você pesquisar no navegador que veio como padrão no Ubuntu/Debian(normalmente é o FireFox), "download Chrome" ou "Download Google Chrome", e vai aparecer alguns links de opções para você entrar e baixar, assim como você faria no Windows.

<img src = "img/google.png" alt = "Google Chrome">

Clicando na página "Navegador da Web Google Chrome", vai entrar na seguinte tela:

<img src = "img/chrome.jpeg" alt = "Google Chrome">

Igual no Windows mesmo, clicando no botão de "Fazer o download do Google Chrome", vai aparcer outra janela pedindo pra você escolher o formato da extensão do arquivo:

<img src = "img/download-chrome.png" alt = "Google Chrome">

Se você estiver usando o Ubuntu, Debian, Linux Mint ou qualquer outra distro baseada no Ubuntu ou Debian, sempre baixe o formato ".deb", que é o padrão de extensão para distros baseadas no Debian, depois de ter baixado, ele vai gerar um arquivo como esse:

<img src = "img/instalacao-chrome.png" alt = "Terminal">

Os arquivos ".rpm" são para as distros que usam o RPMFusion como gerenciador de arquivos e programas, como o Fedora, RedHat, OpenSuse, etc.

Para instalá-lo é bem simples, ou você pode dar um duplo clique no arquivo que ele vai abrir a lojinha do Linux e é so você clicar em "instalar", ou pode fazer isso pelo terminal. Para instalar pelo terminal é bem simples, basta digitar:

```
sudo dpkg -i nomedoarquivo.deb
```

Exemplo:

```
sudo dpkg -i google-chrome-stable_current_amd64.deb
```

O "-i" é o "install" do gerenciador de pacotes ".deb" do dpkg, assim como o "install" para o "apt".

Ou

```
sudo apt install ./nomedoarquivo.deb
```

Exemplo:

```
sudo apt install ./google-chrome-stable_current_amd64.deb
```

E depois que o comando terminar de rodar, ele vai ter instalado o Google Chrome, depois disso é so abrir e usar ele como qualquer outro programa, e você pode fazer isso pra instalar o Discord, ou qualquer outro programa com a extensão ".deb".


E se você quiser remover algum programa com a extensão ".deb" que você tenha instalado, basta digitar:

```
sudo dpkg -r nomedoprograma
```

Exemplo:

```
sudo dpkg -r google-chrome
```

O "-r" é referente ao "remove" do apt, e colocando apenas o nome que o sistema reconhece o programa já vai remove-lo, eu prefiro usar o "sudo apt install ./nomedoarquivo.deb", pois além de ser mais fácil de lembrar quando se está iniciando, ele da menos problemas de pacotes quebrados comparado ao "dpkg -i".

</p>

Caso você tenha algum problema com pacotes quebrados, tem como resolver essas dependencias. Para fazer isso, é necessário listar os pacotes quebrados no Ubuntu e, em seguida, os usuários do Ubuntu podem consertar os pacotes quebrados via linha de comando. Se uma instalação de pacote falhar no Linux Ubuntu, isso pode causar alguns problemas.

Por exemplo, o gerenciador de pacotes congela ou fica bloqueado. É um problema usar o Ubuntu corretamente enquanto os pacotes do sistema estão quebrados. Felizmente, existem algumas maneiras de resolver o problema.

Se você souber o nome do pacote quebrado, poderá removê-lo manualmente usando o seguinte comando.

```
sudo dpkg –remove -force –force-remove-reinstreq NOME_DO_PACOTE_VAI_AQUI
```

Exemplo:

```
sudo dpkg –remove -force –force-remove-reinstreq google-chrome
```

Se você não tiver certeza sobre o nome do pacote quebrado, siga os comandos abaixo:

### Comando 1

```
sudo apt-get –fix-broken install
```

### Comando 2

Se uma instalação do pacote do Ubuntu falhar (devido às dependências), execute os seguintes comando:

```
sudo apt-get clean
```

```
sudo apt-get install -f
```

```
sudo dpkg –configure -a
```

### Comando 3

```
sudo rm /var/lib/apt/lists/* -vf
```

```
sudo apt-get update
```

### Comando 4

```
sudo apt-get clean
```

```
sudo apt-get autoclean
```

```
sudo apt-get autoremove
```

### Comando 5

```
sudo dpkg –configure -a
```

```
sudo apt-get update
```
### Conclusão

Espero que uma dessas correções tenham funcionado para você e que o sistema volte a trabalhar normalmente. Lembre-se que a melhor maneira de lidar com uma situação totalmente é tentar voltar ao que era antes.

## OBS:. Tente não instalar novos pacotes pensando em resolver uma quebra no Ubuntu, a menos que você saiba exatamente o que está fazendo. É provável que você acabe com um emaranhado de coisas quebradas que serão mais difíceis de resolver.

Agora basta aproveitar e usufruir o Ubuntu da melhor maneira que você puder. Caso, venha acontecer novamente este problema, basta recorrer novamente aos comandos aqui listados.

Essas informações foram tiradas do site <a href = "https://sempreupdate.com.br/como-corrigir-pacotes-quebrados-no-ubuntu/"> SempreUpdate</a>.

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

Fedora (conhecido como Fedora Core antes da versão 7) é um sistema operacional (pt-BR) ou sistema operativo (pt-PT) Linux. O sistema operacional Fedora Linux é software livre e de código aberto, e os programas disponíveis dentro de seu repositório de programas também são programas livres que aderem a uma licença livre.

O Fedora Linux existe desde 2003, e seu desenvolvimento e suporte é oferecido pela comunidade do Projeto Fedora. Após ter descontinuado o sistema operacional Red Hat Linux, a Red Hat patrocina o desenvolvimento do sistema operacional Fedora, se envolvendo no desenvolvimento de vários programas disponíveis para o Fedora, que são eventualmente adicionados para o repositório do Red Hat Enterprise Linux, que é a distribuição Linux atual da empresa.

Desde a versão Fedora 21, há três edições disponíveis: Fedora Workstation, focado para computadores pessoais, Fedora Server para servidores, e o Fedora Cloud para servidores com foco em computação em nuvem. Também existem outras edições, chamadas de "spins", com ambientes gráficos diferentes do ambiente gráfico GNOME que acompanha o sistema operacional. Ambientes gráficos como o KDE, Xfce, LXDE, entre outros, estão disponíveis. Também existem edições para usos específicos, como o uso para computação científica, astronomia, robótica, segurança e para jogos. Novas versões do Fedora são lançadas aproximadamente a cada 6 meses.

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
<p id = "arch-linux">

<img src = "img/arch-linux.png" width = "250" alt = "Arch Linux"> <img src = "img/manjaro.png" width = "250" alt = "Manjaro">

Arch Linux, ou Arch é uma distribuição Linux para computadores com arquitetura x86-64. Desenvolvido inicialmente pelo canadense Judd Vinet, esse sistema operacional se apresenta de maneira diferente de outros, como Windows e MacOS. Além de ser composto predominantemente por software livre e de código aberto, ele envolve contribuições da comunidade.

O desenvolvimento é focado na elegância, minimalismo e simplicidade no código, e espera que o usuário faça alguns esforços para compreender o modo de funcionamento do sistema. O gerenciador de pacotes, Pacman, foi escrito especialmente para o Arch Linux e é usado para instalar, remover, pesquisar e atualizar os pacotes do sistema.

O Arch Linux usa o modelo rolling release. Com esse sistema, os usuários podem ter acesso às últimas atualizações estáveis dos pacotes e também evita atualizações muito grandes que podem gerar erros nos componentes do sistema. As imagens de instalação lançadas pela equipe do Arch são apenas capturas instantâneas de imagens de disco atualizadas dos principais componentes do sistema.

Usuários da distribuição podem criar facilmente seus próprios pacotes compatíveis com o pacman usando ferramentas como o "Arch Build System", funcionalidade esta que ajudou a sustentar o AUR, um repositório de pacotes criados por usuários que complementam os repositórios oficiais.

O Arch seria uma distro Linux mais "Hardcore" digamos, pois para você instalar ele, você mesmo tem que "criar" o sitema, instalar tudo por linhas de comando, não é que nem outras distros como o Ubuntu ou Fedora ou muitas outras que tem uns instalador pronto, que você apenas define coisas básicas do sistema como região, idioma, teclado, nome de usuário e so clicar em instalar, você mesmo tem que reparticionar o disco até mesmo chegara instalar a interface gráfica dele. No caso do Manjaro Linux que tem umas instalação simples como as outras distros, e é baseado no kernel do Arch, usando o mesmo gerenciador de pacotes o "pacman", então se você quer instalar o Arch Linux, o recomendado  é que você tenha um pouco de conhecimento em Linux, pode começar por qualquer distro como o Ubuntu, Linux Mint, Debian, Fedora, popOS, entre outros. O mais recomendado para quem está entrando no mundo Linux é que comece pela distro Ubuntu ou Linux Mint, ou qualquer outra distro baseada no Ubuntu, pois terá uma interface mais "amigável", com fácil aprendizado.

E se você quer ir por mundo do Arch, mas não quer ir sem saber nada de como funciona, pode tentar primeiro o Manjaro, já que o mesmo tem uma instalação bem simples.

Da mesma forma que no Ubuntu/Debian ou qualquer outra distro Linux, devemos sempre atualizar o sistema antes de instalar qualquer programa, e para atualizar o Arch Linux/Manjaro basta digitar:


```
sudo pacman -Sy
```

ou

```
sudo pacman -Syyu
```

Para fazer sincronização total com os pacotes e fontes do Arch, e atualizar tudo que precisar.


O "pacman" é o gerenciador de pacotes do Arch/Manjaro, e o "-S" é para instalar algum pacote, e o "-Sy" para sincronizar com as fontes de instalação do Arch e verificar se tem alguma atualização, se tiver atualização, ele vai perguntar se você deseja atualizar ou não o sistema como no Ubuntu ou Fedora.

Para verificar se tem alguma atualização no Arch, basta digitar:

```
sudo pacman -Qu
```


</p>

***
<p id = "snap">

<img src = "img/snapcraft.png" width = "600" alt = "Snap">

Site do <a href = "https://snapcraft.io/" target = "_blank"> Snapcraft</a>.

Snappy é um software de implantação e um sistema de gerenciamento de pacotes originalmente projetado e construído pela Canonical para o sistema operacional Ubuntu phone. Os pacotes, chamados de 'snaps' e a ferramenta para usá-los, 'snapd', funcionam por toda uma gama de distribuições Linux e, portanto, permitem implantação de software upstream de forma distro-agnostic. O sistema é projetado para funcionar em smartphones, nuvem, internet das coisas e ambiente de desktop.

Pacotes de software "snap" são auto-contidos e o funcionam por toda uma gama de distribuições Linux. Essa é uma abordagem diferente do pacote Linux tradicional, como o APT ou o RPM, que exigem pacotes especificamente adaptados para cada distribuição de Linux. Isso adiciona atraso entre o desenvolvimento de aplicações e de sua implementação para os usuários finais.

Snaps não possuem dependências de nenhuma loja de aplicativos, podem ser obtidos a partir de qualquer fonte e pode ser utilizado para implantação de software upstream. Quando snaps são implantados no Ubuntu e em outras versões de Linux, a loja de aplicativos do Ubuntu é utilizada como padrão de back-end, mas outras lojas podem ser ativados.

</p>

***
<p id = "flatpak">

<img src = "img/flathub-logo.png" width = "400" alt = "Flatpak">

Site do <a href = "https://flathub.org/home" target = "_blank"> Flathub</a>.

O Flathub tem como objetivo ser o lugar para obter e distribuir aplicativos para Linux. Ele é desenvolvido por Flatpak, que permite que aplicativos Flathub sejam executados em quase todas as distribuições Linux.

Flatpak, anteriormente conhecido como xdg-app, é um utilitário para implantação de software, gestão de pacote e virtualização para Linux. Uma aplicação empacotada no formato Flatpak provê um ambiente sandbox onde o usuário pode executar programas em isolamento do resto do sistema, ou seja, onde cada aplicação empacotada possui apenas as bibliotecas necessárias para a execução do programa.

Aplicações usando Flatpak necessitam de autorização prévia do usuário para usar o hardware ou acessar arquivos do sistema, semelhante aos aplicativos para o sistema operacional Android.

Diferente do Snappy, o Flatpak foi desenvolvido para ser descentralizado, permitindo adicionar diferentes fontes de programas. Uma fonte popular de aplicativos no formato Flatpak é o Flathub. Atualmente, alguns programas populares disponíveis inclui Mozilla Firefox, GIMP, Inkscape, LibreOffice, Pitivi, KDE Applications, e alguns não oficiais como Chromium, Blender, Spotify, Skype, Discord, e Steam.


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
