# Guia Linux básico
A ideia deste guia é de auxiliar com os primeiros passos. 

# Linux 

Basicamente, o Linux nada mais é que um Kernel, ou seja, é o software responsavel por conectar o hardware (computador, dispositivo embarcado) com o software (Sistema Operacional). 

![GitHub Logo](/img/Kernel_basic.png)
Fonte:https://manjarobrasil.wordpress.com/2015/08/02/o-que-e-kernel/

Uma definição mais tecnica e formal pode ser encontrada nos links abaixo:


# Terminal ou Shell

O terminal do linux ou **Shell** é para os iniciantes no linux, uma coisa de outra mundo e causa um pouco de expanto. Não tem nada disso, o terminal nada mais é que uma ferramenta que interpreta os comandos digitados pelo usuario e executa em baixo nivel no sistema operacional. A ideia deste guia é passar é passarmos pelos comandos basicos e mais utilizados por quem utiliza o linux diariamente. 

Vale ressaltar que durante a gradução e vida profissional na area de engenharia de computação, vamos nos deparar com um terminal do linux. 

# Abrindo o terminal

O atalho para acessar o terminal é:

 > Crtl+Alt+T
 
 Neste momento nos deparamos com a janela do terminal aberta pronta para receber os primeiros comandos.
 
 > engecorp@engecorp:~$ 

 
 
 
 Completar uma palavra
 preciona o tab
insper
# reebrepsni 

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







