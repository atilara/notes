Precisamos criar *drivers* e *stubs* durante o processo de testagem, como foi explicado em [[Categorias de técnicas de teste]]

Alguns frameworks podem facilitar a criação de *stubs*/*mocks*, é o caso do *Mockito*

Por exemplo, para testar a integração entre uma classe *Model* (Responsável por ditar a estrutura do modelo, atributos e métodos) e uma classe *Repository* (Responsável por se comunicar com o banco de dados para inserir, consultar dados)

Caso a classe *Repository* não esteja pronta, é possível criar um *mock* para simular seu comportamento com os métodos `mock` e `when` do *Mockito*

Se o testador não definir o comportamento do *mock*, o valor de retorno dos métodos emulados
pelo é retornar:
- `null`: se o tipo de retorno é uma referência
- `0`: se o tipo retorno é numérico
- `false`: se tipo do retorno é booleano

É possível definir o comportamento e retorno dos *mocks*