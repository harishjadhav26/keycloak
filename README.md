Keycloak MariaDB Deploy using docker-compose

#### Verify and update docker compose

https://docs.docker.com/compose/install/

Clone git repo:

``` git clone https://github.com/harishjadhav26/keycloak.git ```

``` cd keycloak ```

Start docker containers using docker compose.

``` docker-compose -p oauthserver -f keycloak_mariaDB.yml up -d ```

Verify rinnung containers:

``` docker ps ```

Check container logs:

``` docker logs -f oauthserver_keycloak_1 ```

``` docker logs -f oauthserver_mariadb_1 ```

Destroy keycloak containers:

``` docker-compose -p oauthserver -f keycloak_mariaDB.yml down -v ```

```
# Default application username and password.
# DB User: root, Password: strong#password#2345
# Kcloak DB User: keycloakadmin, Password: keycloak#2345, DB: keycloakDB
# Kcloak Login Admin User: admin, Password: admin#2345
```

##### Open URL in your browser

```http://localhost:8080```

Enter given default username and password and your server is ready to use.

