# stardog-docker-compose
Docker Compose Setup and Workflow to re-create POSTDATAs Backend

# use

* go to [stardog.com](https://www.stardog.com/download-free/) and get a license file `stardog-license-key.bin`; move this file to `stardog-home` folder (create it!)
* use `docker-compose up` to get a running instance of stardog and a stardog studio. 
* in stardog studio running at localhost:8888 connect this to the local stardog container running at: http://localhost:5820 ; default user and pw are `admin`
* manually create a new database `PD_KG` in stardog studio
* POSTDATAs data can be loaded with curl: In the unzipped knowledge graph folder:
```
for f in *.ttl; do curl -X POST -H 'Content-Type:application/x-turtle' --data-binary @$f http://admin:admin@localhost:5820/PD_KG ; done
```


