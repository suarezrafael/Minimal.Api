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