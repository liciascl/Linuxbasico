# Guia Linux básico

Este não é um curso regular de Linux, neste curso queremos ensinar conceitos básicos do Linux como navegar pelo sistema de arquivos, etc... e mostrar alguns exemplos básicos, mas com foco nas matérias de Robótica Computacional e Elementos de Sistemas para auxilia-los com os primeiros passos. 

## Infraestrutura

A infra necessária para este curso já está instalada no SSD disponibilizada para os alunos do terceiro semestre de engenharia de computação. 

<img src="/img/ssd.jpeg" width="400" height="400">

## Linux 
<img src="/img/ilovelinux.png" width="700" height="250">

Basicamente, o Linux nada mais é que um Kernel, ou seja, é o software responsavel por conectar o hardware (computador, dispositivo embarcado) com o software (Sistema Operacional). 

Linux já é utilizado amplamente por empresas de tecnologia tanto para infraestrura como para desenvolvimento de sistemas e nos ultimos vem crescendo tambem os usuarios domesticos. Durante a gradução e vida profissional na area de computação, vamos sempre nos deparar com um terminal do linux. 

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
 
 Neste momento nos deparamos com a janela do terminal aberta na home do usuario pronta para receber os primeiros comandos.

![ssd](/img/terminal.png)

## Configurando o Git

Antes começar a falar dos comandos do terminal, vamos configurar o nosso Git, para isso digite no terminal os comandos abaixo:

```bash
git config --global user.name "Seu Nome"
git config --global user.email "seunome@email.com"
```
Para verificar se foi atualizado com sucesso digite:

```bash
git config user.name
git config user.email
```
Agora, vamos aproveitar para clonar o repositório desta aula. 

```bash
git clone https://github.com/arnaldojr/Linuxbasico.git
```

# Navegando entre diretorios e arquivos

De forma bem simplificada, podemos dizer que o sistema Linux possui 2 elementos principais: pastas e arquivos. Os arquivos armazenam dados (txt, py...) e as pastas tambem chamadas de diretórios, armazenam e organizam os arquivos. 
Sabendo disso é importante saber navegar entre os diretórios para encontrar os nossos arquivos.


![pasta logo](/img/FilesAndFolders.png)
[Fonte](https://commons.wikimedia.org/wiki/File:FilesAndFolders.png)


## Comando "cd"

O comando **cd** é um dos comandos mais utilizados no terminal do Linux isso porque ele permite que acessemos um diretório especifico. Vamos acessar uma pasta do repositório que acabamos de clonar. 

```bash
cd Linuxbasico/pasta1/subpasta2/subpasta3/ 
```
Este comando nos leva direto para o diretório chamado **subpasta3** passando pelos diretorios: Linuxbasico, pasta1 e subpasta2. Mas podemos navegar de diretorio em diretório, um por um. 

```bash
cd Linuxbasico
cd pasta1
cd subpasta2
cd subpasta3 
```

Para voltar subir um nivel e acessar o diretório chamado **subpasta2** podemos digitar:

```bash
cd ..
```
Para acessar a home do nosso usuario podemos fazer isso "voltando" as pastas repitindo o comando acima, ou simplismente digitando o comando: 

```bash
cd ~
```
## Comanod "pwd"

Podemos verificar o diretório que estamos digitanto:

```bash
pwd
```

## Comando "ls"

O comando **ls** é utilizado par exibir (listar) o conteudo de um diretório. 
```bash
ls
```

## Visualização de arquivos e pastas ocultos

O comando "ls" sozinho não exibe arquivos ocultos, que são arquivos e pastas que começam com ".". Durante as aulas de robotica teremos que editar um arquivo oculto chamado "**.bashrc**", no momento precisamos apenas saber que este arquivo se encontra na home do usuario. digite:

```bash
cd ~
ls -a
```
ou para listar informações mais detalhadas:

```bash
ls -la
```
ou simplismente:

```bash
ll
```

# Criando diretórios

## Comando "mkdir"

Vamos criar um diretório chamado **minhapasta** dentro do diretório **pasta1**. Podemos fazer essa tarefa de algumas formas:

1. Navegamos até o diretório pasta1 e criamos o minhapasta:
```bash
cd Linuxbasico/pasta1
mkdir minhapasta
```
2. Criamos a pasta passando o caminho completo:

```bash
mkdir ~/Linuxbasico/pasta1/minhapasta 
```
> Dica:. Se estiver com preguiça de digitar o caminho completo, use a tecla TAB para dar auto-completar.

# Criando arquivos

## Comando "touch" e ">"

Vamos criar um arquivo python chamado **meuarquivo.py** dentro da pasta que criamos. Podemos criar o arquivo acessando o diretório "minhapasta" previamente ou passando o caminho completo, a escolha é sua.

1. Usando o comando **touch**:
```bash
touch meuarquivo.py
```

2. Usando o comando **>**:
```bash
> meuarquivo.py
```
# Movendo e Copiando diretórios e arquivos

## Comando "cp"

Para copiar arquivos e diretorios, o famoso CTRL+C + CTRL+V, basta  digitar:

```bash
> meuarquivo.py 
cp meuarquivo.py /home/user/Linuxbasico/pasta1/
```
No exemplo acima foi criado uma copia do arquivo "nome1.py" dentro do diretório pasta1. 

## Comando "mv"

Para mover arquivos e diretorios, o famoso CTRL+x + CTRL+V, basta  digitar:

```bash
> meuarquivo.py 
mv meuarquivo.py /home/user/Linuxbasico/pasta1/
```
No exemplo acima o arquivo "nome1.py" foi movido para dentro do diretório pasta1 (recortado e colado).

## Renomeando diretórios e arquivos

O comando **mv** tambem serve para renomear arquivos e diretorios:

```bash
> nome1.py
mv nome1.py nome2.py
```
> Atenção!! Cuidado para não sobrescrever arquivos e pastas atuais na hora de executar estes comandos.

# Excluindo diretórios e arquivos

## Comando "rm"

Para excluir arquivos e diretórios, o famoso Shift+Del, basta digitar:

```bash
rm -rf nome1.py
rm -rf minhapasta
```
> Atenção!! Cuidado!!!! Arquivos e pastas são apagados permanentemente, não vão para lixeira. No caso de diretórios, apaga o diretório e tudo que está dentro dele.

# Editando arquivos

Existem muitas editores de texto, cada um com seus pros e contras, com o tempo cada desenvolvedor acaba se apegando a um editor especifico, mas podemos dizer que existem 2 tipos de editoes de texto.
Modo console, que abre no proprio terminal e o com interface grafica. 

## Editor nano 
O nano é um editor do modo console, ou seja, abre no proprio terminal. Vamos ver alguns comandos basicos, mas na parte inferior do editor são exibidos comandos que o nano entende.  

![nano logo](/img/main-nano-window.png)

### Abrir
Digite no terminal **nano** e o nome do arquivo com a extensão, caso não exista um arquivo com esse nome um novo arquivo será criado.

```bash
nano novoarquivo.py
nano novoarquivo.txt
```

### Localizar palavra
Para fazer uma busca no texto pressione Ctrl+W, digite a palavra e tecle Enter.

### Salvar e Sair

Para salvar e sair, precione Ctrl+S para salvar e para sair Ctrl+X.
Para sair sem salvar alteraçes, Ctrl+X e "n".

## Editor gedit
Muito parecido com o famoso bloco de notas do Windows.

![nano logo](/img/gedit3-screenshot.png)

### Abrir
Digite no terminal **gedit** e o nome do arquivo com a extensão, caso não exista um arquivo com esse nome um novo arquivo será criado.

```bash
gedit novoarquivo.py
gedit novoarquivo.txt
```
### Localizar palavra

Para fazer uma busca no texto pressione Ctrl+F, digite a palavra e tecle Enter.

### Salvar e Sair

Para salvar e sair, pressione Ctrl+S ou clique em salvar para salvar e para sair Alt+F4.

## Editor vscode

O editor vscode é uma ferramenta que possui mais recursos que auxiliam no desenvimento de codigo.

![vscode logo](/img/vscode-ui-in-container.png)

### Abrir

Digite no terminal **code** e o nome do arquivo com a extensão, caso não exista um arquivo com esse nome um novo arquivo será criado.

```bash
code novoarquivo.py
code novoarquivo.txt
```
### Localizar palavra

Para fazer uma busca no texto pressione Ctrl+F, digite a palavra e tecle Enter.

### Salvar e Sair

Para salvar e sair, pressione Ctrl+S ou clique em salvar para salvar e para sair Alt+F4.


# Modificando as permissões dos arquivos e diretórios

As permissões servem para determinar se um usuario ou grupo terá permissões para ler, gravar, executar. 

Para permitir a execução de um codigo python temos que mudar as permissões do arquivo.

```bash
chmod a+x meuprograma.py
```
# Super Usuário

## Comando "sudo"
Por questões de seguraça, o Linux trabalha com permissões de usuários e para determinados arquivos ou comandos apenas o usuario administrador (root) pode executar. A titulo de curiosidade, "sudo" significa **S**uper **U**ser **DO**. Quando executar comandos com sudo, será necessário informar a senha.

# Atualizações de Sistema e instalação de pacotes 

## Comando "apt" ou "apt-get"

### Atualizar a "lista de pacotes"
```bash
sudo apt-get update 
```
### Atualiza pacotes "já instalados"
```bash
sudo apt-get upgrade 
```
### Instalar pacotes

```bash
sudo apt-get install bastet
```
> instalação do jogo bastet. Para jogar, digite bastet no terminal. 

### Remover pacotes

```bash
sudo apt-get remove bastet
```
# Mostra os formatos básicos de arquivos compactados e como lidar com eles no Linux.
- tar - Agrupando arquivos
- gzip, bzip2 - Compactando arquivos
- zip, rar - Outros formatos de arquivos compactados Comandos de
Tratamento de Texto


# informaçes do sistema
ps 
cat /proc/cpuinfo - Informações sobre o processador
cat /etc/lsb-release 
- uname -a ou -r - Informações de versão do kernel, arquitetura e outros
  - lspci - Mostra informações sobre dispositivos PCI
- lsusb - Mostra informações sobre dispositivos USB
dmesg -  Mensagens de inicialização
man - Ajuda sobre algum comando, assunto ou arquivo de configuração

source .bashrc
export
grep

travou a tela 
xkill - mata a tela
kill, killall

