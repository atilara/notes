# Teste de componente
Um componente pode depender de outro, quando isso acontece precisamos simular o funcionamento desses componentes, utilizando:
- *Drivers* que simulam clientes do componente que será testado
- *Stubs/Mocks* que simulam componentes que a unidade de testes depende
##### Abordagens
- Top-down: mais stubs
- Bottom-up: mais drivers
##### Ferramentas
- JUnit: automatiza níveis dos testes
- Mockito: emula componentes java, cria stubs/mocks
- Emma: realiza análise da cobertura de testes
# Teste de integração
Stubs e drivers substituem os componentes já desenvolvidos e testados. Não utiliza GUI para realização dos testes.

##### Abordagens
- *Big bang:* espera todos os componentes ficarem prontos para testar integração
	- Arriscado
- *Incremental:* assim que um componente fica pronto, testa integração com outros
	- Caro

Geralmente se faz uso do incremental testando integrações mais perigosas, dessa forma pode-se equilibrar:
- Custo
- Tempo
- Qualidade

# Principais categorias técnicas
### Estáticas
Não executam o sistema, responsável por avaliar documentações através de revisões ou ferramentas, pode avaliar *requisitos*, *diagramas*, *código-fonte*
### Dinâmicas
##### Caixa-preta
Sabemos quais as saídas esperadas para determinadas entradas, porém não sabemos o sistema é internamente
##### Caixa-branca
Os testes são feitos com base em informações sobre a estrutura interna, código-fonte, do sistema
##### Exploratório
Baseados na experiência do *tester*, foco na descoberta de problemas e depende da intuição do profissional, ele aprende enquanto testa