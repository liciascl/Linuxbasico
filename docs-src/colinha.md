# Colinha com os comandos da Atividade Complementar

Listamos aqui os comandos mais utilizados pra você consultar 


![referencia](https://github.com/liciascl/Linuxbasico/tree/master/docs/img/atalhos.png){width=200}




Abra um terminal novo, usando o atalho <kbd>Ctrl</kbd> + <kbd>Alt</kbd> + <kbd>T</kbd>



Abra uma aba no terminal que ja existe, <kbd>Ctrl</kbd> + <kbd>Shift </kbd> + <kbd>T</kbd>


## Entrar numa pasta

```bash
cd nome_da_pasta_mãe

ou

cd nome_da_pasta_mãe/nome_da_pasta_filha/nome_da_pasta_infinitamente

```

## Ir até o diretório Home


```bash
cd ~

ou

cd /home/

```

## Visualizar o caminho de onde você está

```bash
pwd

```

## Voltar uma pasta

```bash
cd ..

```

## Voltar duas pastas

```bash
cd ../..

```

## Listar o conteúdo do diretório


```bash
ls

```

## Saber o conteúdo do diretório de forma mais detalhada


```bash
ls -a

ou

ls -la

ou ainda

ll

```

## Remover arquivos permanetemente

```bash
rm -rf

```


## Mover o arquivo de diretório:


```bash
mv ~/local_do_arquivo/nome.py ~/novo_local/nome.py

```


## Apenas renomear o arquivo :


```bash
mv ~/local_do_arquivo/nome.py ~/local_do_arquivo/nome_novo.py

```

## Renomear o arquivo ou mover de diretório:


```bash
mv ~/local_do_arquivo/nome.py ~/novo_local/nome_novo.py

```

## Criar ou abrir arquivos com o seu editor de texto favorito

```bash

nano mais_um_teste.py
code esta_acabando_a_criatividade.py
gedit socorro.py


```

## Recarregar o  `.bashrc `

```bash

source ~/.bashrc

```

## Instalar pacotes disponíveis via apt


```bash
sudo apt-get install nome_do_pacote

```


## Desinstalar pacotes disponíveis via apt

```bash
sudo apt-get remove nome_do_pacote

```

## Informações dos dispositivos conectados na USB 

```bash
lsusb

```
Informações dos dispositivos conectados na PCI

```bash
lspci

```

## Destravar um programa 

Use "xkill" e clique no programa travado com o mouse.


```bash
xkill

```

## Alterar as permissões dos arquivos e diretórios


```bash
chmod a+x roda_tartaruga.py

```
*este comando libera a permissão para o arquivo se tornar executável, para outras opções de permissão, consulte o [guialinux](https://guialinux.uniriotec.br/chmod/)*


