# Atividade Complementar - Introdução ao Linux

## Infraestrutura

A infra necessária para este curso já está instalada no SSD disponibilizada para os alunos do terceiro semestre de engenharia de computação do Insper. 

<img src="/img/ssd.png" width="400" height="400">

# Parte 1

## Linux 
<img src="/img/ilovelinux.png" width="500" height="250">

O desenvolvimento do Linux é um dos exemplos mais proeminentes de colaboração de software livre e de código aberto. O código fonte pode ser usado, modificado e distribuído, com fins comercias ou não, por toda a comunidade, respeitando as licenças.

Normalmente, o Linux é utilizado como plataforma de desenvolvimento em sistemas embarcados

![Kernel logo](/img/Kernel_basic.png)
[Fonte](https://manjarobrasil.wordpress.com/2015/08/02/o-que-e-kernel/)

A distribuição linux ou Sistema Operacional que vamos usar será o Ubuntu. Existem diversas distribuições mas não será o nosso foco.

>Informações técnicas são encontradas de forma vasta na internet, abaixo deixo apenas alguns links, não se restrinja apenas a eles:
>[link1](https://www.linuxfoundation.org/)
>[link2](https://pt.wikipedia.org/wiki/Distribui%C3%A7%C3%A3o_Linux#/media/Ficheiro:Linux_Distribution_Timeline.svg)
>[link3](https://boilingsteam.com/arch-manjaro-still-going-strong/)
>

# Conhecendo e utilizando o Terminal 

O Terminal do Linux pode causar espanto, mas é apenas uma ferramenta que facilita a manipulação do sistema, interpretando os comandos do usuário, fazendo a ponte com o hardware

## Abrindo o terminal

A forma mais facil de abrir o terminal é atraves do atalho:

 > Crtl+Alt+T
 
Neste momento nos deparamos com a janela do terminal aberta no ambiente do usuário (home ou ~) pronta para receber os primeiros comandos.
![ssd](/img/terminal.png)

## Configurando o Git

Antes começar a falar dos comandos do terminal, vamos configurar o nosso Git, para isso copie os comandos abaixo e cole no terminal:

```bash
git config --global user.name "Seu Nome"
git config --global user.email "seunome@email.com"
```
> Se você está tentou usar Crtr+C no texto e Crtr+V no terminal, talvez não tenha dado muito certo. 
> Para copiar e colar no ## terminal ##  use:
> Ctrl+Shift+C (Copiar) e Ctrl+Shift+V (Colar). 
> Sabendo disso, faça atualização do git copiando e colando o comando no terminal.

Para verificar se foi atualizado com sucesso digite:

```bash
git config user.name
git config user.email
```
# Navegando entre diretorios e arquivos

De forma bem simplificada, podemos dizer que o sistema Linux possui 2 elementos principais: pastas e arquivos. Os arquivos armazenam dados (txt, py...) e as pastas tambem chamadas de diretórios, armazenam e organizam os arquivos. 
Sabendo disso é importante saber navegar entre os diretórios para encontrar os nossos arquivos.


![pasta logo](/img/FilesAndFolders.png)
[Fonte](https://commons.wikimedia.org/wiki/File:FilesAndFolders.png)


## Comando "cd"

O comando **cd** é um dos comandos mais utilizados no terminal do Linux isso porque ele permite que acessemos um diretório especifico. Vamos acessar a nossa do repositorio de elementos. 


```bash
cd Z01.1
```
Vamos visualizar toda as estrutaras de arvore desta pasta. Vamos preciar instalar um modulo chamado tree, digite o comando abaixo no terminal: 

```bash
sudo apt install tree
```
Agora digite o comando:
```bash
tree -d -L 4
```
```bash
/home/borg/Z01.1
├── Aulas
│   └── 01-Organizacao-De-Computadores
├── Exercicios
└── Projetos
    ├── A-AmbienteDesenvolvimento
    └── B-LogicaCombinacional
        ├── Quartus
        ├── src
        │   └── rtl
        └── tests
            └── tst

11 directories
```
> os paramentros -d -L 2 indica que que queremos listar (-L )até o quarto (4) nível na hierarquia de pastas, apenas as pastas (-d), para listar tudo digite apenas tree.

Na pasta Z01.1 -> Projetos -> B-LogicaCombinacional -> src -> rtl estão os arquivos .hdl da ultima aula, vamos dar uma olhada neles. 

```bash
cd Projetos
cd B-LogicaCombinacional
cd src
cd rtl
```
ou par ir direto para este diretorio digite:

```bash
cd Projetos/B-LogicaCombinacional/src/rtl
```
> Dica:. Se estiver com preguiça de digitar o caminho completo, digite apenas o começo do comando e use a tecla TAB para dar auto-completar.

Para voltar, subir um nivel, e acessar o diretório anterior podemos digitar:

```bash
cd ..
```
## Comando "pwd"

Podemos verificar o diretório que estamos digitanto:

```bash
pwd
```

## Comando "ls"

O comando **ls** é utilizado par exibir (listar) o conteudo de um diretório. 
```bash
ls
```
## home
Para acessar a home do nosso usuario podemos fazer isso "voltando" as pastas repetindo o comando acima, ou simplismente digitando o comando: 

```bash
cd ~
```
> Toda vez em que abrimos um novo terminal, ele é inicializado na home do usuário. 

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

# Movendo e Copiando diretórios e arquivos

## Comando "cp"

Para copiar arquivos e diretorios, o famoso CTRL+C + CTRL+V, basta  digitar:

```bash
> meuarquivo.py 
cp -R meuarquivo.py /home/user/Linuxbasico/pasta1/
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

# Super Usuário

## Comando "sudo"
Por questões de seguraça, o Linux trabalha com permissões de usuários e para determinados arquivos ou comandos apenas o usuario administrador (root) pode executar. A titulo de curiosidade, "sudo" significa **S**uper **U**ser **DO**. Quando executar comandos com sudo, será necessário informar a senha.




# Atividade 1 - Criando arquivos

## Comando "touch" e ">"

Podemos criar arquivos de algumas formas, os mais clássicos são:

1. Usando o comando **touch**:
```bash

touch teste.py

```

2. Usando o comando **>**:

```bash

> outro_teste.py

```

3. Usando editor de texto, vamos falar deles jaja...

```bash

nano mais_um_teste.py
code esta_acabando_a_criatividade.py
gedit socorro.py

```

# Editando arquivos

Existem muitas editores de texto, cada um com seus pros e contras, com o tempo cada desenvolvedor acaba se apegando a um editor especifico, mas podemos dizer que existem 2 tipos de editoes de texto.
Modo console, que abre no proprio terminal e o com interface gráfica. 

## Editor nano 
O nano é um editor do modo console, ou seja, abre no proprio terminal. Vamos ver alguns comandos basicos, mas na parte inferior do editor são exibidos comandos que o nano entende.  

![nano logo](/img/main-nano-window.png)

### Abrir
Digite no terminal **nano** e o nome do arquivo com a extensão, caso não exista um arquivo com esse nome um novo arquivo será criado.

```bash
nano nano.py
nano nano.txt
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
gedit roda_tartaruga.py
gedit roda_tartaruga.txt
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
code roda_tartaruga.py
```
### Localizar palavra

Para fazer uma busca no texto pressione Ctrl+F, digite a palavra e tecle Enter.

### Salvar e Sair

Para salvar e sair, pressione Ctrl+S ou clique em salvar para salvar e para sair Alt+F4.


# Visualização de arquivos e pastas ocultos

O comando "ls" sozinho não exibe arquivos ocultos, que são arquivos e pastas que começam com ".". Durante as aulas de robotica teremos que editar um arquivo oculto chamado "**.bashrc**", no momento precisamos apenas saber que este arquivo se encontra na home do usuario `~` e que após editado precisamos executar o `source ~/.bashrc` ou `feche o terminal e abra um novo` para recarregar as atualizações do arquivo. digite:

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
```bash
cd ~
code .bashrc
source .bashrc
```

O .bashrc carrega todas as variáveis globais do seu ambiente Linux, esse arquivo é muito importante, e muito utilizado. 

Para subir a tartaruga do ROS, precisamos configurar o nosso *.barshrc*, primeiro, abra o arquivo, usando o comando abaixo;


```bash
code ~/.bashrc
```

Depois, procure essas linhas, e comente, conforme imagem abaixo;

![bashrc](/img/bashrc.png)


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
sudo apt-get install geogebra
```
> instalação do geogebra. Para iniciar, digite geogebra no terminal. 

### Remover pacotes

```bash
sudo apt-get remove geogebra
```

# informaçes do sistema

Comandos menos utilizados no dia a dia mas que sempre aparecem. 

## Informações dos dispositivos conectados na USB e na PCI

```bash
lsusb
lspci
```
## Mensagens do inicialização e do sistema

```bash
ps 
dmesg
htop
tree -L 3
cat /etc/lsb-release 
uname -a
```
## Como destravar o sistema

Para destravar uma tela, use "xkill" e clique na tela com o mouse.
```bash
xkill
```



# Modificando as permissões dos arquivos e diretórios

## Comando "chmod"
As permissões servem para determinar se um usuario ou grupo terá permissões para ler, gravar, executar. Existem diversas configurações possiveis e a que mais utilizamos dá a permissão de execução a um codigo qualquer, como um python, por exemplo;

```bash
chmod a+x roda_tartaruga.py
```
A concatenação de a+x significa que estamos permitindo para todos (a = all) usuarios e grupos que executem (x = execution) o roda_tartaruga.py


