## Minimal.Api

APIs Mínimas com ASP.NET Core​  por Rafael V. Suarez​

### O que são APIs Mínimas?

- Arquitetura simplificada para criar APIs HTTP​
- Poucas dependências e arquivos​
- Ideal para microsserviços e apps leves​
- Alternativa ao uso de Controllers

### Estrutura do Projeto​

- Criação com modelo ASP.NET Core Vazio​
- Utiliza .NET 9.0​
- Arquivo principal: Program.cs​
- Banco de dados In-Memory com EF Core​
- Link repo

### Endpoints da API

- GET /todoitems - Lista todos os itens​
- GET /todoitems/complete - Itens concluídos​
- GET /todoitems/{id} - Item por ID​
- POST /todoitems - Criação de item​
- PUT /todoitems/{id} - Atualização​
- DELETE /todoitems/{id} - Exclusão

### Program.cs - Estrutura Básica

- Builder e serviços configurados​
- Mapeamento de rotas com MapGet, MapPost etc.​
- Uso de Entity Framework com banco em memória​
- Uso de Result e TypedResults para respostas

### Organização com MapGroup​

- Evita repetição de prefixo de URL​
- Criação de grupos de rotas:
  app.MapGroup("/todoitems")​
- Aplicável a configurações como autenticação

### TypedResults e Métodos Nomeados​

- Melhor integração com OpenAPI​
- Facilidade de testes unitários​
- Melhora legibilidade e reutilização​
- Métodos estáticos com retorno IResult

### Uso de DTOs​

- Evita excesso de postagem (Overposting)​
- Oculta campos sensíveis (ex: Secret)​
- Melhora segurança e performance​
- Classe TodoItemDTO com projeção parcial do modelo

### Execução e Testes​

- Uso do Endpoint Manager e arquivos .http​
- Testes com POST, GET, PUT e DELETE​
- Respostas em JSON com status HTTP apropriados​
- Banco de dados é resetado a cada execução​

### Resumo

- APIs mínimas são leves e diretas​
- Ideal para microserviços e aplicações simples​
- Fácil de organizar com MapGroup e TypedResults​
- Uso recomendado de DTOs por segurança e boas práticas

## Referências

- [Documentação Oficial ASP.NET Core](https://docs.microsoft.com/aspnet/core/)
- [Tutorial](https://learn.microsoft.com/en-us/aspnet/core/tutorials/min-web-api?view=aspnetcore-9.0&tabs=visual-studio)
- [Visao Geral de apis minimas](https://learn.microsoft.com/pt-br/aspnet/core/fundamentals/minimal-apis/overview?view=aspnetcore-9.0)
- [Alternativa FastEndpoint](https://fast-endpoints.com/)
- [Alternativa API Docs Scalar ](https://scalar.com/)