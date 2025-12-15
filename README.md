# Easy Scheduling 🗓️

Um aplicativo web moderno para agendamento de reuniões, com integração direta ao Google Calendar. Permite que usuários criem perfis, definam horários disponíveis e agendem reuniões que são automaticamente inseridas no calendário do Google.

## 🚀 Funcionalidades

- **Registro de Usuários**: Crie um perfil personalizado com nome, bio e avatar.
- **Definição de Horários Disponíveis**: Configure intervalos de tempo por dia da semana.
- **Agendamento de Reuniões**: Visualize calendários e agende reuniões com confirmação.
- **Integração com Google Calendar**: Conecte sua conta Google para inserir eventos automaticamente no calendário.
- **Autenticação Segura**: Login via NextAuth com suporte a provedores OAuth.
- **Interface Responsiva**: Design moderno e intuitivo, otimizado para desktop e mobile.

## 🛠️ Tecnologias Utilizadas

- **Frontend**: Next.js 14, React, TypeScript
- **Backend**: Next.js API Routes
- **Banco de Dados**: MySQL com Prisma ORM
- **Autenticação**: NextAuth.js
- **Integração Google**: Google Calendar API
- **Estilização**: Styled Components
- **Outros**: Axios, React Query, Day.js

## 📋 Pré-requisitos

- Node.js (versão 18 ou superior)
- npm ou yarn
- Conta Google (para integração com Calendar)
- Docker (para rodar MySQL localmente)

## 🔧 Instalação e Configuração

### 1. Clone o repositório

```bash
git clone https://github.com/seu-usuario/easy-scheduling.git
cd easy-scheduling
```

### 2. Instale as dependências

```bash
npm install
```

### 3. Configure o banco de dados

#### Opção A: Usando Docker (Recomendado)

```bash
docker run --name easy-scheduling -e MYSQL_ROOT_PASSWORD=docker -p 3306:3306 mysql:latest
docker start easy-scheduling
```

#### Opção B: MySQL local

Certifique-se de ter o MySQL instalado e configure a variável de ambiente `DATABASE_URL` no arquivo `.env`.

### 4. Configure as variáveis de ambiente

Crie um arquivo `.env.local` na raiz do projeto com as seguintes variáveis:

```env
DATABASE_URL="mysql://root:docker@localhost:3306/easy_scheduling"
NEXTAUTH_SECRET="sua-chave-secreta-aqui"
NEXTAUTH_URL="http://localhost:3000"
GOOGLE_CLIENT_ID="seu-google-client-id"
GOOGLE_CLIENT_SECRET="seu-google-client-secret"
```

### 5. Execute as migrações do banco de dados

```bash
npx prisma migrate dev
```

### 6. Gere o cliente Prisma

```bash
npx prisma generate
```

## 🚀 Executando o Projeto

```bash
npm run dev
```

O aplicativo estará disponível em [http://localhost:3000](http://localhost:3000).

## 📊 Visualizando o Banco de Dados

Para visualizar e gerenciar os dados do banco:

```bash
npx prisma studio
```

Isso abrirá o Prisma Studio em seu navegador.

## 🎨 Design

O design do projeto pode ser visualizado no Figma:  
[Figma](https://www.figma.com/design/MAcKkY0lCYpwVfsWP0bpcl/Ignite-Call--Community-?node-id=339-74&p=f&t=yUftVXF8v81kMFGd-0)

## 📄 Licença

Este projeto está sob a licença MIT. Veja o arquivo [LICENSE](LICENSE) para mais detalhes.

---

Se você tiver alguma dúvida ou sugestão, entre em contato e sinta-se à vontade para contribuir !

<img align="left" src="https://avatars.githubusercontent.com/renyzeraa?size=100">

Feito por [Renan L. Silva](https://github.com/renyzeraa)! <br>
🛠 Dev. Frontend <br>
📍 Santa Catarina - Brasil <br>

<a href="https://www.linkedin.com/in/renyzeraa" target="_blank"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=flat&logo=linkedin&logoColor=white" alt="LinkedIn Badge" height="20"></a>&nbsp;
<a href="mailto:renansilvaytb@gmail.com" target="_blank"><img src="https://img.shields.io/badge/Gmail-D14836?style=flat&logo=gmail&logoColor=white" alt="Gmail Badge" height="20"></a>&nbsp;
<a href="#"><img src="https://img.shields.io/badge/Discord-%237289DA.svg?logo=discord&logoColor=white" title="renan_s#7826" alt="Discord Badge" height="20"></a>&nbsp;
<a href="https://www.github.com/renyzeraa" target="_blank"><img src="https://img.shields.io/badge/GitHub-100000?style=flat&logo=github&logoColor=white" alt="GitHub Badge" height="20"></a>&nbsp;

<br clear="left"/>
