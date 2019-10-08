# CouchDBMonitoring
This is partial fork from https://github.com/gesellix/couchdb-prometheus-exporter

# How to Run
 - install docker and docker-compose
 - clone or download this repo
 - open with editor **docker-compose.yml** (edit only address,port,user and password of couchdb) and save that file
 
 couchdbstats1:       
 image: gesellix/couchdb-prometheus-exporter:latest
 command: '--couchdb.uri=**http://192.168.1.17:5984** --logtostderr --databases=_all_dbs'        
 environment:            
 -COUCHDB.USERNAME=${COUCHDB_USER:-**ladmin**}'  '
 -COUCHDB.PASSWORD=${COUCHDB_PASSWORD:-**Local0513**}'`
 
 if couchdb run on other container on same machine, then ip adress should be not 'localhost' or '127.0.0.1'. (put ip your machine in 
 local network e.g. '192.168.1.144')
 
-  open terminal in that folder and type **docker-compose up**
- open localhost:3000 adress and enter user - **admin** password - **foobar**
- click on 'Home' menu and select 'CouchDB Dashboard'

![alt text](https://github.com/pavellzubkov/CouchDBMonitoring/blob/master/screenshots/grafana_login.png)
![alt text](https://github.com/pavellzubkov/CouchDBMonitoring/blob/master/screenshots/select_dashboard.png)
![alt text](https://github.com/pavellzubkov/CouchDBMonitoring/blob/master/screenshots/dashboard.png)
