Framework para criar drivers e testes automáticos para linguagem Java, é capaz de testar:
- Métodos
- Classes
- Componentes

Os testes são armazenados em em outra classe, separados do objeto de teste, por boas práticas, utilizam *annotation*: `@Test`

*Assetion*: compara o valor recebido com o valor esperado, teste é **bem sucedido** caso correspondam, **mal sucedido** caso não correspondam e não haja tratamento para essa exceção.

Ao serem executados, os testes podem ter os retornos:
- *Pass*: todos os métodos de asserção passaram
- *Fail*: método de asserção falhou
- *Error*: exceção

O objetivo é fazer com que todos os testes passem, isso pode ser atingido corrigindo o teste, caso o problema seja o teste, corrigindo a aplicação, caso o problema seja a aplicação.

Alguns métodos de verificação:
- `fail`
- `assertTrue`
- `assertEquals`
- `assertNull`
- `assertNotNull`
- `assertSame`
- `assertNotSame`

Possíveis anotações nos testes:
- `@Test`
- `@Before`
- `@After`
- `@BeforeClass`
- `@AfterClass`
- `@Ignore`

*Classe de teste parametrizada*: serve para que cada teste rode uma vez para cada parâmetro recebido, útil para criar testes utilizando massas de dados