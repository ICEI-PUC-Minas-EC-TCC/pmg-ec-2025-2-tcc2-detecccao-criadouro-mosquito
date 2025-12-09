# Bases de Dados e Dataset

Este diretório contém referências para os dados utilizados no treinamento do modelo de Inteligência Artificial e scripts relacionados à infraestrutura de dados do projeto.

## 📊 Dataset de Imagens

O dataset utilizado para treinar o modelo YOLOv12 é composto por imagens de diversas fontes, incluindo:

*   **MosquitoFusion Dataset**
*   **Coletas Próprias** (Imagens reais de quintais e terrenos)
*   **Imagens Sintéticas** (Geradas via IA Generativa para aumentar a variabilidade)

### Acesso aos Dados

As bases de dados completas, incluindo anotações e divisões de treino/teste, estão disponíveis no Google Drive:

📂 **[Acessar Base de Dados no Google Drive](https://drive.google.com/drive/folders/1Gj5bC2j5OVy_PD2sf3Vgn5SjbJpMNcJb?usp=sharing)**

## 🗄️ Estrutura de Banco de Dados

O sistema utiliza **PostgreSQL** (via Google Cloud SQL em produção) para armazenar:
*   Dados de usuários
*   Campanhas de saúde
*   Registros de detecções e metadados das imagens

Os scripts de migração e definição de tabelas (SQLAlchemy/Alembic) encontram-se no diretório da [API Principal](../api-principal).
