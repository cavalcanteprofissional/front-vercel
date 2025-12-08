# 🐾 Adote Seu Pet - Get A Pet

Uma aplicação web moderna para facilitar a adoção de animais de estimação, conectando tutores em potencial com pets que precisam de um lar.

## 📋 Descrição do Projeto

"Adote Seu Pet" é uma plataforma desenvolvida para simplificar o processo de adoção de animais. A aplicação permite que usuários se cadastrem, façam login seguro, gerenciem seus perfis e navegam por um catálogo de pets disponíveis para adoção.

## 👥 Integrantes do Grupo 04

| Nome | Matrícula |
|------|-----------|
| ANTONIO ANASTACIO DE SOUSA SILVA | 2319190 |
| FERNANDO RICARDO RODRIGUES DA COSTA | 2317576 |
| JOHN GOES MONTEIRO | 2122704 |
| LUCAS CAVALCANTE DOS SANTOS | 2315382 |
| RAIMUNDO BRUNO GOMES SANTIAGO | 2213922 |

## 🛠️ Tecnologias Utilizadas

### Frontend
- **React 18.3.1** - Biblioteca para construção da interface
- **React Router DOM 6.25.0** - Gerenciamento de rotas e navegação
- **Axios 1.7.2** - Cliente HTTP para requisições à API
- **CSS Modules** - Estilos isolados e componentizados
- **Events 3.3.0** - Event Emitter para comunicação entre componentes
- **React Icons 5.2.1** - Biblioteca de ícones SVG

### Backend (Requisito)
- Node.js com Express
- Banco de dados (MongoDB ou similar)
- Autenticação JWT

## 📁 Estrutura do Projeto

```
frontend/
├── public/
│   └── index.html
├── src/
│   ├── assets/
│   │   └── img/                    # Imagens e logo
│   ├── components/
│   │   ├── form/
│   │   │   ├── Input.js            # Componente de input reutilizável
│   │   │   ├── Input.module.css
│   │   │   ├── Select.js           # Componente de select
│   │   │   ├── Select.module.css
│   │   │   ├── PetForm.js          # Formulário para cadastro de pets
│   │   │   └── Form.module.css
│   │   ├── Layout/
│   │   │   ├── Navbar.js           # Barra de navegação
│   │   │   ├── Navbar.module.css
│   │   │   ├── Footer.js           # Rodapé
│   │   │   ├── Footer.module.css
│   │   │   ├── Container.js        # Contenedor principal
│   │   │   ├── Container.module.css
│   │   │   ├── Message.js          # Componente de mensagens flash
│   │   │   ├── Message.module.css
│   │   │   ├── RoundedImage.js     # Imagem arredondada
│   │   │   └── RoundedImage.module.css
│   │   └── pags/
│   │       ├── Home.js             # Página inicial
│   │       ├── Auth/
│   │       │   ├── login.js        # Página de login
│   │       │   └── Register.js     # Página de registro
│   │       └── User/
│   │           ├── Profile.js      # Perfil do usuário
│   │           └── Profile.module.css
│   ├── context/
│   │   └── UserContext.js          # Context para autenticação
│   ├── hooks/
│   │   ├── useAuth.js              # Hook de autenticação
│   │   └── useFlashMessage.js      # Hook para mensagens flash
│   ├── utils/
│   │   ├── api.js                  # Configuração do Axios
│   │   └── bus.js                  # Event Emitter
│   ├── App.js                      # Componente raiz
│   ├── index.js                    # Ponto de entrada
│   └── index.css                   # Estilos globais
├── package.json
├── .gitignore
└── .env.local
```

## 🚀 Como Executar o Projeto

### Pré-requisitos
- Node.js v14 ou superior
- npm ou yarn
- Backend rodando em `http://localhost:5000`

### Instalação e Execução

1. **Navegue até a pasta frontend:**
```bash
cd frontend
```

2. **Instale as dependências:**
```bash
npm install
```

3. **Crie arquivo `.env.local` com:**
```
REACT_APP_API=http://localhost:5000
```

4. **Inicie a aplicação em modo desenvolvimento:**
```bash
npm start
```

A aplicação estará disponível em `http://localhost:3000`

### Build para Produção

```bash
npm run build
```

Gera uma build otimizada na pasta `build/`

## ✨ Funcionalidades Implementadas

### Autenticação
- ✅ Registro de novos usuários com validação
- ✅ Login seguro com JWT
- ✅ Armazenamento de token no localStorage
- ✅ Logout com limpeza de dados
- ✅ Proteção de rotas autenticadas

### Perfil do Usuário
- ✅ Visualizar dados pessoais
- ✅ Editar perfil (nome, email, telefone)
- ✅ Upload e atualização de foto de perfil
- ✅ Alteração de senha

### Interface
- ✅ Navbar responsiva com menu dinâmico
- ✅ Sistema de mensagens flash (sucesso/erro)
- ✅ Componentes de formulário reutilizáveis
- ✅ Footer com informações do projeto
- ✅ Design limpo e intuitivo

## 🔑 Componentes Principais

### Hooks Customizados

**[`useAuth`](frontend/src/hooks/useAuth.js)**
- `register(user)` - Registra novo usuário
- `login(user)` - Realiza login
- `logout()` - Faz logout do usuário
- `authenticated` - Estado de autenticação

**[`useFlashMessage`](frontend/src/hooks/useFlashMessage.js)**
- `setFlashMessage(msg, type)` - Exibe mensagem temporária

### Context

**[`UserContext`](frontend/src/context/UserContext.js)**
- Fornece dados de autenticação globalmente
- Integra com hooks de autenticação

### Utilitários

**[`api`](frontend/src/utils/api.js)** - Cliente Axios pré-configurado
- Base URL: `http://localhost:5000`
- Headers padrão com autenticação

**[`bus`](frontend/src/utils/bus.js)** - Event Emitter
- Comunicação entre componentes
- Gerenciamento de eventos globais

## 📄 Páginas Disponíveis

| Rota | Descrição | Autenticação |
|------|-----------|--------------|
| `/` | Catálogo de pets | Pública |
| `/login` | Login de usuários | Pública |
| `/register` | Registro de novos usuários | Pública |
| `/user/profile` | Perfil do usuário | Protegida |

## 🎨 Paleta de Cores

```css
Primária:    #16479d (Azul)
Secundária:  #FFD400 (Amarelo)
Sucesso:     #25b456 (Verde)
Erro:        #721c24 (Vermelho)
```

## 📦 Dependências do Projeto

```json
{
  "react": "^18.3.1",
  "react-dom": "^18.3.1",
  "react-router-dom": "^6.25.0",
  "axios": "^1.7.2",
  "events": "^3.3.0",
  "react-icons": "^5.2.1",
  "react-scripts": "5.0.1"
}
```

## 🔐 Segurança

- 🔒 Autenticação com JWT tokens
- 🔒 Tokens armazenados no localStorage
- 🔒 Headers de autorização nas requisições
- 🔒 Validação de token em rotas protegidas
- 🔒 Upload seguro de imagens

## 📝 Scripts NPM

```bash
npm start          # Inicia em modo desenvolvimento (porta 3000)
npm run build      # Cria build otimizado para produção
npm test           # Executa testes
npm run eject      # Eject do create-react-app (irreversível)
```

## 🐛 Possíveis Melhorias Futuras

- [ ] Testes automatizados (Jest + React Testing Library)
- [ ] PWA (Progressive Web App)
- [ ] Filtros avançados de busca de pets
- [ ] Paginação do catálogo
- [ ] Integração com redes sociais
- [ ] Sistema de notificações push
- [ ] Modo escuro (Dark Mode)
- [ ] Internacionalização (i18n)
- [ ] Otimização de imagens
- [ ] Cache de dados

## 📄 Licença

Projeto desenvolvido para fins educacionais - UNIFOR.

## 📧 Contato

Para dúvidas ou sugestões sobre o projeto, entre em contato com os desenvolvedores através do repositório GitHub.

---

**Desenvolvido com ❤️ pelo Grupo 04 - UNIFOR**

*Última atualização: 2024*
