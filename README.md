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

## 📊 Resultados do Modelo

O modelo de detecção YOLOv12 foi treinado com uma base de dados diversificada e alcançou os seguintes resultados:

| Métrica      | Resultado |
| ------------ | --------- |
| **Precisão** | 83,93%    |
| **Recall**   | 61,04%    |
| **F1-Score** | 70,68%    |
| **mAP50**    | 74,8%     |
| **mAP75**    | 66,44%    |
| **mAP50-95** | 57,78%    |

### Base de Dados de Treinamento

| Dataset | Total de imagens | Treino | Validação | Testes |
| :--- | :--- | :--- | :--- | :--- |
| MosquitoFusion | 200 | 100 (50%) | 60 (30%) | 40 (20%) |
| Imagens dos autores | 55 | 33 (60%) | 11 (20%) | 11 (20%) |
| Gemini 3 Pro | 293 | 293 (100%) | 0 (0%) | 0 (0%) |
| **Total** | **548** | **426 (77,73%)** | **71 (12,96%)** | **51 (9,31%)** |
| **Total aumentado** | **974** | **852 (87,47%)** | **71 (7,29%)** | **51 (5,24%)** |

*Tabela 2 – Composição das bases de dados. Fonte: Elaborado pelos autores*

### Técnicas de Aumento de Dados

- Espelhamento horizontal
- Rotação
- Transformação afim
- Ajuste de brilho e contraste
- Ajuste de saturação

## 👥 Autores

*   **Davidson Marra Rodrigues Vieira** - davidsonmarra@gmail.com
*   **Gustavo Valadares Castro** - tcc2025@gvcastro.com
*   **Matheus Santos Ferreira Costa** - matheussantosfcosta@gmail.com
*   **Pedro Henrique Teixeira de Souza** - phtsouza@gmail.com
*   **Rafael Henrique da Rocha Silva** - rafaelehnrq@gmail.com

**Orientador:** Prof. Felipe Augusto Lara Soares - felipesoares@pucminas.br

---
*Pontifícia Universidade Católica de Minas Gerais - 2025*
