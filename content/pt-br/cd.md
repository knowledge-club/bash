## CD

Vai para um diretório, relativo ou absoluto. É uma abreviação de `change directory`, em português `mudar diretório`

```sh
# '/'' é a raiz do HD em sistemas baseados em Unix (Linux, MacOS, ...). Similar a 'c:' se você estiver no Windows.
cd /
```

Outro exemplo

```sh
# '~'' é um alias para a pasta de usuário em sistemas baseados em Unix O path completo seria algo como '/Users/darlanmendonca'
cd ~
```

```sh
# path absoluto
cd /Users/darlanmendonca
```

```sh
# path absoluto, Eu estou em /Users/darlanmendonca, e nós queremos entrar no diretório projetos, que está dentro do diretório atual.
cd projects
```

### Nota

with space after command, you can pass multiples arguments to command. In case of ***cd*** command, you only need pass one arguments, but other commands maybe work with multiples. In cases of multiples arguments, just give a space between values.