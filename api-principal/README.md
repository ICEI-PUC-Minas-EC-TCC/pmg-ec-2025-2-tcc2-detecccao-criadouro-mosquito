# API Principal - Detecção de Criadouros

Este projeto backend tem como objetivo integrar os sistemas frontend (aplicativo móvel e portal web) e o sistema de detecção de criadouros. Este trabalho faz parte do Trabalho de Conclusão de Curso (TCC) em Engenharia de Computação da Pontifícia Universidade Católica de Minas Gerais (PUC Minas).

## ℹ️ Informações Técnicas

API REST construída com **FastAPI**, **SQLAlchemy** e **Pydantic** para dar suporte ao portal web e ao aplicativo móvel. Ela expõe endpoints para gerenciamento de usuários (administradores do portal e cidadãos), campanhas e processamento dos resultados de detecção.

## 📁 Estrutura do Projeto

```
deteccaomosquito/
|-- app/
|   |-- config.py           # Configurações e variáveis de ambiente
|   |-- database.py         # Conexão com banco de dados
|   |-- main.py             # Ponto de entrada da aplicação
|   |-- models/             # Modelos do SQLAlchemy (Tabelas)
|   |   |-- campaign.py
|   |   |-- user.py
|   |   `-- userPortal.py
|   |-- routers/            # Rotas da API
|   |   |-- campaign.py
|   |   |-- user.py
|   |   `-- userPortal.py
|   |-- schemas/            # Schemas do Pydantic (Validação)
|   |   |-- campaign.py
|   |   |-- user.py
|   |   `-- userPortal.py
|   `-- services/           # Lógica de negócio
|       |-- campaign_service.py
|       |-- user_service.py
|       `-- userPortal_service.py
|-- requirements.txt
`-- README.md
```

## 📋 Requisitos

- Python 3.13+
- `pip`

## ⚙️ Configuração e Instalação

1.  Crie um ambiente virtual:
    ```bash
    python -m venv .venv
    ```

2.  Ative o ambiente:
    - **Windows PowerShell:**
      ```bash
      .venv\Scripts\Activate.ps1
      ```
    - **macOS/Linux:**
      ```bash
      source .venv/bin/activate
      ```

3.  Instale as dependências:
    ```bash
    pip install -r requirements.txt
    ```

4.  Configure as variáveis de ambiente no arquivo `.env`. Exemplos:
    ```bash
    # SQLite (apenas para desenvolvimento)
    DATABASE_URL=sqlite:///./meubanco.db

    # PostgreSQL (produção)
    # Consulte a página 'Configurações de Ambiente' no Notion para a URL correta
    DATABASE_URL=postgresql://user:password@host/dbname
    ```

## ▶️ Executando a API

Inicie o servidor FastAPI com o Uvicorn:

```bash
uvicorn app.main:app --reload
```

Uma vez em execução, a documentação interativa da API estará disponível em `http://localhost:8000/docs` ou `http://localhost:8000/swagger`.

## 🔒 Notas de Segurança

-   Senhas de usuários e administradores são armazenadas utilizando hashes bcrypt (`UserService` / `UserPortalService`).
-   Endereços de e-mail são únicos em suas respectivas tabelas (`user.email` e `user_portal.email`).

## 🗄️ Notas sobre Banco de Dados

-   As tabelas são geradas automaticamente na inicialização quando se utiliza as migrações do SQLAlchemy em ambiente de desenvolvimento.

## 🔗 Principais Endpoints

Consulte a documentação em `/docs` ou `/swagger` para o contrato completo de todas as rotas.
