### Sinais de controle

**Controle ALU**: informado numa tabela na questão, depende do campo funct 

**RegDst**:
- tipo i terão valor `00`, não registrador destino = `rt`
- tipo r, registrador destino = `rd`, seu valor será `01`

**Branch**: se o valor da próxima instrução vem de um deslocamento ou da instrução seguinte na memória (+4)
- instruções de desvio, como `beq`, `bne`, tem valor `01`
- todo o resto, `00`

**MemRead**: permite ler a memória de dados
* `lw`, única instrução que lê memória de dados para salvar em um registrador, `01`
* todo o resto, `00

**MemtoReg**: determina de onde vem o dado a ser escrito no banco de registradores
- se vem da ALU, em instruções tipo r, `00`
- se vem da memória, instrução `lw`, `01`

**ALUOp**: informado numa tabela da questão, depende da instrução em execução

**MemWrite**: permite escrever na memória de dados
* `sw`, única instrução que escreve na memória de dados para salvar o dado de um registrador na memória, `01`
* todo o resto, `00`

**ALUSrc**: se o segundo parâmetro da instrução é imediato ou de registrador
- `lw`, `sw`, tipo i, ALUSrc vem do extensor de bits, valor `01`
- tipo r, `beq`, ALUSrc vem do registrador, tendo valor `00`

**RegWrite**: determina se o banco de registradores pode ser escrito ou não
* `sw` + `beq` não escrevem no banco de registradores, `00`
- tipo i + tipo r + `lw` escrevem no banco de registradores, `01`

*Obs*: Instruções tipo r são instruções de lógica aritmética que operam diretamente nos registradores
tipo i: instruções imediatas com valores constantes, addi, subi
### Questões
##### `AND Rd, Rs, Rt`

- ALUControl: `0000`
- RegDst: `01`
- Branch: `00`
- MemRead: `00`
- MemtoReg: `00`
- ALUOp: `10`
- MemWrite: `00`
- ALUSrc: `00`
- RegWrite: `01`

##### `Beq Rd, Rs, adress`

- ALUControl: `0110`
- RegDst: `00` ou X
- Branch: `01`
- MemRead: `00`
- MemtoReg: `00` ou X
- ALUOp: `01`
- MemWrite: `00`
- ALUSrc: `00`
- RegWrite: `00`

##### `Addi Rs, Rt, i`

- ALUControl: `0001`
- RegDst: `00`
- Branch: `00`
- MemRead: `00`
- MemtoReg: `00`
- ALUOp: `10`
- MemWrite: `00`
- ALUSrc: `01`
- RegWrite: `01`

##### `Lw Rd, n(Rs)`

- ALUControl: `0010`
- RegDst: `00`
- Branch: `00`
- MemRead: `01`
- MemtoReg: `01`
- ALUOp: `00`
- MemWrite: `00`
- ALUSrc: `01`
- RegWrite: `01`