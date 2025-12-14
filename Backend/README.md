Start Node Server for API's :

node server.js


Docker
------

You can run the backend via Docker Compose from the repo root (this will also bring up Mongo):

```bash
# from repo root
docker-compose up --build backend -d
```

By default Compose sets `MONGO_URI=mongodb://mongo:27017/discountmate` for the backend service.
