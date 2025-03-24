# Emotional chatbot

## Demo

Question:

`"My dog died last week. I am feeling void. What should I do?"`

- Plain answer:

![Screenshot from 2025-03-24 13-29-36](https://github.com/user-attachments/assets/9b7f594e-21eb-466c-b622-876813881818)

- Answer after applying the techniques:


![Screenshot from 2025-03-24 13-27-37](https://github.com/user-attachments/assets/f6f58ea6-c418-4ee9-b14b-bb388699aa43)


## Objective

1. Develop an emotion-aware demonstration ranking framework that optimizes in context learning for ESC. 
2. Implement a ranking-based selection mechanism to prioritize emotionally relevant demonstrations. 
3. Enhance contextual coherence and personalization in ESC using retrieval augmented generation (RAG). 
4. Improve low-resource NLP adaptability by refining demonstration selection for better model performance.


# How to run the application.

Make sure you have docker installed. Now install the qdrant client through docker and run it locally.

The docs can be found here : https://qdrant.tech/documentation/quickstart/

```bash
docker pull qdrant/qdrant
```

```bash
docker run -p 6333:6333 -p 6334:6334 \
    -v "$(pwd)/qdrant_storage:/qdrant/storage:z" \
    qdrant/qdrant
```

If you are able to see the following dashboard in your browser then its a success:

```bash
http://localhost:6333/dashboard#/collections
```

Install and run any model from ollama family. The docs can be found here: https://ollama.com/library

```bash
ollama run llama3.1
```

Make sure you have uv package manager installed. If you are using Linux you can install using the following command:

```bash
curl -LsSf https://astral.sh/uv/install.sh | sh
```

The installation can be found here in case of errors: https://astral.sh/blog/uv.

# Run the code

Pull the repository.

```bash
git clone https://github.com/asifrahaman13/emotional-llm
```

Now initialize the environment.

```bash
uv venv
source .venv/bin/activate
```

Install the packages.

```bash
uv sync
```

Make sure you run the notebook using the virtual environment created. Next you can run the notebook.
