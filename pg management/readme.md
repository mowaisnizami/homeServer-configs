bash into container
sudo docker exec -it <dockerId> bash -u <adminUsername>
create a new user and database
CREATE DATABASE <dbName>;
CREATE USER <userName> WITH PASSWORD '<password>';
GRANT ALL PRIVILEGES ON DATABASE <databaseName> TO <userName>;
exit;
sudo docker exec -it <dockerId> bash -u <adminUsername> -d <newDatabaseName>
GRANT ALL ON SCHEMA public TO <newUserName>;
exit;