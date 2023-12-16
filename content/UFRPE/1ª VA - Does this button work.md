# Introdução
YouTube é o segundo site mais visitado do mundo e seu algoritmo é responsável por direcionar mais da metade das views dentro do site.

O YouTube indica que seus usuários podem gerenciar suas recomendações, através das *[ferramentas de feedback que a plataforma oferece](https://support.google.com/youtube/answer/6342839)*, quais seriam essas ferramentas?
## Retornos de usuário
- Dislike
- Não tenho interesse
- Não recomendar o canal
- Remover histórico
## Ideia do experimento
O Mozilla ouviu que esses usuários não se sentem em controle da sua experiência com o algoritmo de recomendação do YouTube. 

Dessa forma, **2.757** pessoas participaram de uma enquete sobre seus sentimentos em relação ao controle de recomendações na plataforma, o Mozilla aprendeu que muitos sentem que suas ações não possuem nenhum efeito em suas recomendações do YouTube.

Citação pra embasar. Relato de usuária que mudou seu comportamento de utilização do YouTube para tentar "domar" o algoritmo.
# Experimento

## Hipótese e variáveis

Para testar se isso se traduz em dados, o Mozilla recebeu doação de dados de **22.722** usuários de sua extensão *[RegretsReporter](https://foundation.mozilla.org/youtube/regretsreporter/)* a respeito de suas interações com o YouTube. Gerando uma *base de dados* de mais de **500 mil** vídeos recomendados pelo algoritmo do YouTube.

Procura testar as hipotéses:

>Eficácia dos controles de usuário do YouTube na prevenção de recomendações indesejadas

>Adicionar um botão mais conveniente para feedback do usuário pode aumentar a taxa de uso dos controles de feedback?

Diante dessas hipotéses, podemos construir o quadro de variáveis da pesquisa:
- Hipótese 01:
	- Independente: Utilização de retornos do usuário
	- Depentende: mudança nas recomendações do YouTube 
- Hipótese 02:
	- Independente: UX para feedbacks mais amigável
	- Dependente: número de feedbacks
Relação de **causa e efeito** entre os tipos de variáveis
## RegretsReporter

Extensão para navegador onde a pesquisa foi realizada, já era utilizada com o intuito de eliminar recomendações indesejadas, por isso a quantidade alta de participantes. a coleta de dados foi adicionada para realização da pesquisa com usuários que concordassem.

Após instalada, um botão de *Parar de recomendar* é adicionado a todo vídeo:

![[Pasted image 20231211212436.png]]

## Divisão de participantes
Com isso, chegamos na divisão de participantes, que define como a pesquisa realmente é feita.
### Hipótese 01

Dentro do experimento, um usuário é associado a um tipo de ferramenta de feedback do usuário (*Dislike, Não interessado, Não recomende o canal, Remover do histórico*). 

Dessa forma, quando um usuário clica em Parar de recomendar, a ação a qual ele está associada será disparada, caso ele seja do grupo de controle, nada acontece.

![[Pasted image 20231211213131.png]]

> O grupo de controle é utilizado para calcular a base do estudo, eles tinham a opção de clicar em "Parar de recomendar", porém **nenhum** feedback era enviado ao YouTube. 

Os dados coletados desse grupo foram utilizados para calcular o **percentual base de recomendações ruins** sem intervenção do usuário, é possível medir a efetividade de cada tipo de ferramenta de retorno do usuário ao **comparar os outros grupos com este**.

As taxas de *recomendações ruins* são comparadas para cada um desses grupos. 
### Hipótese 02

Divisão entre usuários:
- Os que possuíam a UX facilitada, oferecida pela extensão Regrets Reporter;
- Os que não possuíam e deveriam utilizar a UX original do YouTube, podemos ver na imagem que ela exige mais cliques. Para dar dislike, é necessário abrir o vídeo e para removê-lo do histórico é preciso abrir o histórico e encontrá-lo na listagem.

Foi realizada coleta de dados dos dois grupos com o objetivo de entender se uma UX mais amigável gera mais feedbacks.
# Dados

## Glossário

**Par de vídeo**:
- Vídeo rejeitado
- Vídeo recomendado
**Recomendação ruim**: vídeo recomendado similar ao vídeo rejeitado, o slide é um exemplo de par de vídeo que caracteriza uma recomendação ruim

## Coleta

- Tempo
- Total de participantes
- YouTube "cedeu" informações via API
- Quantidade de vídeos rejeitados (recomendações ruins) pelos usuários

## Análise de dados

Um modelo de *inteligência artificial* foi treinado para fazer essa classificação, já que seria impossível analisar mais de 500 milhões de vídeos.

Dados de acurácia e treinamento do modelo estão disponíveis de forma detalhada no site do Mozilla.

# Resultados

## Interpretação

### Taxa de recomendações ruins

![[Pasted image 20231211214612.png]]

### Prevenção de Recomendações ruins
Foi descoberto que o tipo de feedback mais eficiente não previne mais de 50% de recomendações ruins:

![[Pasted image 20231211213643.png]]

### Taxa de feedback

A quantidade de feedbacks realizados pelo usuário dobrou com a UX facilitada em comparação a UX atual
## Vantagens e Desafios do Estudo

### Vantagens

- Amostra Representativa: A extensão da Mozilla permitiu a participação de usuários reais, oferecendo uma amostra representativa, e que os usuário possuem interesse em participar do experimento, pois se beneficiarão.
- Coleta de Dados Detalhada: Dados extensos sobre interações, recomendações e classificações foram coletados, proporcionando uma visão abrangente e detalhada.

### Desafios/Desvantagens

- Limitações da API do YouTube: Restrições e limites na API do YouTube dificultaram a coleta completa de dados, destacando a necessidade de melhorias na transparência e acesso a dados.
- Classificação Subjetiva: A classificação de vídeos como "aceitáveis" ou "ruins" pode ser subjetiva, introduzindo um potencial viés na análise.

## Recomendações

>Os controles de usuário do YouTube devem ser fáceis de entender e acessar.

As pessoas devem receber informações claras sobre as medidas que podem tomar para influenciar as suas recomendações e devem ser capacitadas para utilizar essas ferramentas.

> O YouTube deve projetar suas ferramentas de feedback de uma forma que coloque as pessoas no comando.

As ferramentas de feedback devem permitir que as pessoas moldem sua experiência de forma proativa, com o feedback do usuário tendo mais peso na determinação de quais vídeos são recomendados.

>O YouTube deveria aprimorar suas ferramentas de acesso a dados.

O YouTube deve fornecer aos pesquisadores acesso a melhores ferramentas que lhes permitam avaliar os sinais que impactam o algoritmo do YouTube.

>Os decisores políticos devem proteger os investigadores de interesse público.

Os decisores políticos devem aprovar e/ou clarificar leis que proporcionem protecções legais à investigação de interesse público.