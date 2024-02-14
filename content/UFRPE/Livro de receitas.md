## MySQL: Mario

- **Usuário**
    - uuid
    - username
    - email
    - password
	- favoritas: tabela a parte de relação, usuário/receita
- **Logs (ao fazer uma pesquisa salvaria um log, ex: {userId, searchType: recipe/ingredient, value: text recipe/array ingredients})**
    - ultimas buscas (a definir) (pode ser uma tabela/collection a parte)
## MongoDB: Átila

- **Receita**
    - uuid
    - title
    - description
    - ingredients
    - avaliação: array com objetos que armazenam o id do usuário e a nota
    - tempo de preparo: estará nulo por limitação do dataset
    - passos: array de passos
    - quantas porções
    - tamanho da porção
- **Ingredientes únicos**
    - id
    - name
## Neo4j: João

- **Pesquisa por receitas a partir de ingredientes**
    - Receitas que possuem os ingredientes/Receitas que possuem apenas os ingredientes

## Observações

Pesquisa por receitas diretamente pelo nome dela (Ex: bolo de chocolate) será feita através do **MongoDB** e a pesquisa pela receita através da construção de seus ingredientes será feita pelo **Neo4j**

Ordenação e Filtros em cima do resultado retornado de receitas (maleavel dependendo dos campos disponiveis na receita) **(Mongo query)**
- Ordenar por tempo de preparo (crescente e decrescente)
- Ordenar por tamanho da porção
- Filtrar por categoria/tags (sobremesa, café da manhã, almoço, italiana, japonesa, etc…)
- Ordenar por avaliação

O mongo precisará gerar um .csv com os dados da receita:
- uuid
- title
- ingredients
Um depende do outro no contexto da aplicação, seus dados são diretamente ligados e a responsabilidade de popular o neo4j com base nos dados armazenados no mongo seria da aplicação.
# Dataset

*[https://www.kaggle.com/datasets/sooryaprakash12/cleaned-indian-recipes-dataset](https://www.kaggle.com/datasets/sooryaprakash12/cleaned-indian-recipes-dataset)*
##### To do

- [x] Modelagem
- [x] Scripts de inserção dos dados
- [x] Imagens docker
	- [x] Mongo
	- [x] Neo4j
	- [x] MariaDB
- [ ] Desenhar modelagem
- [ ] Slide
- [ ] Atualizar os ingredientes únicos do mongo
- [ ] Atualizar o nome dos campos do csv
- [ ] Queries
	- [ ] MongoDB e perguntas
	- [ ] Neo4J e perguntas
	- [x] MariaDB e perguntas
- [ ] Garantir consistência entre IDs dos diferentes bancos