# ⚙️ Etapa 2: APIs, Web Services e Persistência de Dados Distribuída

Este documento serve como diretriz mestre de engenharia e repositório de evidências para a **Etapa 2: Desenvolvimento de APIs, Web Services e Persistência**. Ele foi estruturado para orientar o desenvolvimento prático do backend distribuído e permitir o acompanhamento e auto-gestão das atividades pelos alunos.

---

## 🎯 Rubricas de Avaliação desta Etapa

Ao final desta Etapa, cada aluno será avaliado individualmente nestas 6 competências (incluindo oportunidades de desenvolvimento e reavaliação):

1. **H34a-SI-G: Gerenciar e documentar serviços de TI**: Gerenciar e documentar serviços de TI, de forma clara e objetiva (Reavaliação teórica e prática a partir do gerenciamento de serviços no backend em [src/backend/](src/backend/)).
2. **H35b-SI-G: Planejar, desenvolver e gerenciar uma arquitetura de aplicação distribuída**: Desenvolver uma arquitetura de aplicação distribuída (Medido no código em [src/backend/](src/backend/) e na seção [Modelagem da Aplicação e Arquitetura de Dados](#2-modelagem-da-aplicacao-e-arquitetura-de-dados)).
3. **H35c-SI-G: Planejar, desenvolver e gerenciar uma arquitetura de aplicação distribuída**: Gerenciar uma arquitetura de aplicação distribuída, testando, implantando e avaliando a solução (Medido na seção [Instruções de Implantação e DevOps](#5-instrucoes-de-implantacao-e-devops)).
4. **H36a-SI-G: Planejar, desenvolver e gerenciar APIs e Web Services**: Planejar e documentar APIs e Web Services, de forma clara e objetiva (Medido na seção [Especificação Avançada de Endpoints](#3-especificacao-avancada-de-endpoints) e atualizações no design de contratos).
5. **H36b-SI-G: Planejar, desenvolver e gerenciar APIs e Web Services**: Desenvolver APIs e Web Services (Medido em [src/backend/](src/backend/) e na construção real dos endpoints).
6. **H36c-SI-G: Planejar, desenvolver e gerenciar APIs e Web Services**: Gerenciar APIs e Web Services, testando, implantando e avaliando a solução (Medido na seção [Estratégia e Relatório de Testes Automatizados](#4-estrategia-e-relatorio-de-testes-automatizados)).

---

## 📅 QUADRO DE CONTRIBUIÇÃO REAL (ETAPA 2)

**Atenção alunos:** Preencham esta tabela para atualizar o andamento das tarefas e quem foi o responsável técnico pela construção do backend. Os nomes, usuários e links de evidências devem corresponder aos entregáveis em [src/backend/](src/backend/).

- **Status admitidos**: `⌛ Não Iniciado` | `📝 Em Progresso` | `✔️ Entregue`
- **Autoria Git**: Indica se há commits desse estudante nos arquivos da tarefa.

**Atividades Semanais desta Etapa** (ver [Cronograma do Semestre](contexto.md#-cronograma-do-semestre-semana--periodo)):
- `ATV2.1` — Desenvolvimento de Funcionalidades - API (Semanas 5 a 8)
- `ATV2.2` — Testes - API (Semana 9)

| Rubrica Curricular | ID Tarefa | Atividade Semanal | Descrição Detalhada da Tarefa | Estudante Responsável | GitHub Username | Status de Entrega | Evidência/Seção Temática | Autoria Git |
| :---: | :---: | :---: | :--- | :--- | :---: | :---: | :--- | :---: |
| **H36b** | `T2.1` | `ATV2.1` | Configuração do Boilerplate da API, Roteamento e Inicialização | [Nome do Aluno 1] | `username1` | `⌛ Não Iniciado` | [Instalação/README](src/backend/README.md) | [ ] |
| **H36b** | `T2.2` | `ATV2.1` | Modelagem e Persistência de Dados (Conexão DB, ORM, Schemas) | [Nome do Aluno 2] | `username2` | `⌛ Não Iniciado` | [Seção 2.1](#21-schema-e-diagrama-entidade-relacionamento) | [ ] |
| **H36b** | `T2.3` | `ATV2.1` | Implementação de Endpoints CRUD e Lógica de Negócios Principal | Giovanny Lisboa | `glisboapuc` | `⌛ Não Iniciado` | [Seção 3.0](#3-especificacao-avancada-de-endpoints) | [ ] |
| **H36b** | `T2.4` | `ATV2.1` | Mecanismo de Segurança da API (Autenticação/Autorização JWT) | [Nome do Aluno 4] | `username4` | `⌛ Não Iniciado` | [Seção 3.3](#33-seguranca-e-autorizacao) | [ ] |
| **H35b** | `T2.5` | `ATV2.1` | Gateway, Integração de Serviços Web e Clientes HTTP Externos | [Nome do Aluno 5] | `username5` | `⌛ Não Iniciado` | [Seção 2.2](#22-integracao-e-infraestrutura-distribuida) | [ ] |
| **H36c** | `T2.6` | `ATV2.2` | Desenvolvimento de Testes Automatizados (Unitários/Integração) | [Nome do Aluno 6] | `username6` | `⌛ Não Iniciado` | [Seção 4.0](#4-estrategia-e-relatorio-de-testes-automatizados) | [ ] |
| **H35c** | `T2.7` | `ATV2.1` | Construção de Dockerfile e Configuração de docker-compose | [Nome do Aluno 1] | `username1` | `⌛ Não Iniciado` | [Seção 5.1](#51-conteinerizacao-de-servicos) | [ ] |
| **H36c** | `T2.8` | `ATV2.2` | Proposta de Implantação e Pipeline de CI/CD Backend | [Nome do Aluno 5] | `username5` | `⌛ Não Iniciado` | [Seção 5.2](#52-proposta-de-infraestrutura-de-deploy-e-ambiente-em-producao) | [ ] |

---

# 1. Escopo e Objetivos do Backend

[Insira aqui uma breve introdução descrevendo o papel e os objetivos técnicos do seu ecossistema de APIs de backend. Esclareça quais microserviços ou módulos compõem a solução, a escolha de tecnologias de desenvolvimento (SGBDs, frameworks) e o que se espera em termos de volumetria e capacidade transacional.]

---

# 2. Modelagem da Aplicação e Arquitetura de Dados

*(Esta seção atende diretamente à rubrica **H35b**)*

## 2.1. Schema e Diagrama Entidade-Relacionamento

[Insira aqui o detalhamento lógico de banco de dados por meio de tabelas, relacionamentos, chaves primárias e estrangeiras. Também deve ser incluído o DER (Diagrama Entidade-Relacionamento) ou script de migração schema DDls.]

```
[Insira o Diagrama de Classes, DER ou representação lógica das entidades aqui]
```

## 2.2. Integração e Infraestrutura Distribuída

[Descreva como a sua arquitetura backend gerencia concorrência e escalabilidade física. Por exemplo: pool de conexões com banco de dados, divisão em microsserviços, tratamento de chamadas síncronas/assíncronas ou persistências distribuídas (como cache Redis, clusterização, mensageria via RabbitMQ).]

---

Analisando a **Seção 3 (Especificação Avançada de Endpoints)** do seu esboço em comparação com o template:

### 📊 Análise de Comparação

1. **Atendimento à Rubrica H36b**: Declarado no cabeçalho.
2. **3.1. Relação Geral de Endpoints**: O esboço possui todos os endpoints do projeto VagaLivre. **Ajuste necessário:** Alinhar o nome das colunas da tabela ao padrão exato do template (`Método / Verbo`, `Caminho da Rota (URI)`, `Descrição do Recurso / Ação`, `Reclama Autenticação?` e `Responsável Técnico`).
3. **3.2. Detalhamento dos Payloads**: O esboço contém os payloads reais do VagaLivre (substituindo os exemplos de *pedidos* do template). **Ajuste necessário:** Padronizar a formatação das subseções de cada endpoint utilizando os rótulos do template (`- **Verbo**:`, `- **Headers Requeridos**:`, `- **Payload de Entrada (JSON)**:`, `- **Payload de Resposta de Sucesso (...)**:`, etc.).
4. **3.3. Segurança e Autorização**: O esboço já atende a todos os pontos (CORS, HMAC-SHA256, expiração de 24h, tokens Bearer e controle de acesso baseado em papéis - RBAC entre `manager` e `resident`).

---

# 3. Especificação Avançada de Endpoints

*(Esta seção atende diretamente à rubrica **H36b**)*

Abaixo estão listados os contratos reais implementados e disponibilizados no diretório [`src/backend/`](src/backend/). Cada endpoint encontra-se detalhado descrevendo métodos HTTP, caminhos de rota, mecanismos de autenticação, payloads de requisição/resposta e comportamentos de erro. Em ambiente de produção, o acesso público é centralizado pelo API Gateway.

### 3.1. Relação Geral de Endpoints

| Método / Verbo | Caminho da Rota (URI) | Descrição do Recurso / Ação | Reclama Autenticação? | Responsável Técnico |
| :---: | :--- | :--- | :---: | :---: |
| `GET` | `/health` | Verificação de saúde (*health check*) do serviço e gateway | Não | Equipe |
| `POST` | `/api/v1/auth/login` | Autenticação de morador/síndico e geração de token HMAC | Não | Pedro |
| `GET` | `/api/v1/auth/me` | Recuperação dos dados do usuário autenticado na sessão | Sim (Bearer) | Pedro |
| `POST` | `/api/v1/auth/logout` | Encerramento da sessão no lado do cliente | Sim | Pedro |
| `GET` | `/api/v1/condominiums` | Listagem de condomínios cadastrados | Sim | Roberta |
| `GET` | `/api/v1/condominiums/:id` | Busca detalhada de um condomínio específico por ID | Sim | Roberta |
| `POST` | `/api/v1/condominiums` | Cadastro de novo condomínio | Sim (Síndico / Admin) | Roberta |
| `GET` | `/api/v1/users` | Listagem de usuários com filtros por status e condomínio | Sim (Síndico / Admin) | Roberta |
| `GET` | `/api/v1/users/:id` | Consulta de perfil de usuário específico | Sim | Roberta |
| `POST` | `/api/v1/users` | Cadastro de usuário (1º cadastro do condomínio vira `manager` aprovado) | Não (Onboarding) | Roberta |
| `PATCH` | `/api/v1/users/:id` | Atualização de perfil ou alteração de status (`approved` / `denied`) | Sim (Síndico / Próprio) | Roberta |
| `DELETE` | `/api/v1/users/:id` | Remoção de usuário do sistema | Sim (Admin) | Roberta |
| `GET` | `/api/v1/spots` | Consulta e listagem de vagas com filtros (`q`, `type`, `status`, `date`) | Sim | Allan |
| `GET` | `/api/v1/spots/:id` | Detalhamento de uma vaga de garagem específica | Sim | Allan |
| `GET` | `/api/v1/reservations` | Consulta de reservas com filtros por usuário e vaga | Sim | Gustavo |
| `GET` | `/api/v1/reservations/:id` | Detalhes de uma reserva específica | Sim | Gustavo |
| `POST` | `/api/v1/reservations` | Criação de reserva com validação de regras de agenda e conflitos | Sim | Gustavo |
| `DELETE` | `/api/v1/reservations/:id` | Cancelamento de reserva existente | Sim (Dono da reserva) | Gustavo |
| `GET` | `/notifications/user/:userId` | Consulta do histórico de avisos e notificações do morador | Sim | André |
| `POST` | `/notifications` | Registro de novo aviso e disparo de e-mail transacional | Sim | André |
| `PATCH` | `/notifications/:id/read` | Atualização de status da notificação para lida | Sim | André |
| `DELETE` | `/notifications/:id` | Exclusão de aviso do histórico | Sim | André |
| `GET` / `POST` / `PUT` / `DELETE` | `/api/ParkingSpots` | Endpoints CRUD HATEOAS para gestão de vagas (.NET ASP.NET Core) | Sim | Giovanny |

---

### 3.2. Detalhamento dos Payloads de Requisição e Resposta (Exemplos)

#### Endpoint: `/api/v1/auth/login` (Autenticação de Usuário)
- **Verbo**: `POST`
- **Headers Requeridos**: `Content-Type: application/json`
- **Payload de Entrada (JSON)**:
  ```json
  {
    "email": "teste@vagalivre.com",
    "password": "123456"
  }
  ```
- **Payload de Resposta de Sucesso (`200 OK`)**:
  ```json
  {
    "message": "Login realizado com sucesso.",
    "data": {
      "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9...",
      "user": {
        "id": "user-demo",
        "name": "Morador Teste",
        "email": "teste@vagalivre.com",
        "role": "resident",
        "status": "approved"
      }
    }
  }
  ```
- **Comportamento em caso de Erro (`401 Unauthorized` - Credenciais Inválidas)**:
  ```json
  {
    "message": "Credenciais inválidas ou conta pendente de aprovação."
  }
  ```

#### Endpoint: `/api/v1/auth/me` (Validação de Sessão)
- **Verbo**: `GET`
- **Headers Requeridos**: `Authorization: Bearer <token_hmac>`
- **Payload de Resposta de Sucesso (`200 OK`)**:
  ```json
  {
    "data": {
      "id": "user-demo",
      "name": "Morador Teste",
      "email": "teste@vagalivre.com",
      "role": "resident",
      "status": "approved"
    }
  }
  ```
- **Comportamento em caso de Erro (`401 Unauthorized` - Token Expirado/Inválido)**:
  ```json
  {
    "message": "Token de acesso inválido ou expirado."
  }
  ```

#### Endpoint: `/api/v1/spots` (Listagem e Filtro de Vagas)
- **Verbo**: `GET`
- **Headers Requeridos**: `Authorization: Bearer <token_hmac>`
- **Parâmetros de Busca (Query Params)**: `q`, `type` (`compact` | `standard` | `suv` | `motorcycle`), `status` (`available` | `occupied`), `date` (`YYYY-MM-DD`)
- **Payload de Resposta de Sucesso (`200 OK`)**:
  ```json
  {
    "data": [
      {
        "id": "spot-demo",
        "number": "A-01",
        "type": "standard",
        "location": "Subsolo 1",
        "isAvailable": true,
        "ownerId": "user-demo",
        "availability": [],
        "reservations": []
      }
    ]
  }
  ```

#### Endpoint: `/api/v1/reservations` (Criação de Reserva)
- **Verbo**: `POST`
- **Headers Requeridos**: `Authorization: Bearer <token_hmac>`, `Content-Type: application/json`
- **Payload de Entrada (JSON)**:
  ```json
  {
    "spotId": "spot-demo",
    "userId": "user-demo",
    "startTime": "2026-10-08T08:00:00Z",
    "endTime": "2026-10-10T18:00:00Z",
    "vehiclePlate": "XYZ-9A87"
  }
  ```
- **Payload de Resposta de Sucesso (`201 Created`)**:
  ```json
  {
    "message": "Vaga reservada com sucesso!",
    "data": {
      "id": "res-1029",
      "spotId": "spot-demo",
      "userId": "user-demo",
      "startTime": "2026-10-08T08:00:00Z",
      "endTime": "2026-10-10T18:00:00Z",
      "vehiclePlate": "XYZ-9A87"
    }
  }
  ```
- **Comportamento em caso de Erro (`409 Conflict` - Conflito de Agenda)**:
  ```json
  {
    "message": "A vaga selecionada já possui reserva no período informado."
  }
  ```

#### Endpoint: `/api/v1/users` (Cadastro de Usuário)
- **Verbo**: `POST`
- **Headers Requeridos**: `Content-Type: application/json`
- **Payload de Entrada (JSON)**:
  ```json
  {
    "name": "Novo Morador",
    "email": "morador@vagalivre.com",
    "password": "senhaSegura123",
    "condominiumId": "condo-01"
  }
  ```
- **Payload de Resposta de Sucesso (`201 Created`)**:
  ```json
  {
    "message": "Usuário cadastrado com sucesso. Aguardando aprovação do síndico.",
    "data": {
      "id": "user-new",
      "name": "Novo Morador",
      "email": "morador@vagalivre.com",
      "role": "resident",
      "status": "pending"
    }
  }
  ```

---

### 3.3. Segurança e Autorização

A segurança do canal de comunicação e o controle de acesso ao ecossistema de APIs do **VagaLivre** foram estruturados em quatro camadas complementares:

1. **CORS (Cross-Origin Resource Sharing):** Habilitado em todos os microsserviços e no API Gateway para restrição e suporte seguro às requisições originadas dos clientes Web e Mobile.
2. **Gestão de Segredos e Variáveis de Ambiente:** Credenciais sensíveis (como `DATABASE_URL`, `JWT_SECRET` e tokens de serviço de e-mail) não são armazenadas no repositório Git, sendo injetadas diretamente através das variáveis de ambiente na plataforma de hospedagem Render. O arquivo `.env` é mantido no `.gitignore`.
3. **Autenticação por Token de Sessão (HMAC-SHA256):** O serviço de identidade assina os tokens no momento do login utilizando a biblioteca criptográfica nativa do Node.js (`crypto.createHmac("sha256", JWT_SECRET)`). O token expede um *payload* contendo `{ id, email, role, exp }` com validade de **24 horas**. O cliente deve transmitir o cabeçalho `Authorization: Bearer <token>` em todas as rotas protegidas.
4. **Controle de Acesso Baseado em Papéis (RBAC):**
   - Papel **`manager` (Síndico):** Possui privilégios para criar novos condomínios, visualizar todos os moradores do condomínio e alterar o status de aprovação de novos cadastros (`approved` / `denied`).
   - Papel **`resident` (Morador):** Possui permissão para consultar vagas disponíveis, realizar reservas de vagas e gerenciar seus próprios dados.
   - **Validação de Status e Posse:** O login e o acesso às funcionalidades principais são restritos a contas com status `approved`. Operações sensíveis de escrita/exclusão (como cancelar uma reserva) validam se o `userId` requisitante corresponde ao proprietário do recurso, retornando erro `403 Forbidden` em caso de divergência.

---

# 4. Estratégia e Relatório de Testes Automatizados

*(Esta seção atende diretamente à rubrica **H36c**)*

[Explique a estratégia adotada pela equipe para testar as rotas de backend. Detalhe como rodar os testes localmente no repositório. O processo de avaliação pedagógica identificará a implementação física destes testes no diretório de código para validar as metas da rubrica.]

1. **Ferramenta de Asserção Utilizada**: (Ex: `Jest` em Node, `pytest` em Python, `xUnit/NUnit` em .NET).
2. **Método de Execução do Comando de Teste**:
   *(Exemplo)*: `npm run test:cov` ou `dotnet test`.
3. **Cobertura Esperada/Alcançada**: (Porcentagem geral de caminhos de controle avaliados).

### Exemplo de Quadro de Cobertura de Testes:

| Módulo do Sistema | Tipo de Teste (Unitário/Integração) | Cenários Avaliados | Status da Suíte |
| :--- | :--- | :--- | :---: |
| **Módulo de Autenticação** | Unitário | Geração do JWT, senhas incorretas, usuários inexistentes | ✔️ Passou |
| **Serviço de Pedidos** | Integração (com DB mockado) | Criação de orders, validação de itens esgotados, cálculo de frete | ✔️ Passou |

---

# 5. Instruções de Implantação e DevOps

*(Esta seção atende diretamente à rubrica **H35c**)*

Abaixo detalhe como a aplicação backend é empacotada de forma portável e como seria o processo ideal de implantação/hospedagem em nuvem (proposta teórica). **Nota:** Não há cobrança de deploy prático em nuvem nesta disciplina; a avaliação consiste na demonstração teórica da arquitetura física proposta e nas automações de build/testes locais.

## 5.1. Conteinerização de Serviços

[Insira aqui a justificativa e os caminhos de arquivos das imagens Docker criadas. Demonstre como múltiplos contêineres se comunicam na mesma rede por meio de um arquivo `docker-compose.yml` que sobe a API de backend juntamente com quaisquer instâncias de banco de dados ou mensageria de forma auto-contida para execução e testes locais.]

- **Caminho do Dockerfile do Backend**: `[src/backend/Dockerfile](src/backend/Dockerfile)` *(adicione o link do arquivo se ele já existir)*
- **Caminho do Docker Compose**: `[docker-compose.yml](docker-compose.yml)` *(opcional se na raiz)*

---

## 5.2. Proposta de Infraestrutura de Deploy e Ambiente em Produção

[Descreva de forma conceitual como seria estruturado o deploy contínuo (CI/CD) para o ambiente de produção. Por exemplo, indique como seria configurado o GitHub Actions para rodar testes locais e como seria a topologia de implantação na nuvem (ex: Render, AWS, Fly.io, Azure).]

- **Modelo de CI/CD Planejado**: [Indique que ações seriam realizadas a cada push/pull request para validar o código, como testes rodando automaticamente.]
- **Arquitetura Física Proposta**: [Apresente as premissas de arquitetura de hospedagem planejadas: onde a API responderia, como seriam geridos os bancos de dados em nuvem e variáveis de ambiente secretas.]

---

# 6. Referências Acadêmicas e de Engenharia

[Registre as referências que deram suporte técnico para a modelagem lógica, banco de dados ou metodologias de automação do backend das APIs.]

1. **DATE, C. J**. *Introdução a Sistemas de Bancos de Dados*. Rio de Janeiro: Elsevier, 2004.
2. **RICHARDSON, Leonard; RUBY, Sam**. *RESTful Web Services*. O'Reilly Media, 2007.
3. [Adicione referências de documentação oficial, SGBDs ou bibliotecas utilizadas].
