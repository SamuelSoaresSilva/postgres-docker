# Requirements
- Docker desktop 
- Your favorite DBMS that supports Postgres

> **Note:** If you don't meet some of the **requirements**, below are links that will help you

## Recommending links
### [Docker](https://desktop.docker.com/win/main/amd64/Docker%20Desktop%20Installer.exe?utm_source=docker&utm_medium=webreferral&utm_campaign=dd-smartbutton&utm_location=module&_gl=1*126zw6w*_gcl_au*MTAxNjQzMDc1OC4xNzE5MzMzODIz*_ga*MTY1NjU4OTQyMC4xNzE4NjQxNTA3*_ga_XJWPQMJYHQ*MTcxOTMzOTk1MS4zLjEuMTcxOTMzOTk1Mi41OS4wLjA.) | [DBever](https://dbeaver.io/files/dbeaver-ce-latest-x86_64-setup.exe)

# Let's start!!
### Running a postgres image with the following command line by your cmd or powershell

> cmd ex: <br/>
> C:\Users\your.user>docker run -p 5432:5432 -e POSTGRES_PASSWORD=admin -d postgres
```
docker run -p 5432:5432 -e POSTGRES_PASSWORD=admin -d postgres
```

After this command you will not notice many visual results
> cmd ex: <br/>
C:\Users\your.user>docker run -p 5432:5432 -e POSTGRES_PASSWORD=admin -d postgres <br/>
fd6b9d426dbf3666744dcc089c00a740835e45d9fd19fb6e51a6362de3f10e83<br/>
C:\Users\your.user> <br/>

to see this enter the following command:

```
docker ps
```

or:

```
docker ps -a
```
>cmd ex: <br/>
C:\Users\your.user>docker ps -a <br/>


| CONTAINER ID | IMAGE    | COMMAND                | CREATED         | STATUS         | PORTS                   | NAMES       |
|--------------|----------|------------------------|-----------------|----------------|-------------------------|-------------|
| fd6b9d426dbf | postgres | "docker-entrypoint.s…" | 2 minutos atrás | Ativo 2 minutos | 0.0.0.0:5432->5432/tcp  | sweet_nash  |


> C:\Users\your.user> <br/>

## After that, you can just stop and remove all stopped containers
<br/>

### Stop container

>cmd ex: <br/>
C:\Users\your.user>docker stop -t 0 fd6b9d426dbf <br/>

```
docker stop -t 0 ID
```

In this case, the code after **stop** is the **CONTAINER ID** and **-t (N)** it's for define a time for stop the container
<br/>
### Remove all stopped containers

>cmd ex: <br/>
C:\Users\your.user>docker container prune<br/>
WARNING! This will remove all stopped containers.<br/>
Are you sure you want to continue? [y/N]<br/>

```
docker container prune
```

### Just type "y" to confirm

