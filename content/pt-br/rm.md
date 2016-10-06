## RM

Significar `remover`, é usado para deletar arquivos ou diretórios. <span color="red">**Mas cuidado, este comando não envia para lixeira**</span>, ele deleta o arquivo e não tem como voltar.

```sh
# remove o arquivo chamado index.html na pasta atual
rm index.html
```

```sh
# remove múltiplos arquivos em um único comando
rm index.html style.css
```

```sh
# finalmente, para remover um diretório, você precisa usar as flags `r` e `f`, respectivamente, são abreviações para `recursive` e `force`
rm -rf app
```