Utilizamos o código-fonte para criar testes, diferente de caixa-preta, onde não sabemos como o sistema funciona, apenas o que ele faz.
### Cobertura de comando
É preciso analisar se todos os comandos possíveis dentro do objeto de teste são cobertos pelo teste. É necessário criar mais casos de teste caso isso não aconteça.

Mede o percentual de comandos cobertos pelos testes:

$$
\frac{\text{número de comandos cobertos}}{\text{número total de comandos}} \times 100\%
$$
### Cobertura de decisão
Um teste para *verdadeiro* e outro para *falso*, comandos que possuem decisões:
- `if`
- `while`
- `do-while`
- `repeat-until`
- `for`
- `case`
$$
\frac{\text{número de decisões V e F cobertas}}{\text{número total de decisões V e F}} \times 100\%
$$
É difícil atingir 100% de cobertura em sistemas grandes, 75% a 85% é um valor economicamente viável em sistemas grandes.

### Cobertura de condição
Entra nos detalhes de uma decisão:

![[Pasted image 20231204171828.png]]

Os casos de teste devem tornar cada condição verdadeira ou falsa.
$$
\frac{\text{número de decisões V e F cobertas}}{\text{número total de decisões V e F}} \times 100\%
$$
### Cobertura de caminho
É montado um diagrama dos caminhos que o código pode seguir durante execução, os cados de teste devem cobrir todos os caminhos possíveis:

![[Pasted image 20231204173212.png]]