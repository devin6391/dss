### Prisma Deploy
* Make sure you have config folder with valid .env files. If you don't have that then get it from your peer.
* Prisma container needs environment variable named `PRISMA_MANAGEMENT_API_SECRET` with value equal to `dssdev`, make sure it is available in terminal. In docker-compose it is mentioned as `managementApiSecret: dssdev`.
* Make sure docker is installed, also docker-compose is installed. Make sure Prisma and nodejs are installed as well.
* Create Prisma and Postgre containers by going to the path - `./dss-prisma`. There enter the command `sudo docker-compose up -d`.
* Endpoint in ubuntu generally refers to the local ip of the machine. Make sure to curl these things to make sure docker container of Prisma is up at either `http://localhost:4466` OR `http://192.168.x.x:4466` OR `http://127.0.0.1:4466`.
* Also check about containers by entering `sudo docker ps` and `sudo docker info`.
* Once we are sure that all containers are there then we should deploy our prisma server by entering the command `sudo prisma deply -e ../config/dev.env`. The `PRISMA_MANAGEMENT_API_SECRET` environment variable is available via `config/dev.env` file.
* Now we should be seeing our prisma server on `http://localhost:4466` OR `http://192.168.x.x:4466` OR `http://127.0.0.1:4466`.
* Any change in datamodel.prisma/prisma.yml requires to rerun `sudo prisma deply -e ../config/dev.env`.
* On the given server address for localhost, we can do CRUD operations as per graphql and prisma's documentation. But we need to make sure to generate auth token before that. Which can be done by going to the folder `./dss-prisma/` and then executing the command `sudo prisma token -e ../config/dev.env`.
* Copy the token, in the prisma graphql UI, we would see in bottom-left and option for entering HTTP HEADERS. There add this json
    ```
    {
        "Authorization": "Bearer ${Your prisma auth token}"
    }
    ```
* Now you will be able to see schema and docs of any query and thus be able to execute any.
* Changing schema and redeploying prisma might throw error if there already is data stored in postgreSQL. TO fix that all data must be deleted for that model and then redeployment of prisma should happen. Or migrate data.