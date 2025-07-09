# NLW Agents - Rocketseat

Projeto desenvolvido durante o NLW (Next Level Week) da Rocketseat, focado em criar um sistema de agentes inteligentes.

## 🛠 Tecnologias e versões principais

- **Node.js 20+**: Ambiente de execução JavaScript server-side
- **TypeScript 5+**: Superset tipado do JavaScript
- **Drizzle ORM 0.29+**: ORM moderno para bancos relacionais
- **PostgreSQL 17**: Banco de dados relacional (rodando via Docker)
- **Fastify**: Framework web rápido para Node.js (servidor HTTP)
- **Zod**: Biblioteca para validação de dados com TypeScript
- **Biome 1.5+**: Ferramenta para formatação e linting de código

## 🗄 Estrutura do banco de dados

O projeto utiliza PostgreSQL com as seguintes tabelas principais:
- `rooms`: Armazena informações das salas/ambientes dos agentes
- Migrações gerenciadas via Drizzle ORM


## 🚀 Setup do projeto

### Pré-requisitos
- Node.js 20+ instalado
- Docker e Docker Compose instalados
- PostgreSQL 17 (opcional, pode usar o container Docker)

### Passo a passo
1. Clone o repositório:
```bash
git clone https://github.com/matheuszarpellon/NLWAgents-Server.git
cd NLWAgents-Server/server
```

2. Instale as dependências:
```bash
npm install
```

3. Configure as variáveis de ambiente:
```bash
cp .env.example .env
# Edite o .env com suas configurações
```

4. Inicie os containers Docker:
```bash
docker-compose up -d
```

5. Execute as migrações do banco de dados:
```bash
npm run db:migrate
```

6. Inicie o servidor de desenvolvimento:
```bash
npm run dev
```

## 💻 Comandos úteis

- `npm run dev`: Inicia o servidor em modo desenvolvimento (hot-reload)
- `npm run build`: Compila o projeto TypeScript
- `npm run db:migrate`: Executa as migrações do banco de dados
- `npm run db:seed`: Executa os seeds do banco de dados
- `npm run format`: Formata o código usando Biome
- `npm run lint`: Verifica problemas de linting

## 🌐 Rotas disponíveis

- `GET /rooms`: Lista todas as salas disponíveis
- Consultar `client.http` para exemplos de requisições

## 🐳 Ambiente Docker

O projeto inclui configuração para:
- PostgreSQL
- Configurações básicas no `docker-compose.yml`

## 🤝 Como contribuir

1. Faça um fork do projeto
2. Crie uma branch para sua feature (`git checkout -b feature/fooBar`)
3. Commit suas mudanças (`git commit -am 'Add some fooBar'`)
4. Push para a branch (`git push origin feature/fooBar`)
5. Abra um Pull Request
