# Sistema de Cadastro e Login com Flask

Este projeto é um sistema básico de cadastro e login criado com Flask, SQLite e outras ferramentas úteis como Werkzeug para segurança de senhas. Ele inclui funcionalidades de registro, login, autenticação de usuários e dashboard com sessões.

## **Tecnologias Utilizadas**

- **Flask**: Framework web Python para criar aplicações web.
- **SQLite**: Banco de dados embutido para armazenamento de usuários.
- **Werkzeug**: Utilitário para hashing de senhas e outras funcionalidades de segurança.
- **HTML**: Interface básica do sistema.

---

## **Configuração do Ambiente**

### 1. Clonar o Repositório

```bash
$ git clone https://github.com/seu_usuario/seu_repositorio.git
$ cd seu_repositorio
```

### 2. Criar Ambiente Virtual

```bash
$ python -m venv .venv
$ source .venv/bin/activate  # No Windows: .venv\Scripts\activate
```

### 3. Instalar Dependências

```bash
$ pip install -r requirements.txt
```

### 4. Criar o Banco de Dados

Crie o banco de dados SQLite com a tabela de usuários:

```sql
CREATE TABLE users (
    id INTEGER PRIMARY KEY AUTOINCREMENT,
    username TEXT UNIQUE NOT NULL,
    password TEXT NOT NULL
);
```

Para isso, execute o comando Python interativo ou use uma ferramenta como DB Browser for SQLite.

---

## **Executando o Projeto**

### Iniciar o Servidor Flask

```bash
$ flask run
```

O sistema estará disponível em: [http://127.0.0.1:5000](http://127.0.0.1:5000)

---

## **Funcionalidades**

### 1. Registro de Usuários
- Página: `/register`
- Permite criar uma nova conta inserindo um nome de usuário e senha.
- Mensagens dinâmicas são exibidas para feedback (sucesso ou erro).

### 2. Login
- Página: `/login`
- Autentica os usuários cadastrados usando nome de usuário e senha.
- Inicia uma sessão para o usuário autenticado.

### 3. Dashboard
- Página: `/dashboard`
- Exibe uma mensagem de boas-vindas ao usuário logado.
- Protegida por sessão: apenas usuários logados podem acessá-la.

### 4. Logout
- Página: `/logout`
- Encerra a sessão do usuário e redireciona para a página de login.

---

## **Estrutura do Projeto**

```plaintext
.
├── app.py                 # Código principal da aplicação Flask
├── static/                # Midias
│   ├── style.css          # Folha de estilo (vazia)
├── templates/             # Templates HTML
│   ├── login.html         # Página de login
│   ├── register.html      # Página de registro
│   ├── dashboard.html     # Página do painel do usuário
├── requirements.txt       # Dependências do projeto
└── README.md              # Documentação do projeto
```

---

## **Dependências**

As dependências estão listadas no arquivo `requirements.txt`. Para instalá-las:

```bash
$ pip install -r requirements.txt
```

Conteúdo do arquivo `requirements.txt`:

```plaintext
blinker==1.9.0
click==8.1.7
colorama==0.4.6
Flask==3.1.0
itsdangerous==2.2.0
Jinja2==3.1.4
MarkupSafe==3.0.2
Werkzeug==3.1.3
```

---

## **Melhorias Futuras**

- Implementar validações adicionais no formulário de registro.
- Adicionar funcionalidade de recuperação de senha.
- Criar estilos com CSS para melhorar a aparência das páginas.
- Usar Flask-WTF para validações mais robustas.

---

## **Contribuições**

Contribuições são bem-vindas! Sinta-se à vontade para abrir issues ou enviar pull requests no repositório.

---

## **Licença**

Este projeto está licenciado sob a [MIT License](LICENSE).

---

**Autor**: Sidney Luiz 
**Contato**: [sidneylcarneiro@gmail.com](mailto:sidneylcarneiro@gmail.com)

