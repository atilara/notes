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

(**[Food.com](http://Food.com) Recipes with Ingredients and Tags**)

**Basic Information:**

- `id`: Unique identifier for each recipe.
- `name`: The title of the recipe.
- `description`: A brief overview of the recipe.

**Detailed Recipe Breakdown:**

- `steps`: Step-by-step cooking instructions.

**Ingredient Insights:**

- `ingredients_raw`: Original list of ingredients as written in the recipe.
- `ingredients`: Cleaned and processed list of ingredients.

**Additional Details:**

- `servings`: Suggested number of servings.
- `serving_size`: The amount per serving.
- `tags`: Keywords associated with the recipe (e.g., vegan, quick, summer).

[https://www.kaggle.com/datasets/realalexanderwei/food-com-recipes-with-ingredients-and-tags](https://www.kaggle.com/datasets/realalexanderwei/food-com-recipes-with-ingredients-and-tags)