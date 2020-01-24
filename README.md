# Guia Linux básico

Este não é um curso regular de Linux, neste curso queremos ensinar conceitos básicos do Linux como navegar pelo sistema de arquivos, etc... e mostrar alguns exemplos básicos, mas com foco nas matérias de Robótica Computacional e Elementos de Sistemas para auxilia-los com os primeiros passos. 

Linux já é utilizado amplamente por empresas de tecnologia tanto para infraestrura como para desenvolvimento de sistemas e nos ultimos vem crescendo tambem os usuarios domesticos. Durante a gradução e vida profissional na area de computação, vamos sempre nos deparar com um terminal do linux. 

## Linux 

Basicamente, o Linux nada mais é que um Kernel, ou seja, é o software responsavel por conectar o hardware (computador, dispositivo embarcado) com o software (Sistema Operacional). 

![Kernel logo](/img/Kernel_basic.png)
[Fonte](https://manjarobrasil.wordpress.com/2015/08/02/o-que-e-kernel/)

A distribuição linux ou Sistema Operacional que vamos usar será o Ubuntu. Existem diversas distribuições mas não será o nosso foco.

>Informações técnicas são encontradas de forma vasta na internet, abaixo deixo apenas alguns links, não se restrinja apenas a eles:
>[link1](https://www.linuxfoundation.org/)
>[link2](https://pt.wikipedia.org/wiki/Distribui%C3%A7%C3%A3o_Linux#/media/Ficheiro:Linux_Distribution_Timeline.svg)
>[link3](https://boilingsteam.com/arch-manjaro-still-going-strong/)
>

# Conhecendo e utilizando o Terminal 

O terminal do linux ou **Shell** é para os iniciantes no linux algo de outro mundo e causa um pouco de expanto. Não tem nada disso, o terminal nada mais é que um software que interpreta os comandos digitados pelo usuario e executa em baixo nivel no hardware. 

## Abrindo o terminal

A forma mais facil de abrir o terminal é atraves do atalho:

 > Crtl+Alt+T
 
 Neste momento nos deparamos com a janela do terminal aberta pronta para receber os primeiros comandos.
 
 > engecorp@engecorp:~$ 

O nosso primeiro passo será clonar o repositório no GitHub desta aula, para isso digite no terminal os comandos abaixo:

> git clone https://github.com/arnaldojr/Linuxbasico.git


## Navegando entre diretorios e arquivos

De forma bem simplificada, podemos dizer que o sistema Linux possui 2 elementos principais: pastas e arquivos. Os arquivos armazenam dados (txt, py...) e as pastas tambem chamadas de diretórios, armazenam e organizam os arquivos. 
Sabendo disso é importante saber navegar entre os diretórios para encontrar os nossos arquivos.

## Comando "cd"

O comando **cd** é um dos comandos mais utilizados no terminal do Linux isso porque ele permite que acessemos um diretório especifico. Vamos acessar uma pasta do repositório que acabamos de clonar. 

> cd Linuxbasico/pasta1/subpasta2/subpasta3/ 

Este comando nos leva para o diretório chamado **subpasta3** passando pelos diretorios: Linuxbasico, pasta1 e subpasta2. 

Para voltar subir um nivel e acessar o diretório chamado **subpasta2** podemos digitar:

> cd ..

Para acessar a home do nosso usuario podemos fazer isso "voltando" as pastas repitindo o comando acima, ou simplismente digitando o comando: 

> cd ~

## Comanod "pwd"

Podemos verificar o diretório que estamos digitanto:

> pwd


## Comando "ls"

O comando **ls** é utilizado par exibir (listar) o conteudo de um diretório. 

> ls

## Visualização de arquivos e pastas ocultos

O comando "ls" sozinho não exibe arquivos ocultos, que são arquivos e pastas que começam com ".". Para listar esses aquivos:

> ls -a

ou para listar informações mais detalhadas:

> ls -la

Durante as aulas de robotica teremos que editar um arquivo oculto chamado ".bashrc", no momento precisamos apenas saber que este arquivo se encontra na home do usuario. digite:

> cd ~
> ls -la




Agora que estamos em nossa home podemos 


arquivos ocultos
ls -la
.bashrc
source .bashrc

criação de pasta
mkdir
criação de arquivos
> asdf.py
touch asdf.txt

Renomeando, movendo e copiando arquivos
rm -rf asdf.txt
mv
cp


ln - Cria links entre arquivos
ln -s file1 link1

dar so uma espiada no conteudo de um arquivo
cat - Exibe o conteúdo de um arquivo
head, tail - Mostra o começo e fim de um arquivo

editor de texto nano e gedit
editar e salvar alteração
nano adf.txt

Mostra os formatos básicos de arquivos compactados e como lidar com
eles no Linux.
- tar - Agrupando arquivos
- gzip, bzip2 - Compactando arquivos
- zip, rar - Outros formatos de arquivos compactados Comandos de
Tratamento de Texto

travou a tela 
xkill - mata a tela
kill, killall

sudo apt-get update = Atualiza a "lista de pacotes"
sudo apt-get upgrade = Atualiza pacotes "já instalados"
sudo apt-get install = Instala pacotes (necesário informar o nome do pacote desejado, conforme exemplo abaixo)
sudo apt-get install speedtest-cli htop nmap = Instala pacotes speedtest, htop e nmap
sudo apt-get remove = Remove pacotes instalados (necessário informar o nome do pacote desejado, conforme exemplo abaixo)
sudo apt-get remove speedtest-cli = remove pacote speedtest

 grep – Procura texto e expressões dentro de um arquivo
 
 Além de mostrar como funcionam as permissões dos arquivos no Linux,
ensina a utilizar os comandos que tratam das permissões.
- chown - Modifica os donos de arquivos e diretórios
- chmod - Modifica as permissões dos arquivos e diretórios


informaçes do sistema
ps 
cat /proc/cpuinfo - Informações sobre o processador
cat /etc/lsb-release 
- uname -a ou -r - Informações de versão do kernel, arquitetura e outros
  - lspci - Mostra informações sobre dispositivos PCI
- lsusb - Mostra informações sobre dispositivos USB
dmesg -  Mensagens de inicialização
man - Ajuda sobre algum comando, assunto ou arquivo de configuração

Utilizado em distribuições Debian, Ubuntu e seus derivados para
instalar e remover programas.
- apt-get update - Atualiza a lista de pacotes dos repositórios
- apt-cache search - Procura um pacote por palavras
- apt-get install - Instala pacotes de programas
- apt-get remove - Remove pacotes de programas do sistema
- apt-get upgrade - Atualiza todos os pacotes do sistema
- apt-get dist-upgrade - Atualiza a versão da distribuição e todos seus
pacotes
- apt-get moo - Invoca os poderes da vaca Gerenciador de pacotes: yum

Comando Sudo: No Linux por razões de segurança, o sistema operacional trabalha com permissões de usuários e, por com disso, determinados arquivos ou até mesmo comandos são só permitidos para o próprio administrador (root). O comando Sudo ajuda o usuário para que não tenha que ficar trocando de conta a todo instante, e assim, ele garante a credencial de usuário administrador temporariamente mediante a informação de uma senha. Para executar o atalho Linux Sudo, é só digitar no terminal sudo ls/root e depois que você informar a senha do seu usuário o comando será executado normalmente.





