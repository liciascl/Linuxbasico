# Colinha com os comandos da Atividade Complementar

Listamos aqui os comandos mais utilizados pra você consultar 





<img src="/img/atalhos.png" width="400" height="400">


Abra um terminal novo, usando o atalho Crtl + T
```
Crtl+Alt+T

```

Abra uma aba no terminal que ja existe, Crtl + Shift + T

```
Crtl+Alt+ Shift + T

```

Para entrar numa pasta

```
cd nome_da_pasta_mãe

ou

cd nome_da_pasta_mãe/nome_da_pasta_filha/nome_da_pasta_infinitamente

```

Se quiser ir até uma pasta que está no diretório Home


```
cd ~

ou

cd /home/

```

Se quiser saber aonde você está

```
pwd

```

Se quiser voltar uma pasta

```
cd ..

```

Se quiser voltar duas pastas

```
cd ../..

```

Para saber o conteúdo do diretório


```
ls

```

Para saber o conteúdo do diretório de forma mais detalhada


```
ls -a

ou

ls -la

ou ainda

ll

```

Para remover arquivos permanetemente

```
rm -rf

```


Para mover o arquivo de diretório:


```
mv ~/local_do_arquivo/nome.py ~/novo_local/nome.py

```


Para apenas renomear arquivo :


```
mv ~/local_do_arquivo/nome.py ~/local_do_arquivo/nome_novo.py

```

Para renomear e mover o arquivo de diretório:


```
mv ~/local_do_arquivo/nome.py ~/novo_local/nome_novo.py

```

Criando ou abrindo arquivos com o seu editor de texto favorito

```

nano mais_um_teste.py
code esta_acabando_a_criatividade.py
gedit socorro.py


```

Para recarregar o .bashrc

```

source ~/.bashrc

```

Para instalar pacotes disponíveis via apt


```
sudo apt-get install nome_do_pacote

```


Para desinstalar pacotes disponíveis via apt

```
sudo apt-get remove nome_do_pacote

```

Informações dos dispositivos conectados na USB 

```
lsusb

```
Informações dos dispositivos conectados na PCI

```
lspci

```

Para destravar uma tela, use "xkill" e clique na tela com o mouse.


```
xkill

```

Para alterar as permissões dos arquivos e diretórios


```
chmod a+x roda_tartaruga.py

```
*este comando libera a permissão para o arquivo se tornar executável, para outras opções de permissão, consulte o [guialinux](https://guialinux.uniriotec.br/chmod/)*
