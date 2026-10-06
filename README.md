# 🛋️ CasaBela — Catálogo Online de Móveis

Um sistema web desenvolvido para a loja **CasaBela**, com foco na apresentação de um catálogo online de móveis. O projeto permite a visualização geral dos itens disponíveis e navegação detalhada por produto, além de interface de administração para gerenciamento do acervo.

> **Projeto Acadêmico / Prático**  
> Desenvolvido para a disciplina de **Frameworks Back-End**, utilizando **Django**.

- [x] **Catálogo Geral:** Listagem de móveis com filtro e suporte a imagens/thumbnails.
- [x] **Página de Detalhes:** Exibição completa de informações do móvel (descrição, dimensões, material, preço, fotos).
- [x] **Painel Administrativo:** Interface do Django Admin para criação, edição e remoção de produtos e categorias.
- [x] **Navegação Responsiva:** Layout adaptável para dispositivos móveis e desktops.

---

## 📌 Funcionalidades Requisitadas e Implementadas

1. **Estrutura Django:** Projeto Django (`casabela`) configurado com a aplicação `moveis`.
2. **Modelo de Dados (`Movel`):** Implementação do model no `models.py` e execução das respetivas migrações (`makemigrations` e `migrate`).
3. **Painel de Administração:** Registo do modelo no `admin.py` e cadastro de pelo menos 8 móveis de exemplo através do Django Admin.
4. **Listagem Geral (`index.html`):** View que procura todos os registos (`Model.objects.all()`) e exibe-os numa tabela HTML com colunas para cada campo.
5. **Página de Detalhes (`detalhe.html`):** Rota dinâmica (`/moveis/<int:id>`) e view que obtém um único registo (`Model.objects.get(id=id)`) exibindo todos os seus dados.
6. **Navegação Dinâmica:** Links nos nomes dos itens da tabela a redirecionar para a página de detalhes através da tag `{% url %}`.
7. **Estilização Personalizada:** Aplicação de ficheiro de estilos estático (`static/css/estilos.css`) nas páginas do projeto.
8. **Imagens Estáticas:** Inclusão de imagens em `static/imagens/` exibidas nos templates utilizando a tag `{% static %}`.
9. **Ficheiro JavaScript:** Script em `static/js/script.js` com função executada via botão no template.
10. **Testes de Ambiente:** Testes de funcionamento em modo de desenvolvimento (`DEBUG = True`) e produção (`DEBUG = False`, com execução prévia do `collectstatic`).

---

## 🛠️ Tecnologias 

- **Linguagem:** Python 3.x
- **Framework Back-End:** Django
- **Banco de Dados:** SQLite (Desenvolvimento)
- **Front-End:** HTML5, CSS3 / Bootstrap
- **Gerenciamento de Dependências:** `pip` / `venv`

---

## 🗃️ Especificação do Model `Movel`

O modelo `Movel` foi definido em `moveis/models.py` com os seguintes campos:

| Campo | Tipo | Descrição |
| :--- | :--- | :--- |
| `nome` | `CharField` | Nome do móvel |
| `preco` | `DecimalField` | Preço de venda |
| `estoque` | `IntegerField` | Quantidade em estoque |
| `material` | `CharField` | Material (ex.: madeira, metal, mdf) |

---

## 📁 Estrutura de Ficheiros

```text
projeto_moveis/
│
├── casabela/                      # Configurações globais do projeto Django
│   ├── __init__.py                # Indica que o diretório é um pacote Python
│   ├── asgi.py                    # Configuração para servidores ASGI
│   ├── settings.py                # Configurações do projeto (apps, DB, static)
│   ├── urls.py                    # Roteamento de URLs principais do projeto
│   └── wsgi.py                    # Configuração para servidores WSGI
│
├── moveis/                        # App principal do catálogo de móveis
│   ├── migrations/                # Histórico de migrações da base de dados
│   │   └── 0001_initial.py        # Migração inicial das tabelas
│   │
│   ├── static/                    # Ficheiros estáticos da aplicação
│   │   ├── css/
│   │   │   └── estilos.css        # Estilização personalizada do catálogo
│   │   ├── imagens/               # Imagens estáticas do projeto
│   │   └── js/
│   │       └── script.js          # Interações JavaScript
│   │
│   ├── templates/
│   │   └── moveis/                # Templates HTML da aplicação
│   │       ├── index.html         # Tabela de listagem geral
│   │       └── detalhe.html       # Página de detalhes do item
│   │
│   ├── admin.py                   # Registo e personalização do Django Admin
│   ├── apps.py                    # Configuração da aplicação 'moveis'
│   ├── models.py                  # Definição do modelo Movel
│   ├── tests.py                   # Testes automatizados da aplicação
│   ├── urls.py                    # Rotas internas do app 'moveis'
│   └── views.py                   # Regras de negócio e renderização
│
├── db.sqlite3                     # Base de dados SQLite de desenvolvimento
├── manage.py                      # Utilitário de linha de comandos do Django
└── README.md                      # Documentação do repositório
Aqui está um **README.md** profissional, bem estruturado e completo para o repositório do seu projeto.

---

```markdown
# 🛋️ CasaBela — Catálogo Online de Móveis

Um sistema web desenvolvido para a loja **CasaBela**, com foco na apresentação de um catálogo online de móveis. O projeto permite a visualização geral dos itens disponíveis e navegação detalhada por produto, além de interface de administração para gerenciamento do acervo.

> **Projeto Acadêmico / Prático**  
> Desenvolvido para a disciplina de **Frameworks Back-End**, utilizando **Django**.

---

## 📌 Funcionalidades

- [x] **Catálogo Geral:** Listagem de móveis com filtro e suporte a imagens/thumbnails.
- [x] **Página de Detalhes:** Exibição completa de informações do móvel (descrição, dimensões, material, preço, fotos).
- [x] **Painel Administrativo:** Interface do Django Admin para criação, edição e remoção de produtos e categorias.
- [x] **Navegação Responsiva:** Layout adaptável para dispositivos móveis e desktops.

---

## 🛠️ Tecnologias Utilizadas

- **Linguagem:** Python 3.x
- **Framework Back-End:** Django
- **Banco de Dados:** SQLite (Desenvolvimento)
- **Front-End:** HTML5, CSS3 / Bootstrap
- **Gerenciamento de Dependências:** `pip` / `venv`

---

## 📁 Estrutura do Projeto

```text
projeto_moveis/
│
├── casabela/                      # Configurações globais do projeto Django
│   ├── __init__.py                # Indica que o diretório é um pacote Python
│   ├── asgi.py                    # Configuração para servidores ASGI
│   ├── settings.py                # Configurações do projeto (apps, DB, static)
│   ├── urls.py                    # Roteamento de URLs principais do projeto
│   └── wsgi.py                    # Configuração para servidores WSGI
│
├── moveis/                        # App principal do catálogo de móveis
│   ├── migrations/                # Histórico de migrações do banco de dados
│   │   └── 0001_initial.py        # Migração inicial das tabelas
│   │
│   ├── static/                    # Arquivos estáticos da aplicação
│   │   ├── css/
│   │   │   └── estilos.css        # Estilização personalizada do catálogo[cite: 8]
│   │   ├── imagens/               # Imagens estáticas do projeto[cite: 8]
│   │   └── js/
│   │       └── script.js          # Scripts e interações do front-end[cite: 8]
│   │
│   ├── templates/
│   │   └── moveis/                # Templates HTML da aplicação
│   │       ├── index.html         # Tabela de listagem geral[cite: 8]
│   │       └── detalhe.html       # Página de detalhes do item[cite: 8]
│   │
│   ├── admin.py                   # Registro e personalização do Django Admin[cite: 8]
│   ├── apps.py                    # Configuração da aplicação 'moveis'
│   ├── models.py                  # Definição do modelo Movel[cite: 8]
│   ├── tests.py                   # Testes automatizados da aplicação
│   ├── urls.py                    # Rotas internas do app 'moveis'
│   └── views.py                   # Regras de negócio e renderização das views[cite: 8]
│
├── db.sqlite3                     # Banco de dados SQLite de desenvolvimento
├── manage.py                      # Script CLI para comandos do Django
└── README.md                      # Documentação do repositório

```
