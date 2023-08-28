# mysql_docker

You can run the mysql database in docker easily


**Note** 

I'm using port `3307`

# Quick Start
### Step 1:
Clone the repository
```
git clone <REPO_LINK>
```
```
cd <REPOSITORY>
```

### Step 2:
Start the database
```
docker compose up -d
```

Note:
Default Password: `123`
Default Database: `mydatabase`


# Access Database
You can inspect a Docker container and see the database contents using the following steps:

1. **Find the Container ID or Name:** Use the following command to list the running containers and find the ID or name of the MySQL container:

   ```
   docker ps
   ```

2. **Access the Container Shell:** Once you have the container ID or name, you can access the shell of the container using the following command:

   ```
   docker exec -it <container_id_or_name> bash
   ```

3. **Access MySQL:** Inside the container shell, you can access the MySQL database using the MySQL command-line client. You'll need to provide the root password you set when starting the MySQL container.

   ```
   mysql -uroot -p
   ```

4. **Explore the Database:** Once you are in the MySQL command-line client, you can interact with the database as you would on a regular MySQL server. For example, you can show databases, switch to a specific database, list tables, perform queries, and more.

   ```
   SHOW DATABASES;
   USE mydatabase;
   SHOW TABLES;
   SELECT * FROM your_table;
   ```

Remember to replace `mydatabase` with the actual name of the database you created and replace `your_table` with the name of the table you want to inspect.

Please note that these steps allow you to interact with the MySQL database from within the container. If you want to access the database from outside the container, you can connect to it using a MySQL client on your host machine, specifying the appropriate host and port (usually `localhost:3307` unless you've mapped it to a different port).