# PSQL commands

- type in ```psql``` to enter into the psql CLI interface. (Can also use ```pgcli```)

- ```\l``` lists all databases

### Managing users and permissions

- ```\du``` lists all users
- ```drop user jimmy;``` deletes the user jimmy
- ```create user jimmy superuser password 'jimmyface';``` creates a superuser jimmy with password jimmyface.
- ```alter database my_database owner to jimmy;``` changes owner of my_database to jimmy.