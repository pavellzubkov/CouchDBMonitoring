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
 
-  open terminal in that folder and type **docker-compose up**
- open localhost:3000 adress and enter user - **admin** password - **foobar**
