# Conceitos fundamentais
Software precisa de qualidade, que não possui uma única definição, pode envolver vários aspectos:
- Tecnologia
- Qualidade do processo de desenvolvimento
- Qualidade do time de desenvolvimento
- Custo, tempo e cronograma
Qualidade **não** pode ser injetada no **fim** do processo de desenvolvimento. Os testes eram deixados para o final no modelo em cascata onde os danos talvez não pudessem mais ser revertidos.
- **Quality assurance:** garantia de qualidade, proativo
- **Quality control:** controle de qualidade, reativo
# O que é teste de software?
### Objetivo
- Verificar cumprimento de requisitos
- Validar se o objeto do testo atende expectativas
- Reduzir risco de falhas não detectadas no desenvolvimento
- Criar confiança no objeto do testo, classificar falhas de alto/baixo impacto
- Previne defeitos
- Atende padrões que definem **parâmetros de qualidade**
- Encontra defeitos e falhas
Um tester não corrige bugs, reporta para o desenvolvedor e é essencial que os dois tenham comunicação fluida e se encontrem perto um do outro.

### Príncipios
- Testar não garante ausência de problemas
- Teste exaustivo é impossível: **cobertura <100%**
- Testar cedo salva tempo e dinheiro
- Distribuição de bugs dentro do sistema não é homogênea
- Ausência de erros não quer dizer que o sistema atende, perspectiva de **produto**

### Tipos de teste
- **Funcional:** funcionalidade do sistema
- **Estrutural:** estrutura interna do objeto de testes
	- O que isso quer dizer?
- **Não-funcional:** requisitos não funcionais
	- Confiabilidade
	- Usabilidade
	- Segurança
	- Desempenho
- **Orientado a mudanças:** executado após uma mudança no sistema
- **Confirmação:** teste executado com mesmos dados dentro do ambiente de teste deve ser sempre aceite
- **Regressão:** mudanças em partes que (não) tem relação direta com os testes feitos, que devem ser reexecutados para garantir o funcionamento

### Níveis de teste
- Unitário/De componente
	- Classes
	- Métodos
	- Estruturas de dados
	- Menor nível possível de um teste
- Integração: interação entre componentes do sistema
- Sistema: testa as aplicações do sistema no ambiente operacional , testado pelos testers
- Aceitação: testes manuais que testam aplicações do sistema, testado pelos **PO**s

### Metodologias para testagem
Continuous integration (**CI**)
Test driven development (**TDD**)
