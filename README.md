# 🚀 PostgreSQL with pgVector & pgAdmin 4 in Docker  

This guide helps you **quickly set up PostgreSQL with the pgVector extension** and **pgAdmin 4** using Docker.  

## 🛠️ **Run PostgreSQL with pgVector**  

You can start a **PostgreSQL container** with **pgVector** using the following command:  

```bash
docker run --name pgvector-container \
    -e POSTGRES_USER=langchain \
    -e POSTGRES_PASSWORD=langchain \
    -e POSTGRES_DB=langchain \
    -p 6024:5432 \
    -d pgvector/pgvector:pg16```

##✅ Customizations:

Change POSTGRES_USER and POSTGRES_PASSWORD as needed.
Modify POSTGRES_DB to match your project.
Ensure port 6024 is available, or change it (-p <your_port>:5432).
