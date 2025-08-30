## Definição

Nível de hierarquia de memória mais próxima do CPU
* Pouca memória mas muito rápida
* Está entre a memória principal e CPU
Itens utilizados como base para construção de uma memória Cache:
- Enderaçamento: qual tipo de endereço é utilizado para mapear os dados que estão armazenados na cache
- Tamanho da cache: afeta quantidade informação mapeada por vez
	-  Quanto maior, mais caro
	- Mais cache, mais rápido (limite na verificação da cache, mapeamento)
- Função de mapeamento: calcular qual endereço da cache é usado pra armazenar um dado copiado da memória
- Algoritmo de substituição: a cache é pequena, isso é importante para definir quais dados são substituídos quando a cache encher
- Política de escrita: define quando o valor da memória cache é atualizado na memória principal
- Tamanho da linha: linhas de cache ou bloco de dados
- Quantidade de caches: caches podem ser multiníveis (*Level1, L2, L3*) ou não 
## Endereçamento

### Memória virtual
- Utilizado pra que a memória passe a ser tratada de forma lógica ao invés de física
- Memory Management Unit: hardware utilizado para converter endereços virtuais em físicos durante leitura e escrita na memória principal
A cache pode ser construída utilizando endereço virtual ou físico

## Mapeamento
#### Mapeamento direto
Local onde o bloco é armazenado na cache é determinado pelo endereço de onde vem na memória principal
$$
i = endereçoDoBloco \bmod qtdLinhasCache
$$
Sendo: 
- `i` = número da linha da cache
- Número de blocos da memória principal e cache sempre são potências de 2
- Para calcular módulo, basta olhar bits de endereço de ordem baixa

##### *Tag*
- Verifica qual bloco está armazenado em uma linha de cache
- Utiliza os bits de alta ordem
- Uma linha de cache não pode ser dedicada a armazenar um único bloco por ser muito menor que a memória principal

##### Valid
- Verifica se há dados armazenado em uma linha de cache
- `valid = 1`, dado presente
- `valid = 0`, dado não presente

###### Exemplo:

![[Pasted image 20240915232119.png]]

*[Resposta](https://www.inf.pucrs.br/~emoreno/undergraduate/SI/orgarq/class_files/Aula12.pdf)*
#### Associativo
Blocos da memória principal podem ser armazenados em qualquer linha de cache
#### Associativo por conjunto
Meio termo entre mapeamento direto e associativo. 
## Algoritmo de substituição
Define os blocos a serem substituídos quando um novo bloco é trazido para uma cache cheia. É implementado em hardware para evitar gargalo no CPU

> Não é necessário para mapeamento direto, pois só existe um possível endereço para armazenamento do dado

Pode ser:
- *Least recently used (LRU)*: substitui o bloco que ficou mais tempo sem ser referenciado
- *First-in-first-out (FIFO)*: substitui o que está há mais tempo na cache 
- *Least frequently used (LFU)*: substitui o bloco que sofreu menor número de referências