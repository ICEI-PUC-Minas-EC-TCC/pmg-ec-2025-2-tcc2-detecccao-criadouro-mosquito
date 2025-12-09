# Serviço de Detecção de Criadouros (YOLOv12)

Este microsserviço é responsável pelo processamento de imagens e execução do modelo de inteligência artificial para detecção de focos de reprodução do mosquito *Aedes aegypti*.

Ele utiliza a biblioteca **Ultralytics YOLO** e **OpenCV** para inferência e manipulação de imagens.

## 🚀 Funcionalidades

*   **Detecção de Objetos**: Identifica potenciais criadouros em imagens enviadas.
*   **Processamento de Imagem**: Redimensiona e normaliza imagens para o modelo.
*   **Anotação**: Gera uma nova versão da imagem com os bounding boxes desenhados (em vermelho) sobre os objetos detectados.
*   **Contagem**: Retorna a contagem precisa de focos encontrados.

## 🛠️ Tecnologias

*   **Python 3.10+**
*   **FastAPI**: Framework web de alta performance.
*   **Ultralytics YOLO**: Implementação do modelo YOLOv12.
*   **OpenCV**: Processamento de imagens.
*   **Google Cloud Storage**: Integração para download de modelos e persistência.

## 📦 Instalação

1.  Crie um ambiente virtual:
    ```bash
    python -m venv venv
    source venv/bin/activate  # Linux/Mac
    # ou
    venv\Scripts\activate  # Windows
    ```

2.  Instale as dependências:
    ```bash
    pip install -r requirements.txt
    ```

## ⚙️ Configuração

O serviço verifica automaticamente a presença do modelo YOLO. Se não encontrado localmente, ele tentará baixá-lo a partir da URL configurada em `YOLO_MODEL_URL`.

Certifique-se de configurar as variáveis de ambiente necessárias (consulte `.env.example` se disponível ou o código em `app/config.py`).

## ▶️ Execução

Para iniciar o servidor de desenvolvimento:

```bash
uvicorn app.main:app --reload
```

O serviço estará disponível em `http://localhost:8000` (ou porta configurada).
