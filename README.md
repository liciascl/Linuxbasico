# Guia Linux básico <img src="/img/linux.png" width="100" height="100">

Este não é um curso regular de Linux, neste curso queremos ensinar conceitos básicos do Linux como navegar pelo sistema de arquivos, etc... e mostrar alguns exemplos básicos, mas com foco nas matérias de Robótica Computacional e Elementos de Sistemas para auxilia-los com os primeiros passos. 

Afim de não ser algo chato e sem graça, vamos ao final desta aula 

## Infraestrutura

A infra necessária para este curso já está instalada no SSD disponibilizada para os alunos do terceiro semestre de engenharia de computação do Insper. 

<img src="/img/ssd.jpeg" width="400" height="400">

# Parte 1

## Linux 
<img src="/img/ilovelinux.png" width="500" height="250">

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

Antes começar a falar dos comandos do terminal, vamos configurar o nosso Git, para isso copie os comandos abaixo e cole no terminal:

```bash
git config --global user.name "Seu Nome"
git config --global user.email "seunome@email.com"
```
> Se você está tentou usar Crtr+C no texto e Crtr+V no terminal, talvez não tenha dado muito certo. 
> Para copiar e colar no ## terminal ##  use:
> Ctrl+Shift+C (Copiar) e Ctrl+Shift+V (Colar). 
> Sabendo disso, faça atualização do git copiano e colando o comando no terminal.

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
## home
Para acessar a home do nosso usuario podemos fazer isso "voltando" as pastas repitindo o comando acima, ou simplismente digitando o comando: 

```bash
cd ~
```
> Toda a vez que abrimos um novo terminal, ele é inicializado na home do usuário. 

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


# Atividade 1:

Agora que conhecemos alguns comandos temos base suficiente para fazer a uma correção na inicialização do SSD. Os alunos que tem os SSD com numeração `0xB__` ja perceberam que aparece uma msg de erro na inicialização do sistema. 

![boot SSD](/img/bootSSD.png)

Para corrigir, é necessário realizar a copia de uma pasta de uma pasta especifica para outro diretorio.

Vamos começar montando a partição do sistema. 

> Quando necessário lembre de uar SUDO

```bash
cd /mnt
mkdir disco
mount /dev/sd`X`3 /mnt/disco
```
> o `X` é o nome da partição, isso vai mudar de computador para computador (alguns pc tem 2 hds internos), normalmente é a `b` ou `c`.
> O mount basicamente monta a partição sdb3 na pasta disco, fazemos isso para poder acessar este diretório como uma pasta normal. 

Verifique se o conteudo da pasta esta igual o abaixo: 

```bash
├── backup
├── boot
│   ├── grub
│   └── memtest
├── EFI
│   └── BOOT
└── restore
```

Se sim, vamos em frente! Caso contrario, execute o comando abaixo e teste a outra partição e verifique se esta correta a estruta de pasta criada: 
```bash
cd /mnt
umount /mnt/disco 
```
O proximo passo é copiar a pasta x86_64-efi que esta em /boot/grub
```bash
/boot
├── efi
└── grub
    ├── fonts
    ├── locale
    └── x86_64-efi
```

Para a /mnt/disco/boot/grub: o resultado deve ser igual o abaixo.

```bash
/mnt 
└── disco
    ├── boot
    │   ├── grub
    │   │   ├── fonts
    │   │   ├── i386-pc
    │   │   ├── locale
    │   │   └── x86_64-efi
    │   └── memtest
    └── EFI
        └── BOOT
```
Se deu tudo certo, parabens!! Desmonte a partição montada:
```bash
cd /mnt
umount /mnt/disco
```
E exclua a pasta disco. A pasta mnt deve ficar vazia.

# Parte 2

# Criando arquivos

## Comando "touch" e ">"

Podemos criar arquivos de algumas formas, os mais clássicos são:

1. Usando o comando **touch**:
```bash
touch meuarquivo.py
```

2. Usando o comando **>**:
```bash
> meuarquivo.py
```

3. Usando editor de texto, vamos falar deles jaja...
```bash
nano meuarquivo.py
code meuarquivo.py
gedit meuarquivo.py
```
> no caso 3, usando um editor, um arquivo meuarquivo.py será criado caso não exista um arquivo com este nome, neste diretório.

# Editando arquivos

Existem muitas editores de texto, cada um com seus pros e contras, com o tempo cada desenvolvedor acaba se apegando a um editor especifico, mas podemos dizer que existem 2 tipos de editoes de texto.
Modo console, que abre no proprio terminal e o com interface gráfica. 

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

# Atividade 2

Vamos realizar algumas atividades utilizando o simulador Gazebo com o Robô Turtlebot3: 

## Atividade 2.1 

Para utilizar o Simulador Gazebo precisamos nos certificar de que as configurações para o simulador foram setadas. 

Passo 1:
    Edite o arquivo `.bashrc`;
    Comente com `#` as linhas;
        export ROS_MASTER_URI="http://"$IPBerry":11311" 
        export ROS_IP=`hostname -I`  
        export TURTLEBOT3_MODEL=burger
    Descomente a linha:
        export TURTLEBOT3_MODEL=waffle_pi     
   
Passo 2:
    Execute os comandos abaixo, abra novos terminais se necessário:
        roslaunch turtlebot3_gazebo turtlebot3_world.launch
        roslaunch turtlebot3_gazebo turtlebot3_gazebo_rviz.launch
        roslaunch turtlebot3_teleop turtlebot3_teleop_key.launch 

Se tudo deu certo, você já consegue teleoperar o turtlebot pelo teclado. 

## Atividade 2.2

Configure o .bashrc e rode o simulador gazebo. 
Rode o programa python de exemplo le_scan.py 

> DICA: use o comando 'locate' para descobrir onde este este arquivo. Use o google se necessário. 

## Atividade 2.3

adicione no arquivo .bashrc o alias de parada do robo. 

> #Pararobo
> alias pararobo="rostopic pub -1 /cmd_vel geometry_msgs/Twist -- '[0.0, 0.0, 0.0]' '[0.0, 0.0, 0.0]'"

Toda a vez que for executado o comando paraboro, um comando de parada será publicado no robo.

Execute o comando e verifique atraves do simulador se esta funcionando.


# Modificando as permissões dos arquivos e diretórios

## Comando "chmod"
As permissões servem para determinar se um usuario ou grupo terá permissões para ler, gravar, executar. Existem diversas configurações possiveis e não falar de todas elas. Precisamos permitir a execução de um codigo python logo, temos que mudar as permissões do arquivo.

```bash
chmod a+x meuprograma.py
```
A concatenação de a+x significa que estamos permitindo para todos (a = all) usuarios e grupos que executem (x = execution) o meuprograma.py


# Atividade 3

Vamos continuar trabalhando com o simulador Gazebo e o Robo, mas ao inves de executar exemplos, agora vamos criar nossa propria pasta de projetos python para o nosso robo. 

Passo 1: 
    Acesse o diretorio catkin_ws -> src

Passo 2: Execute o comando abaixo:
```bash
catkin_create_pkg meu_projeto std_msgs sensor_msgs geometry_msgs rospy roscpp
```

este comando cria uma pasta chamada meu_projeto, que ja está configurada para o ambiente de programação do robo (ROS).

o resultado esperado é: 
```bash
Created file meu_projeto/CMakeLists.txt
Created file meu_projeto/package.xml
Created folder meu_projeto/include/meu_projeto
Created folder meu_projeto/src
Successfully created files in /home/borg/catkin_ws/src/meu_projeto. Please adjust the values in package.xml.
```

Passo 3:
Acesse a diretorio criada (meu_projeto).

Passo 4: Crie uma pasta chamada scripts.
> nesta pasta scripts estarão todos os programas python que vamos criar para o robo.

Passo 5: Crie um arquivo python chamado roda.py, com o script abaixo:

```python
#! /usr/bin/env python
# -*- coding:utf-8 -*-

import rospy
from geometry_msgs.msg import Twist, Vector3

v = 10  # Velocidade linear
w = 5  # Velocidade angular

if __name__ == "__main__":
    rospy.init_node("roda_exemplo")
    pub = rospy.Publisher("cmd_vel", Twist, queue_size=3)

    try:
        while not rospy.is_shutdown():
            vel = Twist(Vector3(v,0,0), Vector3(0,0,w))
            pub.publish(vel)
            rospy.sleep(2.0)
    except rospy.ROSInterruptException:
        print("Ocorreu uma exceção com o rospy")
```

Passo 6: Aplique a permissão de execução para todos os usuarios neste arquivo. 

Passo 7: Retorne para a pasta catkin_ws e execute o comando:

```bash
catkin_make
```
Se der tudo certo, a compilação irá chegar até 100%. 


Passo 8: Vamos testar nosso codigo. Como criamos um projeto ROS, vamos executar de outra maneira agora. 

Faça as configurações do bashrc e abra o simulador e então execute o comando abaixo:

```bash
rosrun meu_projeto rodateste.py 
```

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

Comandos menos utilizados no dia dia mas que sempre aparecem. 

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
Durante as aulas de Elementos pode ocorrer alguma falha no gravador. Para corrigir desconecte e conecte o cabo usb se não funcionar execute os comandos:


```bash
sudo killall -9 jtagd
sudo killall -9 jtagd
jtagconfig
```
