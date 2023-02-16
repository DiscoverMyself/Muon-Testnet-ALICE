# 1. Backup your .Renv file (rename if you already do this before)

```
docker cp muon-node:/usr/src/muon-node-js/.env ./backup.env
```

# 2. Rebuild

```
cd ~/muon-node-js
docker-compose down --rmi all
git pull
docker-compose pull
docker-compose up -d
```

# 3. Restore

```
docker cp backup.env muon-node:/usr/src/muon-node-js/backup.env
docker exec -it muon-node ./node_modules/.bin/ts-node ./src/cmd keys restore backup.env
docker restart muon-node
```
