# 🚀 Conversational RAG with PDF Uploads & Chat History

Welcome to **Conversational RAG**, a powerful Streamlit-based application that allows you to upload PDFs and chat with their content using AI-powered retrieval mechanisms. 📄💬

## 📌 Features:
✅ Upload and process PDFs effortlessly  
✅ Retrieve context-aware responses from uploaded documents  
✅ Seamless chat history management  
✅ Built-in PostgreSQL vector storage with `pgvector`  
![Screenshot 2025-02-22 220103](https://github.com/user-attachments/assets/12be97af-5618-4699-b6e1-ba7272427d99)


## 🚀 PostgreSQL with pgVector & pgAdmin 4 in Docker  

This guide helps you **quickly set up PostgreSQL with the pgVector extension** and **pgAdmin 4** using Docker.  

## 🛠️ **Run PostgreSQL with pgVector**  

You can start a **PostgreSQL container** with **pgVector** using the following command:  

```sh
docker run --name pgvector-container \
    -e POSTGRES_USER=langchain \
    -e POSTGRES_PASSWORD=langchain \
    -e POSTGRES_DB=langchain \
    -p 6024:5432 \
    -d pgvector/pgvector:pg16
```

### ✅ Customizations:

-Change `POSTGRES_USER` and `POSTGRES_PASSWORD` as needed.

-Modify `POSTGRES_DB` to match your project.

-Ensure port 6024 is available, or change it `(-p <your_port>:5432)`.


# 🖥️ Set Up pgAdmin 4 (Optional but Recommended)
If pgAdmin 4 is not installed on your system, you can easily run it in Docker:

### 1️⃣ Pull the pgAdmin 4 Docker Image
```sh
docker pull dpage/pgadmin4
```
### 2️⃣ Run the pgAdmin Container
```sh
docker run --name pgadmin-container \
    -p 5050:80 \
    -e PGADMIN_DEFAULT_EMAIL=user@domain.com \
    -e PGADMIN_DEFAULT_PASSWORD=password \
    -d dpage/pgadmin4
```
### ✅ Customizations:

-Replace `PGADMIN_DEFAULT_EMAIL` with your email.

-Change `PGADMIN_DEFAULT_PASSWORD` for security.

-Ensure port 5050 is free, or modify it `(-p <your_port>:80)`.

### 📌 Access pgAdmin 4

After running the container, open pgAdmin in your browser:
'🔗 http://localhost:5050](http://localhost:5050/login?next=/browser/'

Login with the 'email & password' set in the command.
![Screenshot 2025-02-22 231822](https://github.com/user-attachments/assets/2141b902-5907-4c27-bd6e-14d64f5e4156)

## ⚡ Quick Start

### 1️⃣ Clone the Repository  
```bash
git clone https://github.com/your-username/your-repo.git
cd your-repo
```
### 2️⃣ Install Dependencies
Ensure you have Python installed. Install all required packages using:
```pip install -r requirments.txt```

### 3️⃣ Run the Application
```streamlit run app.py```

![Screenshot 2025-02-22 222551](https://github.com/user-attachments/assets/dd3c8089-f167-433e-9842-f976272f701a)


