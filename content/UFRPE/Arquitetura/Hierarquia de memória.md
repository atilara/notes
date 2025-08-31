Temos as seguintes relações quando se trata de memória:
- Tempo de acesso mais rápido, maior maior custo por bit
- Maior capacidade, menor custo por bit
- Maior capacidade, menor tempo de acesso

Programadores não querem se preocupar se há memória suficiente e se ela é rápida suficiente para execução de um programa.  Por isso surgiu a necessidade de criarmos uma *hierarquia de memória*, se memória rápida fosse barata, todas seguiriam essa mesma tecnologia.

Princípios da localidade de memória:

> [!IMPORTANT] Localidade temporal
> Posições de memória acessadas recentemente provavelmente serão acessadas novamente em breve
> *Exemplo*: instruções em um loop

> [!IMPORTANT] Localidade espacial
> Se uma posição de memória é acessada, provavelmente posições próximas serão acessadas em breve
> *Exemplo*: acesso sequencial a dados de um array

Para tirar vantagem dos tipos diferentes de memória:

- Disco armazena tudo, como instalação do sistema operacional e programas
- Ao executar um programa, os itens desse programa são copiados para memória *RAM*, que é menor mas tem velocidade maior que o disco
- Ao carregar instruções do programa, os dados são copiados para memória mais rápidas ainda, memória *cache* que fica localizada no CPU

Pirâmide de hierarquia de memória:

![[Pasted image 20240916204736.png]]

Memórias de níveis mais altos ficam mais próximas do CPU, os dados armazenados nos níveis mais altos sempre terão cópias armazenados nos níveis mais baixos. 

Durante o acesso a memória, podemos ter um *hit* ou *miss*.
- *hit*: dado acessado está presente no nível superior
- *miss*: dado acessado está ausente e deve ser copiado do nível mais baixo, sendo fornecidos pro nível superior. Causa uma penalidade pelo acesso a memória inferior

Características do sistema de memória

- Localização: interno (registrador), externo (disco)
- Capacidade: words, bytes
- Unidade de transferência: word, block
- Método de acesso: sequencial, direto, aleatório
- Desempenho: tempo de acesso e ciclo
- Tipo físico: semicondutor, magnético, óptico
- Características físicas: volátil/não-volátil, erasable/non-erasable
- Organização: módulos de memória 
