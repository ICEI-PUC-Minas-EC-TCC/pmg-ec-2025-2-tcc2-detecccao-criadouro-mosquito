# Sistema de Detecção de Potenciais Criadouros de Mosquito Aedes aegypti

Este projeto compõe o Trabalho de Conclusão de Curso (TCC) do curso de Engenharia de Computação da Pontifícia Universidade Católica de Minas Gerais (PUC Minas). O objetivo é fornecer uma solução integrada para auxiliar no combate ao mosquito Aedes aegypti através da detecção automática de focos de reprodução em imagens.

O sistema utiliza inteligência artificial (YOLOv12) e visão computacional para identificar objetos como caixas d'água, pneus, garrafas e outros recipientes que possam acumular água parada.

## 🔗 Recursos Principais (Links Rápidos)

Abaixo estão os links para os recursos mencionados no artigo do TCC:

| Recurso | Descrição | Link |
| :--- | :--- | :--- |
| **Portal Web** | Painel de gestão para visualização de focos e campanhas. | [Acessar Portal](https://deteccao-criadouro.web.app/) |
| **Aplicativo Android (APK)** | Aplicativo para envio de denúncias e análise de imagens. | [Baixar APK](https://drive.google.com/file/d/1HOnxv3qVMAGiNVke45Xuy1oZMFLGCYxv/view?usp=sharing) |
| **Artigo PDF** | Documento completo do Trabalho de Conclusão de Curso. | [Acessar artigo](https://drive.google.com/file/d/1GJVAG7F7XILGYWyt1tKXGRE7BBhv--57/view?usp=drive_link) |

## 🏗️ Componentes do Projeto

O sistema é dividido em microsserviços e aplicações independentes. Consulte o README de cada componente para detalhes de instalação e execução.

### [📱 Aplicativo Mobile (React Native)](aplicativo-mobile/README.md)
Aplicativo para cidadãos capturarem imagens, visualizarem detecções em tempo real e participarem de campanhas de saúde.
*   **Tecnologias**: React Native, Expo, TypeScript.

### [💻 Portal Web (Vue/React/Vanilla)](portal-web/README.md)
Painel administrativo para gestores monitorarem as ocorrências em um mapa interativo e gerenciarem campanhas.
*   **Tecnologias**: HTML5, CSS3, JavaScript, Firebase Hosting.

### [⚙️ API Principal (FastAPI)](api-principal/README.md)
Backend central que gerencia usuários, autenticação, campanhas e orquestra os dados entre os aplicativos e o banco de dados.
*   **Tecnologias**: Python, FastAPI, SQLAlchemy, PostgreSQL.

### [🧠 Serviço de Detecção (YOLO)](servico-deteccao/README.md)
Serviço especializado responsável por processar as imagens e executar o modelo de Inteligência Artificial para identificar criadouros.
*   **Tecnologias**: Python, YOLOv12, OpenCV.

### [🗄️ Base de Dados](base-dados/README.md)
Scripts e definições de infraestrutura para o banco de dados e armazenamento.

## 👥 Autores

*   **Davidson Marra Rodrigues Vieira**
*   **Gustavo Valadares Castro**
*   **Matheus Santos Ferreira Costa**
*   **Pedro Henrique Teixeira de Souza**
*   **Rafael Henrique da Rocha Silva**

**Orientador:** Prof. Felipe Augusto Lara Soares

---
*Pontifícia Universidade Católica de Minas Gerais - 2025*
