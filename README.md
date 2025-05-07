# Getting Started

This is a project to test Docker and create different containers.

### Running the Application for the First tTime

> 💡 Before running the application, ensure that Docker and Docker Compose are installed and set up. You may also need to ask a team member to provide the necessary environment variables.

```bashrc
docker-compose up
```

> 💡 Add the `-d` flag to run the containers in detached mode.


### Accessing the Database

I often find myself wanting to update the database from the command line. To do so, first you will need to access the container:

```bashrc
docker exec -it <container_name> bash
```

> _💡 To get the container name, you can run `docker ps`_

Once inside the container, run the following command:

```bashrc
psql -U <database_user> -d <database_name>
```

The variables used here should match the ones defined in your `.env` file.
