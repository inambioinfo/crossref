# Store and process the Crossref Database

## MongoDB

MongoDB is run via [Docker](https://hub.docker.com/_/mongo/).
It's available on the host machine at http://localhost:27017/.

```sh
# https://hub.docker.com/_/mongo/
docker run \
  --name=mongo-crossref \
  --publish=27017:27017 \
  --volume=`pwd`/mongo.db:/data/db \
  --detach \
  --rm \
  mongo:3.4.2
```

```
# Remove all containers
docker rm `docker ps --no-trunc -aq`
```