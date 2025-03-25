# Teste prático para Desenvolvedor Node.js

### Introdução
Este teste tem como objetivo avaliar seus conhecimentos em Node.js, Express, manipulação de dados e desenvolvimento frontend. Você deverá criar uma API RESTful e uma interface frontend conforme os requisitos descritos abaixo.

### Requisitos

1. **Backend (API):**
   - Crie uma API utilizando Node.js com Express.
   - A API deve ter as seguintes rotas:

      - **GET /clientes** - Listar todos os clientes.
      - **POST /clientes** - Adicionar um novo cliente.
      - **GET /clientes/:id** - Buscar um cliente pelo ID.
      - **PUT /clientes/:id** - Atualizar um cliente pelo ID.
      - **DELETE /clientes/:id** - Remover um cliente pelo ID.
      - **POST /clientes/import** - Importar clientes de forma bulk a partir de um arquivo Excel.

   - Utilize um array de objetos como banco de dados mockado para armazenar os clientes.
   - Crie uma camada de serviço separada que gerencie as operações de CRUD para organizar melhor a lógica do negócio.
   - Implemente uma função de middleware que registre todas as requisições realizadas na API (método, endpoint e timestamp).

2. **Frontend (Tela HTML):**
   - Crie uma tela em HTML simples que exiba a lista de clientes de forma dinâmica. Utilize o `GET /clientes` para obter os dados e mostrar na tela.
   - A tela deve exibir os seguintes campos:
      - Nome do cliente.
      - Email do cliente.
   - A tela também deve ter um formulário para adicionar um novo cliente, com os seguintes campos:
      - Nome.
      - Email.
   - Implemente a lógica para enviar o novo cliente para a API utilizando a rota `POST /clientes`.

3. **Exemplo de estrutura do cliente:**
   ```json
   {
       "id": 1,
       "nome": "João Silva",
       "email": "joao@email.com"
   }
    ```

### Regras de Negócio
- Os endpoints devem retornar mensagens claras em caso de erro (ex.: "Cliente não encontrado").

- Cada cliente deve ter um ID único e incremental.

- Utilize JSON para entrada e saída de dados.

O middleware deve exibir os logs no console com a seguinte estrutura:

```bash
[2024-09-14 14:30:00] - GET /clientes
[2024-09-14 14:30:00] - GET /clientes/1
[2024-09-14 14:30:00] - POST /clientes
[2024-09-14 14:30:00] - PUT /clientes/1
[2024-09-14 14:30:00] - DELETE /clientes/1
[2024-09-14 14:30:00] - GET /clientes
[2024-09-14 14:30:00] - POST /clientes
```

- A rota de importação deve permitir o envio de um arquivo Excel contendo uma lista de clientes para cadastro em massa.

- A tela HTML deve ser funcional e interativa, permitindo a adição de novos clientes e a exibição da lista atualizada de clientes.

### Critérios de Avaliação
- Estrutura e organização do código (backend e frontend).

- Correta implementação das rotas e suas funcionalidades.

- Boa utilização de mensagens de erro e status HTTP adequados.

- Uso adequado de funções assíncronas (se necessário).

- Implementação correta do middleware para logs.

- Implementação correta da funcionalidade de importação de clientes em massa.

- A tela HTML deve ser simples e funcional, com a capacidade de interagir com a API.

### Instruções para Entrega
- Crie um repositório público no GitHub contendo seu código (backend e frontend).

- Inclua um arquivo README.md explicando como rodar o projeto.

- Envie o link do repositório para o avaliador.

#### Boa sorte e bom código!
