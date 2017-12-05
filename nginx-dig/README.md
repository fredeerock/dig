A simple nginx proxy docker image for serving other docker images. 

- Run with `docker-compose up -d`
- Visit the nginx proxy site at http://localhost:8080
- Visit the other docker images at http://localhost:8080/server1 and http://localhost:8080/server2

---

You can use this in conjunction with other docker-compose defined services. For instance the below command will run 2 docker-compose files with a common network called **thedig**. 

`docker-compose -f nginx-docker-proxy/docker-compose.yml -f mediawiki-dig/docker-compose.yml -p thedig up`

