# Agenda Web

Sistema de agenda pessoal com gerenciamento de **Contatos** e **Compromissos**.

## Stack

- **Backend**: Java 17, Spring Boot 3.2, Spring Data JPA, H2 Database (em memória)
- **Frontend**: React, Axios, React Router
- **Testes**: JUnit 5, Mockito

## Estrutura do Projeto

### Backend
- `Contato.java` / `Compromisso.java` — Entities JPA
- `ContatoController.java` / `CompromissoController.java` — REST Controllers
- `ContatoRepository.java` / `CompromissoRepository.java` — Repositories

### Frontend
- `ContatoList.js` / `ContatoForm.js` — CRUD de Contatos
- `CompromissoList.js` / `CompromissoForm.js` — CRUD de Compromissos
- `api.js` — Serviço HTTP (Axios)

## Endpoints da API

### Contatos
| Método | Rota | Descrição |
|--------|------|-----------|
| GET | /api/contatos | Listar todos |
| GET | /api/contatos/{id} | Buscar por ID |
| POST | /api/contatos | Criar |
| PUT | /api/contatos/{id} | Atualizar |
| DELETE | /api/contatos/{id} | Excluir |

### Compromissos
| Método | Rota | Descrição |
|--------|------|-----------|
| GET | /api/compromissos | Listar todos |
| GET | /api/compromissos/{id} | Buscar por ID |
| POST | /api/compromissos | Criar |
| PUT | /api/compromissos/{id} | Atualizar |
| DELETE | /api/compromissos/{id} | Excluir |

## Como executar

```bash
# Backend (H2 em memória, sem necessidade de banco externo)
cd backend
mvn spring-boot:run

# Frontend
cd frontend
npm install
npm start
```

O backend sobe na porta 8080. O console H2 fica disponível em http://localhost:8080/h2-console.

## Como rodar os testes

```bash
cd backend
mvn test
```

## Equipe

- **DEV 1 (Ana)** — Módulo de Contatos
- **DEV 2 (Bruno)** — Módulo de Compromissos
