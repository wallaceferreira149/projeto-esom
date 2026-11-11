# projeto-esom

Monorepo do projeto ESOM. Contém a API e o frontend web em um único
repositório, com documentação centralizada na raiz.

## Estrutura

```
.
├── api-esom/          API — Spring Boot 4 / Java 21 / Maven
├── web-esom/          Frontend web
├── docs/              Documentação centralizada do projeto
├── .agents/skills/    Skills de agentes (escopo do projeto)
└── skills-lock.json   Lockfile das skills instaladas
```

## api-esom

API REST em Spring Boot 4.1 (Java 21), com Spring Data JPA, Bean Validation
e H2 Console para desenvolvimento.

```bash
cd api-esom
./mvnw spring-boot:run     # sobe a aplicação
./mvnw verify              # build + testes
```

## web-esom

Frontend web. Stack e comandos a definir no scaffold inicial.

## Convenções

- **Commits** usam escopo por área: `api: ...`, `web: ...`, `docs: ...`
- **Tags de release** são independentes por parte: `api-vX.Y.Z`, `web-vX.Y.Z`
- **Um único repositório**, com CI separado por path:
  - `.github/workflows/api.yml` → `api-esom/**`
  - `.github/workflows/web.yml` → `web-esom/**`

## Documentação

Toda a documentação do projeto vive em [`docs/`](docs/).