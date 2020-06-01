# Docker
## Microsoft SQL Server 2017 en docker desktop Windows 10
### Comando ejecutar en PowerShell


```powershell
docker run -e "ACCEPT_EULA=Y" -e "SA_PASSWORD=Sample123$" -p 1433:1433 --rm --name MSSQL -v /d/Docker/MSSQL/data:/var/opt/mssql/data -d mcr.microsoft.com/mssql/server
:2017-latest

```


#### Salida de Ejecucion de PowerShell
```powershell
PS C:\Windows\system32> docker ps
CONTAINER ID        IMAGE                                        COMMAND                  CREATED             STATUS              PORTS                    NAMES
c2ac5912e72b        mcr.microsoft.com/mssql/server:2017-latest   "/opt/mssql/bin/nonr…"   19 minutes ago      Up 19 minutes       0.0.0.0:1433->1433/tcp   sql1
PS C:\Windows\system32>
```

Conexion desde SSMS 
Server = localhost,1433
Username = sa
Password = Sample123$


## Prune unused Docker objects
## Prune images🔗
docker image prune -a --filter "until=24h"
