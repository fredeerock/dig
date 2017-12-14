A way to manage a server with multiple services and a nginx proxy.

---

Perhaps it is better to run separate commands for each docker comopse:

1. `cd mediawiki-dig && docker-compose -p thedig up -d`
2. `cd nginx-dig && docker-compose -p thedig up -d`

Then for making changes run:

1. `cd nginx-dig && docker-compose restart`
2. `cd mediawiki-dig && docker-compose restart` 

---

You could also run the below command with 2 docker-compose files and a common project and network name called **thedig**. 

`docker-compose -f nginx-docker-proxy/docker-compose.yml -f mediawiki-dig/docker-compose.yml -p thedig up`

*However, the above command creates volumes relative to the first docker-compose file only.*