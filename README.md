# NodeJS Postgresql CRUD Application

This is a CRUD Rest API project built using Node.js Express, and Postgresql running on a docker container for user management.


## Features

- Create a user with a name and email in the Postgresql database. 
- Get all users from the Postgresql database. 
- Get a user from the Postgresql database using the user's ID.
- Update a user's name and email from the Postgresql database using the user's ID.
- Delete a user from the Postgresql database using the user's ID.
- Postgresql database in docker so the system is containerized

## API testing (postman):

### User Created
![image](/imgs/post.png)

### User Getting
![image](/imgs/get.png)

### User Updating
![image](/imgs/editby.png)

### User Deleting
![image](/imgs/deleteby.png)


## Getting Started

### Prerequisites

- Node.js 18+ 
- npm or yarn
- Docker 

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/Siratul804/postgresql_node_CRUD.git
   cd postgresql_node_CRUD
   ```

2. Install dependencies:
   ```bash
   npm install
   # or
   yarn install
   ```

3. Docker Setup :

   ```
   /* Check version */
   docker --version 

   /* Pull postgres image */
   docker pull postgres 

   /* Run postgres in docker container */
   docker run --name postgres-db -e POSTGRES_PASSWORD= -p 5432:5432 -d postgres

   /* Get info about docker container */
   docker ps

   /* Connect to PostgreSQL Container */
   docker exec -it postgres-db psql -U postgres 
   ```
   
4. PGAdmin4 extension for Docker Desktop :
   - You can use this extension, which will help you to deal with postgres easily.
   -  <a href="https://github.com/marcelo-ochoa/pgadmin4-docker-extension"> PGAdmin4 Extension</a> 

5.  Set up environment variables:
   Create a `.env` file in the root directory with:
   ```env
   PORT=5001
   DB_USER=postgres
   DB_HOST=localhost
   DB_NAME=express-curd
   DB_PASSWORD=admin
   DB_PORT=5432
   ```

6. Run the development server:
   ```bash
   npm run dev
   # or
   yarn dev
   ```

7. If the setup is ready you will see in your terminal:
   ```
    nodemon src/index.js
   [nodemon] 3.1.9
   [nodemon] to restart at any time, enter `rs`
   [nodemon] watching path(s): *.*
   [nodemon] watching extensions: js,mjs,cjs,json
   [nodemon] starting `node src/index.js`
   User table created if not exists
   Server is running on http:localhost:5001
   Connection pool establised with Database
   ```

## Tech Stack

- Node.js
- Postgresql
- Docker


## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.


<p align="right">
  <small>© 2025  <a href="https://github.com/Siratul804">  Siratul Islam </a>. All rights reserved.</small>
</p>

