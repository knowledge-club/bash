## LS

Significa `listar`. Útil para ver quais arquivos existem em um path/diretório atual.

```sh
# Eu estou em '~', o comando abaixo lista os arquivos em meu diretório atual
ls
```

```sh
# lista os arquivos em um path específico
ls /Users
```

```sh
# Se você quer mostrar arquivos ocultos, use a flag -a
ls -a /
```

```sh
# útil para checar se um arquivo existe, se existir, retorna os arquivos encontrados, se não, retorna 'No cuch file or directory'
ls ~/Desktop/test.js
```

### Nota

Sempre que você escrever um path para um arquivo, você pode usar glob files. Glob files, é um jeito de definir caminho para arquivos escrevendo partes do nome, entre outros mais.

```sh
# lista apenas os arquivos em um path, que tenham uma extensão .js
ls ~/Desktop/projeto1/*.js
```

```sh
# o dobro **, é para listar recursivamente interno a pasta projeto1
ls ~/Desktop/projeto1/**/*.js
```