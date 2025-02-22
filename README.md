# A simple MERN stack application 

### Create a network for the docker containers

`docker network create demo`

### Build the client 

```sh
cd mern/frontend
docker build -t mern-frontend .
```

### Run the client

`docker run --name=frontend --network=demo -d -p 5173:5173 mern-frontend`

### Verify the client is running

Open your browser and type `http://localhost:5173`

### Run the mongodb container

`docker run --network=demo --name mongodb -d -p 27017:27017 -v ~/opt/data:/data/db mongodb:latest`

### Build the server

```sh
cd mern/backend
docker build -t mern-backend .
```

### Run the server

`docker run --name=backend --network=demo -d -p 5050:5050 mern-backend`

## Using Docker Compose

`docker compose up -d`

## Outputs

<img width="958" alt="image" src="https://github.com/user-attachments/assets/67506688-9345-4f08-9586-54c542886c17" />

<img width="948" alt="image" src="https://github.com/user-attachments/assets/bcb996ad-b7e5-45b0-b88f-74a9814dc816" />

<img width="959" alt="image" src="https://github.com/user-attachments/assets/fc185a03-5f6c-4d9f-bc45-75795f936881" />

<img width="956" alt="image" src="https://github.com/user-attachments/assets/fd173548-eac0-4b02-bd6b-2763a022447e" />


## Explanation of Porject

### **Project: Three-Tier Web Application Using Docker**  
- Built a **three-tier architecture** with **React (frontend), Express.js (backend), and MongoDB (database)**.  
- **Containerized** each component using **Dockerfiles** and managed them with **Docker Compose**.  
- Created a **Docker network** for **secure communication** between containers.  
- Ensured **MongoDB data persistence** using **Docker volumes**.  
- Used **Docker Compose** to automate deployment and container orchestration.  
- Overcame **networking issues** by using **service names instead of localhost**.  
