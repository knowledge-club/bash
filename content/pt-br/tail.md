## TAIL

Pega o conteúdo final de um arquivo e mostra ele na tela.

```sh
# Pega as últimas linhas do arquivo error.log
tail error.log
```

Também é possível ler um stream de dados em tempo real, exemplo, ler os logs do apache em tempo real, enquanto o server está executando.

```sh
tail -f apache/error.log
```