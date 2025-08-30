Memória principal sempre vai ter capacidade de endereçamento que as Cache. O mapeamento é uma função que mapeia blocos de memória em blocos de memória cache.

### Direto
Um bloco na memória só pode ser armazenado em uma linha de cache.

Forma mais simples de implementar:

$$\text{número da linha da cache} = \text{endereço do bloco na memória} \mod \text{quantidade de linhas da cache}$$
`Tag`: bits de alta ordem que indicam  o endereço do bloco de memória
`valid`: indica se o dado armazenado é válido ou não

Exemplo:

![[Pasted image 20240929193606.png]]

`Miss`: não há nada armazenado na cache
Endereço em binário do item a ser buscado na memória é `10110`

Nossa cache tem `3` bits de endereçamento, tendo `8` linhas
O `mod` são os bits de baixa ordem, portanto `110`, endereço na cache onde o dado é inserido
`Tag` é igual a `10`, sendo os bits de alta ordem que complementam o endereço onde o dado está armazenado fora da cache
`Data` armazena o valor vindo da memória
### Totalmente associativo
Um dado da memória principal pode ser mapeado em qualquer linha da cache. Todas as entradas devem ser pesquisadas de uma vez só, bastante caro.
### Associativo em conjunto
Cada bloco da memória principal pode ser mapeado para um conjunto determinado (sets) de linhas de cache. Apenas pesquisa nas possíveis posições onde a variável pode ser armazenada. Mais barato que o totalmente associativo.

