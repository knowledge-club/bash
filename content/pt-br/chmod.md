## CHMOD

Vem de `change modes`. É usado para mudar o controle de acesso de um arquivo ou pasta na ordem para permitir o dono, usuários, ou todos para `ler/escrever/exectuar` um arquivo.

Permissões em sistemas baseados em unix são baseados em bitcounts. Nós temos 3 bits, um para `read`, outro para `write` e um para `exec`, sendo `000` (ou `read write exec`), se nós setarmos `001`, pela soma dos bits teremos `1` (por que `0001=1`), se nós quisermos setar todas as permissões para um arquivo nós podemos simplesmente usar `111` (e sumando todos nós temos `7` porque a soma binária de `111` é `7`).

Numa outra parte nós temos que setar as permissões para os usuários. A ordem é `owner` `users in group` `not in group`, então nós conseguimos ter 3 conjuntos de bits `000 000 000` que significa `owner user guest`. Então nós podemos setar as permissões por juntar as somas dos bites como `654`, isto signficia: Owner pode ler-escrever (`110=6`), usuários podem ler e executar (`101=5`) e guests podem apenas ler (`100=4`).

```sh
# seta a permissão para owner puderem fazer qualquer coisa, usuários podem ler e executar, e guests apenas ler o arquivo "permissions.txt"
chmod 754 permissions.txt
```