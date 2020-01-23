# Guia Linux básico
A idéia deste guia é de apenas auxiliar com os primeiros passos. 

Linux já é utilizado amplamente por empresas de tecnologia tanto para infraestrura como para desenvolvimento de sistemas e nos ultimos vem crescendo tambem os usuarios . Durante a gradução e vida profissional na area de computação, vamos sempre nos deparar com um terminal do linux. 

## Linux 

Basicamente, o Linux nada mais é que um Kernel, ou seja, é o software responsavel por conectar o hardware (computador, dispositivo embarcado) com o software (Sistema Operacional). 

![Kernel logo](/img/Kernel_basic.png)
[Fonte](https://manjarobrasil.wordpress.com/2015/08/02/o-que-e-kernel/)

A distribuição linux ou Sistema Operacional que vamos usar será o Ubuntu. Existem diversas distribuições mas não será o nosso foco no momento.
>
>Informações técnicas são encontradas de forma vasta na internet, abaixo deixo apenas alguns links, não se restrinja apenas a eles:
>[link1](https://www.linuxfoundation.org/)
>[link2](https://pt.wikipedia.org/wiki/Distribui%C3%A7%C3%A3o_Linux#/media/Ficheiro:Linux_Distribution_Timeline.svg)
>[link3](https://boilingsteam.com/arch-manjaro-still-going-strong/)
>>


# Conhecendo e utilizando o Terminal 

O terminal do linux ou **Shell** é para os iniciantes no linux algo de outro mundo e causa um pouco de expanto. Não tem nada disso, o terminal nada mais é que um software que interpreta os comandos digitados pelo usuario e executa em baixo nivel no hardware. 

Vamos tratar apenas de comandos básicos e mais utilizados por quem utiliza o linux diariamente. 


## Abrindo o terminal

A forma mais facil de abrir o terminal é atraves do atalho:

 > Crtl+Alt+T
 
 Neste momento nos deparamos com a janela do terminal aberta pronta para receber os primeiros comandos.
 
 > engecorp@engecorp:~$ 

 
 
 
 Completar uma palavra
 preciona o tab

como navegar entre diretorios e arquivos e arquivos

Comando de navegação
pwd
ls
cd 

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





