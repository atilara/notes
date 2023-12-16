# Introdução
YouTube é o segundo site mais visitado do mundo e seu algoritmo é responsável por direcionar mais da metade das views dentro do site.

O YouTube indica que seus usuários podem gerenciar suas recomendações, através das *[ferramentas de feedback que a plataforma oferece](https://support.google.com/youtube/answer/6342839)*, quais seriam essas ferramentas?
# Retornos de usuário
- Dislike
- Não tenho interesse
- Não recomendar o canal
- Remover histórico
# Ideia do experimento
O Mozilla ouviu que esses usuários não se sentem em controle da sua experiência com o algoritmo de recomendação do YouTube. 

Dessa forma, **2.757** pessoas participaram de uma enquete sobre seus sentimentos em relação ao controle de recomendações na plataforma, o Mozilla aprendeu que muitos sentem que suas ações não possuem nenhum efeito em suas recomendações do YouTube.

Citação pra embasar.

Denificação do que seria uma recomendação ruim, que incomoda os participantes da survey. Assim, foi realizado o experimento

# Experimento
Para testar se isso se traduz em dados, o Mozilla recebeu doação de dados de **22.722** usuários de sua extensão *[RegretsReporter](https://foundation.mozilla.org/youtube/regretsreporter/)* a respeito de suas interações com o YouTube. Gerando uma *base de dados* de mais de **500 mil** vídeos recomendados pelo algoritmo do YouTube.

Procura testar as hipotéses:

>Eficácia dos controles de usuário do YouTube na prevenção de recomendações indesejadas

>Adicionar um botão mais conveniente para feedback do usuário pode aumentar a taxa de uso dos controles de feedback?

## RegretsReporter
Extensão onde a pesquisa do Mozilla foi executada, busca responder duas perguntas:
### Hipótese 01
Após instalada, um botão de *Parar de recomendar* é adicionado a todo vídeo:

![[Pasted image 20231211212436.png]]

Dentro do experimento, um usuário é associado a um tipo de ferramenta de feedback do usuário (*Dislike, Não interessado, Não recomende o canal, Remover do histórico*). 

Dessa forma, quando um usuário clica em Parar de recomendar, a ação a qual ele está associada será disparada, caso ele seja do grupo de controle, nada acontece.

![[Pasted image 20231211213131.png]]

O grupo de controle é utilizado para calcular a base do estudo, eles tinham a opção de clicar em "Parar de recomendar", porém **nenhum** feedback era enviado ao YouTube. Os dados coletados desse grupo foram utilizados para calcular o **percentual base de recomendações ruins** sem intervenção do usuário, é possível medir a efetividade de cada tipo de ferramenta de retorno do usuário ao **comparar os outros grupos com este**.

As taxas de *recomendações ruins* são comparadas para cada um desses grupos. Um modelo de *inteligência artificial* foi treinado para fazer essa classificação, já que seria impossível analisar mais de 500 milhões de vídeos. 

Foi descoberto que o tipo de feedback mais eficiente não previne mais de 50% de recomendações ruins:

![[Pasted image 20231211213643.png]]

### Hipótese 02

Divisão entre usuários que possuíam UX facilitada e os que não possuíam e deveriam utilizar a UX do YouTube. Foi realizada coleta de dados dos dois grupos com o objetivo de entender se uma UX mais amigável gera mais feedbacks.
## Interpretação

### Tipo de Feedback:

![[Pasted image 20231211214612.png]]


# Conceitos Básicos do Estudo:

1. Metodologia:

- Participantes: Usuários que instalaram a extensão web da Mozilla e optaram pelo experimento e coleta de dados.
- Grupos Experimentais: Divididos em controle, "dislike," "history," "not interested," e "don't recommend," com alguns sem botão de controle.
- Dados Coletados: ID de instalação, grupo experimental, uso do botão "Stop Recommending" com informações de onde foi usado e quando, recomendações do YouTube, interações com controles nativos e dados demográficos.

2. Análise de Dados:

- Período de Tempo: Dezembro de 2021 a junho de 2022.
- Participantes: 22,722 analisados após remoção de comportamentos excepcionais.
- Resultados: 30,314 vídeos rejeitados, 567,880,195 recomendações, 162,983,496 pares de vídeos analisados.
- Classificação: 24 assistentes de pesquisa classificaram 44,434 pares de vídeos em aceitáveis (75%), ruins (22%), e incertos (3%).


3. YouTube Data:

- Obtenção: Realizada por solicitações automáticas, incluindo informações de mais de 6 milhões de vídeos.

4. Métricas e Modelos:

- Taxa de Má Recomendação: Avaliou a eficácia dos controles do YouTube em evitar recomendações indesejadas.
- Taxa de Interação: Calculada como o número de interações dividido pelo número de vídeos assistidos, onde interações são algum tipo de uso do sistema nativo do youtube como clicar em não gostei.
- Modelo de Similaridade Semântica: Aplicado a pares não classificados por assistentes de pesquisa, utilizando um modelo de machine learning.

5. Pesquisa Adicional:

- Inclusão: Explorou experiências dos usuários no controle de recomendações no YouTube.
- Perguntas: Sobre eficácia das ações, mudanças nas recomendações, sensação de controle, desejos não atendidos e necessidade de informações sobre o algoritmo de recomendação.

### Vantagens e Desafios do Estudo:

#### Vantagens:

- Amostra Representativa: A extensão da Mozilla permitiu a participação de usuários reais, oferecendo uma amostra representativa, e que os usuário possuem interesse em participar do experimento, pois se beneficiarão.
- Coleta de Dados Detalhada: Dados extensos sobre interações, recomendações e classificações foram coletados, proporcionando uma visão abrangente e detalhada.

#### Desafios/Desvantagens:

- Limitações da API do YouTube: Restrições e limites na API do YouTube dificultaram a coleta completa de dados, destacando a necessidade de melhorias na transparência e acesso a dados.
- Classificação Subjetiva: A classificação de vídeos como "aceitáveis" ou "ruins" pode ser subjetiva, introduzindo um potencial viés na análise.

Etapas/Elementos:

1. Instalação da Extensão:
	- Participantes optaram por instalar a extensão da Mozilla e optaram pelo experimento.
2. Atribuição aos Grupos Experimentais:
	- Atribuição aleatória aos grupos de controle e experimentais, incluindo diferentes ações de controle.
3. Coleta de Dados:
	- Dados detalhados foram coletados, incluindo interações, recomendações, e dados demográficos.
4. Análise de Dados:
	- Análise abrangente da eficácia dos controles, taxas de recomendação indesejada e interações dos usuários.
5. Classificação por Pesquisadores:
	- 24 assistentes de pesquisa classificaram pares de vídeos quanto à qualidade da recomendação.
6. Modelo de Similaridade Semântica:
	- Aplicação de um modelo para pares não classificados, contribuindo para uma análise mais abrangente.
7. Pesquisa Adicional:
	- Exploração qualitativa das experiências dos usuários por meio de perguntas estruturadas.

  

### Correlação com o material:

1. Variáveis Independentes e Dependentes:

- Experimento: Envolve manipulação de variáveis independentes para observar seu impacto nas variáveis dependentes.
- "Does This Button Work?" Experimento: A variável independente é a ação do usuário no botão, e a variável dependente é a mudança nas recomendações do YouTube.

2. Observação e Medição:

- Experimento: Envolvem observação cuidadosa e medição precisa para coletar dados válidos.
- "Does This Button Work?" Experimento: Coletou dados sobre interações dos usuários, recomendações do YouTube e feedbacks para análise.

3. Teste de Hipóteses:

- Experimento: Geralmente inclui a formulação e teste de hipóteses para tirar conclusões significativas.
- "Does This Button Work?" Experimento: Testou a hipótese de que a ação do usuário no botão influenciaria as recomendações do YouTube.
