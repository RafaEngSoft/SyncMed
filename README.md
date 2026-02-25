# SyncMed 🏥

> Plataforma de gerenciamento de plantões médicos — conectando hospitais e médicos de forma simples e eficiente.

---

## 📋 Sobre o Projeto

O **SyncMed** é uma aplicação web desenvolvida com **Angular 19** que facilita o gerenciamento e a negociação de plantões médicos. A plataforma oferece painéis dedicados para administradores de hospitais e médicos, permitindo o controle completo de escalas, disponibilidade e troca de plantões.

---

## ✨ Funcionalidades

### 👨‍💼 Administrador
- Visualização de dashboard com resumo de plantões
- Gerenciamento completo de plantões (criar, editar, remover)
- Controle de escalas por especialidade e unidade

### 👨‍⚕️ Médico
- Dashboard pessoal com plantões agendados
- Visualização da própria escala
- Marketplace para troca e aquisição de plantões disponíveis

### 🔐 Autenticação
- Login e cadastro de usuários
- Rotas protegidas por `AuthGuard` (Angular Route Guards)
- Persistência de sessão via `localStorage`

---

## 🚀 Tecnologias

| Tecnologia | Versão |
|---|---|
| [Angular](https://angular.io/) | 19.2.6 |
| [TypeScript](https://www.typescriptlang.org/) | ~5.6.2 |
| [RxJS](https://rxjs.dev/) | ~7.8.0 |
| Angular Router | 19.2.6 |
| Angular Forms | 19.2.6 |

---

## 📁 Estrutura do Projeto

```
SyncMed/
└── SyncMed/
    └── src/
        ├── components/
        │   ├── admin-dashboard/      # Painel do administrador
        │   ├── admin-shifts/         # Gerenciamento de plantões (admin)
        │   ├── doctor-dashboard/     # Painel do médico
        │   ├── doctor-schedule/      # Escala do médico
        │   ├── doctor-marketplace/   # Marketplace de plantões
        │   ├── auth/                 # Login e Registro
        │   ├── header/               # Cabeçalho global
        │   └── landing/              # Página inicial
        ├── guards/
        │   └── auth.guard.ts         # Proteção de rotas
        ├── services/
        │   └── shift.service.ts      # Serviço de plantões (localStorage)
        ├── app.routes.ts             # Configuração de rotas
        └── main.ts                   # Bootstrap da aplicação
```

---

## ⚙️ Como Executar Localmente

### Pré-requisitos
- [Node.js](https://nodejs.org/) (v18 ou superior)
- [Angular CLI](https://angular.io/cli): `npm install -g @angular/cli`

### Instalação

```bash
# Clone o repositório
git clone https://github.com/seu-usuario/SyncMed.git

# Entre na pasta do projeto Angular
cd SyncMed/SyncMed

# Instale as dependências
npm install

# Inicie o servidor de desenvolvimento
npm start
```

Acesse em: **http://localhost:4200**

### Build para produção

```bash
npm run build
```

---

## 🗺️ Rotas da Aplicação

| Rota | Componente | Acesso |
|---|---|---|
| `/` | Landing Page | Público |
| `/login` | Login | Público |
| `/register` | Cadastro | Público |
| `/admin/dashboard` | Admin Dashboard | 🔒 Autenticado |
| `/admin/shifts` | Gerenciar Plantões | 🔒 Autenticado |
| `/doctor/dashboard` | Doctor Dashboard | 🔒 Autenticado |
| `/doctor/schedule` | Minha Escala | 🔒 Autenticado |
| `/doctor/marketplace` | Marketplace | 🔒 Autenticado |

---

## 📄 Licença

Este projeto está sob a licença MIT. Consulte o arquivo [LICENSE](LICENSE) para mais detalhes.

---

<p align="center">Feito com ❤️ por Rafael Aráujo</p>
