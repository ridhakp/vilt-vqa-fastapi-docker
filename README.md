# Vision-and-Language Transformer (ViLT) for VQA using FastAPI

This project demonstrates how to set up a Vision-and-Language Transformer (ViLT) model fine-tuned on VQAv2 using FastAPI. The model can answer questions about the content of an image.


## Installation

1. **Clone the repository:**

    ```bash
    git clone https://github.com/ridhakp/vilt-vqa-fastapi-docker.git
    cd vilt-vqa-fastapi-docker
    ```

2. **Create and activate a virtual environment:**

    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows use `venv\Scripts\activate`
    ```

3. **Install the required packages:**

    ```bash
    pip install -r requirements.txt
    ```

## Usage

1. **Run the FastAPI application:**

    ```bash
    uvicorn main:app --reload
    ```

2. **Open your browser and navigate to the Swagger UI:**

    ```
    http://localhost:8000/docs
    ```

3. **Ask a question about an image:**

    - Write your question in the `text` field.
    - Upload an image.
    - Click "Execute" to get the answer.

## Dockerization

1. **Build and run the Docker container:**

    ```bash
    docker compose up --build
    ```

2. **Access the application via Docker:**

    ```
    http://localhost:8000/docs
    ```

## Endpoints

- **GET /**: Returns a welcome message.
- **POST /ask**: Takes a question and an image, returns the answer.

## Example

1. **Upload an image and ask a question:**

    - **Question**: "How many cats are there?"
    - **Image**: (Upload an image with cats)

2. **Response**:

    ```json
    {
        "answer": "2"
    }
    ```


