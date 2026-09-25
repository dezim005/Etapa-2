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
| **H36b** | `T2.2` | `ATV2.1` | Modelagem e Persistência de Dados (Conexão DB, ORM, Schemas) | Todos | `username1` `username2` `username3` `username4` `username5` `username6` | `⌛ Não Iniciado` `⌛ Não Iniciado` `⌛ Não Iniciado` `⌛ Não Iniciado` `⌛ Não Iniciado` `⌛ Não Iniciado` | [Seção 2.1](#21-schema-e-diagrama-entidade-relacionamento) | [ ] |
| **H36b** | `T2.3` | `ATV2.1` | Implementação de Endpoints CRUD e Lógica de Negócios Principal | Todos | `username1` `username2` `username3` `username4` `username5` `username6` | `⌛ Não Iniciado` `⌛ Não Iniciado` `⌛ Não Iniciado` `⌛ Não Iniciado` `⌛ Não Iniciado` `⌛ Não Iniciado` | [Seção 3.0](#3-especificacao-avancada-de-endpoints) | [ ] |
| **H36b** | `T2.4` | `ATV2.1` | Mecanismo de Segurança da API (Autenticação/Autorização JWT) | [Nome do Aluno 4] | `username4` | `⌛ Não Iniciado` | [Seção 3.3](#33-seguranca-e-autorizacao) | [ ] |
| **H35b** | `T2.5` | `ATV2.1` | Gateway, Integração de Serviços Web e Clientes HTTP Externos | [Nome do Aluno 5] | `username5` | `⌛ Não Iniciado` | [Seção 2.2](#22-integracao-e-infraestrutura-distribuida) | [ ] |
| **H36c** | `T2.6` | `ATV2.2` | Desenvolvimento de Testes Automatizados (Unitários/Integração) | Todos | `username1` `username2` `username3` `username4` `username5` `username6` | `⌛ Não Iniciado` `⌛ Não Iniciado` `⌛ Não Iniciado` `⌛ Não Iniciado` `⌛ Não Iniciado` `⌛ Não Iniciado` | [Seção 4.0](#4-estrategia-e-relatorio-de-testes-automatizados) | [ ] |
| **H35c** | `T2.7` | `ATV2.1` | Construção de Dockerfile e Configuração de docker-compose | [Nome do Aluno 1] | `username1` | `⌛ Não Iniciado` | [Seção 5.1](#51-conteinerizacao-de-servicos) | [ ] |
| **H36c** | `T2.8` | `ATV2.2` | Proposta de Implantação e Pipeline de CI/CD Backend | [Nome do Aluno 5] | `username5` | `⌛ Não Iniciado` | [Seção 5.2](#52-proposta-de-infraestrutura-de-deploy-e-ambiente-em-producao) | [ ] |

---

# 1. Escopo e Objetivos do Backend

[Insira aqui uma breve introdução descrevendo o papel e os objetivos técnicos do seu ecossistema de APIs de backend. Esclareça quais microserviços ou módulos compõem a solução, a escolha de tecnologias de desenvolvimento (SGBDs, frameworks) e o que se espera em termos de volumetria e capacidade transacional.]

---

# 2. Modelagem da Aplicação e Arquitetura de Dados `Andre`

## 2.1. Schema e Diagrama Entidade-Relacionamento `Andre`

O serviço de notificações foi projetado para garantir o registro individualizado, a rastreabilidade e a persistência do histórico de avisos enviados aos moradores do condomínio. A modelagem de dados utiliza o ORM **Prisma** conectado a uma instância do banco de dados relacional **PostgreSQL hospedado na plataforma Serverless Neon**.

### A. DDL e Representação do Schema Prisma [schema.prisma](https://github.com/ICEI-PUC-Minas-PMV-SI/pmv-si-2026-2-pe6-t2-g09/blob/main/src/backend/andre/schema.prisma)

A entidade central do serviço é a tabela `Notification`, estruturada no arquivo de schema da seguinte forma:

```
// Módulo de Notificações - Vaga Livre
model Notification {
  id        String   @id @default(uuid())
  userId    String   // Chave Estrangeira lógica referenciando a entidade User
  title     String
  message   String
  type      String   @default("RESERVA_CONFIRMADA")
  read      Boolean  @default(false)
  createdAt DateTime @default(now())
  updatedAt DateTime @updatedAt

  @@map("notifications")
}
```
### B. Dicionário de Dados da Tabela `notifications`

| Campo         | Tipo SQL       | Restrições                      | Descrição                                                            |
| ------------- | -------------- | ------------------------------- | -------------------------------------------------------------------- |
| **id**        | `VARCHAR(36)`  | **PK**, Not Null, Unique        | Identificador único universal (UUID) da notificação.                 |
| **userId**    | `VARCHAR(36)`  | **FK** (Lógica), Not Null       | Identificador do usuário/morador destinatário da mensagem [2, 11]. |
| **title**     | `VARCHAR(255)` | Not Null                        | Título do aviso (ex: "Reserva Confirmada") [2, 11].                |
| **message**   | `TEXT`         | Not Null                        | Conteúdo descritivo detalhado da notificação enviada [2, 11].      |
| **type**      | `VARCHAR(50)`  | Default: `'RESERVA_CONFIRMADA'` | Categoria do evento gerador da notificação.                          |
| **read**      | `BOOLEAN`      | Default: `false`                | Status de leitura da mensagem pelo usuário.                          |
| **createdAt** | `TIMESTAMP`    | Default: `NOW()`                | Data e hora exatas da criação e envio do registro.                   |
| **updatedAt** | `TIMESTAMP`    | UpdatedAt                       | Data e hora da última modificação do registro.                       |

### C. Diagrama Entidade-Relacionamento (DER)

Abaixo é apresentada a representação lógica do relacionamento entre a entidade de usuários/moradores e o serviço de notificações do **Vaga Livre**:

```mermaid
erDiagram
    USER ||--o{ NOTIFICATION : "recebe"
    
    USER {
        string id PK
        string name
        string email
    }
    
    NOTIFICATION {
        string id PK
        string userId FK
        string title
        string message
        string type
        boolean read
        datetime createdAt
        datetime updatedAt
    }
```

<img width="1909" height="903" alt="table notification" src="https://github.com/user-attachments/assets/55aa9335-a9aa-470e-98ef-6e924d8f2f3b" />

*Tabelas criadas diretamente no painel da **Neon PostgreSQL**, mostrando os registros inseridos após os testes de confirmação de reserva*


## 2.2. Integração e Infraestrutura Distribuída `Andre`

A arquitetura do Backend do **Vaga Livre** foi projetada sob o paradigma de microsserviços/serviços distribuídos, visando alta disponibilidade, desacoplamento e tempo de resposta otimizado para o usuário final.

```
[ Frontend (React/Next) ]
       │
       │  (Chamada HTTP / CORS)
       ▼
[ Backend API (Express/Node.js) ] ── (Prisma Pool) ──► [ Neon PostgreSQL (Cloud) ]
       │
       │  (Requisição Assíncrona HTTPS / Porta 443)
       ▼
[ Resend API (Email Service) ] ──────────────────────► [ Caixa de Entrada do Morador ]

```

### 1. Comunicação Entre Serviços e Gestão de CORS

O **Frontend** e o **Backend** da aplicação operam como serviços independentes (*Web Services*) implantados na nuvem através do **Render**.

* A comunicação cross-origin é gerenciada pelo middleware `cors()` no servidor Express (`server.ts`).
* O endereço do Backend é injetado dinamicamente no Frontend por meio da variável de ambiente `NEXT_PUBLIC_API_URL`, garantindo a segurança e o desacoplamento das URLs de produção.

### 2. Gerenciamento de Concorrência e Connection Pooling (Neon + Prisma)

Para gerenciar múltiplas requisições simultâneas sem esgotar os recursos de banco de dados:

* É utilizado o **Prisma Client** encapsulado como uma instância *singleton*.
* O banco de dados **Neon PostgreSQL** utiliza uma camada de *Connection Pooling Serverless*. Isso permite que centenas de conexões simultâneas vindas das instâncias do Render sejam multiplexadas eficientemente sem causar estouro de memória no banco relacional.

### 3. Tratamento Assíncrono Não-Bloqueante (Non-blocking I/O)

Para evitar travamentos da interface e tempo de espera excessivo (*latency*) ao confirmar uma reserva:

* O controller (`NotificationController.ts`) executa a gravação da notificação no banco via Prisma (`await prisma.notification.create(...)`) e **responde imediatamente ao cliente HTTP** com o código de sucesso `201 Created`.
* O disparo do e-mail é delegado para execução em segundo plano (*background execution*) através de uma Promise assíncrona não-bloqueante.

### 4. Resiliência e Tráfego de E-mail por API HTTP (Resend)

Para contornar o bloqueio de portas SMTP tradicionais (25, 465, 587) comum em infraestruturas Serverless/PaaS em nuvem como o Render:

* A arquitetura adota a **Resend API**, realizando o envio de e-mails transacionais via chamadas **REST/HTTPS na porta 443**.
* Essa abordagem elimina *timeouts* de rede (`ETIMEDOUT` / `ENETUNREACH`), garante entrega instantânea e isola falhas de infraestrutura de rede externa.

# 3. Especificação Avançada de Endpoints `Andre`

Abaixo estão listados os contratos reais implementados no diretório [src/backend/andre](src/backend/andre) para o módulo de **Notificações**, detalhando os métodos HTTP, rotas, payloads de requisição/resposta, códigos de status e mecanismos de segurança da API.

### 3.1. Relação Geral de Endpoints `Andre`

| Método / Verbo | Caminho da Rota (URI)         | Descrição do Recurso / Ação                                    | Reclama Autenticação? | Responsável Técnico |
| -------------- | ----------------------------- | -------------------------------------------------------------- | --------------------- | ------------------- |
| `POST`         | `/notifications`              | Cria notificação no banco Neon e dispara e-mail via Resend API | Sim                   | André Lopes         |
| `GET`          | `/notifications/user/:userId` | Listagem de todas as notificações gravadas de um morador       | Sim                   | André Lopes         |
| `PATCH`        | `/notifications/:id/read`     | Atualiza o status da notificação para lida (`read: true`)      | Sim                   | André Lopes         |
| `DELETE`       | `/notifications/:id`          | Remove um registro de notificação do histórico do usuário      | Sim                   | André Lopes         |
---

### 3.2. Detalhamento dos Payloads de Requisição e Resposta (Exemplos) `Andre`

#### Endpoint 1: `/notifications` (Criação e Disparo de Notificação)

* **Verbo**: `POST`
* **Headers Requeridos**: `Content-Type: application/json`
* **Payload de Entrada (JSON)**:

```
{
  "userId": "usr-882319",
  "userEmail": "andre.lopes.1521271@sga.pucminas.br",
  "title": "Reserva Confirmada",
  "message": "Sua reserva para a vaga A-12 foi confirmada com sucesso!",
  "type": "RESERVA_CONFIRMADA"
}

```

* **Payload de Resposta de Sucesso (** **201 Created** **)**:

```
{
  "id": "f47ac10b-58cc-4372-a567-0e02b2c3d479",
  "userId": "usr-882319",
  "title": "Reserva Confirmada",
  "message": "Sua reserva para a vaga A-12 foi confirmada com sucesso!",
  "type": "RESERVA_CONFIRMADA",
  "read": false,
  "createdAt": "2026-09-24T22:39:42.102Z",
  "updatedAt": "2026-09-24T22:39:42.102Z"
}

```

* **Comportamento em caso de Erro (** **400 Bad Request** **\- Parâmetro Ausente)**:

```
{
  "error": "Campos obrigatórios ausentes."
}

```

* **Comportamento em caso de Erro Interno (** **500 Internal Server Error** **)**:

```
{
  "error": "Erro ao processar notificação."
}

```

---

#### Endpoint 2: `/notifications/user/:userId` (Listagem de Notificações do Morador)

* **Verbo**: `GET`
* **Parâmetros de Rota**: `userId` (string UUID do morador)
* **Payload de Resposta de Sucesso (** **200 OK** **)**:

```
[
  {
    "id": "f47ac10b-58cc-4372-a567-0e02b2c3d479",
    "userId": "usr-882319",
    "title": "Reserva Confirmada",
    "message": "Sua reserva para a vaga A-12 foi confirmada com sucesso!",
    "type": "RESERVA_CONFIRMADA",
    "read": false,
    "createdAt": "2026-09-24T22:39:42.102Z"
  }
]

```

---

#### Endpoint 3: `/notifications/:id/read` (Marcar Notificação como Lida)

* **Verbo**: `PATCH`
* **Parâmetros de Rota**: `id` (string UUID da notificação)
* **Payload de Resposta de Sucesso (** **200 OK** **)**:

```
{
  "id": "f47ac10b-58cc-4372-a567-0e02b2c3d479",
  "read": true,
  "updatedAt": "2026-09-24T22:45:10.512Z"
}
```

---

### 3.3. Segurança e Autorização `Andre`

A segurança da infraestrutura e do tráfego de dados da API de Notificações é fundamentada em quatro pilares principais:

1. **Criptografia em Trânsito (HTTPS/TLS)**: Toda a comunicação entre a aplicação cliente (Frontend) e a API Backend hospedada no **Render** ocorre através de conexões seguras criptografadas sob o protocolo **HTTPS (TLS 1.3)** na porta padrão `443`.
2. **Política de Origem Cruzada (CORS)**: O servidor Express implementa o middleware `cors()` configurado para autorizar exclusivamente requisições vinda do domínio do Frontend do **Vaga Livre**, prevenindo ataques de origens não autorizadas (*Cross-Site Request Forgery / CSRF*).
3. **Gerenciamento de Credenciais e Variáveis de Ambiente**: Chaves sensíveis como a URL do banco PostgreSQL Neon (`DATABASE_URL`) e a chave da API do Resend (`RESEND_API_KEY`) são isoladas e mantidas estritamente no ambiente do servidor na nuvem (**Render Environment Variables**), nunca expostas no código-fonte nem enviadas ao cliente/navegador.
4. **Tráfego Seguro de E-mails via HTTPS**: Para evitar varreduras de porta e ataques de *man-in-the-middle* comuns em conexões SMTP puras, a API dispara e-mails através do SDK oficial da **Resend API**, autenticando via chave de API criptografada e realizando requisições HTTPS REST diretas na porta `443`.

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

