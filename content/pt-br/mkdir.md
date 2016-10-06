## MKDIR

Comando para fazer um diretório, abreviação de `make a directory`.

```sh
# cria um diretório chamado 'nomeDaPata' na pasta atual
mkdir nomeDaPasta
```

```sh
# crie dois ou mais diretórios, apenas dê espaço entre os argumentos.
# neste caso, nós estamos criando dois diretórios, 'name1' e 'name2', ambos na pasta atual.
mkdir name1 name2
```

```sh
# cria um diretório chamado 'test' no path '/Users/darlanmendonca/Desktop'
mkdir /Users/darlanmendonca/Desktop/test
```

```sh
# -p é uma flag(option), para criar diretórios (no nosso caso, pasta 'parent'), caso estes não existam
mkdir -p /Users/darlanmendonca/Desktop/test/parent/children
```

```sh
# se você precisa de espaços no nome da pasta, use "\ "(barra invertida + espaço)
# criando uma pasta chamada "nome com espaços"
mkdir nome\ com\ espaços
```
