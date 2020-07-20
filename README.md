# swarm-traefik-wordpress

1. sudo docker swarm init
   - This setup assumes Docker Swarm.
2. sudo docker network create -d overlay web
   - Create a network for traefik.
3. touch acme.json && chmod 600 acme.json
   - Create acme.json for Let's Encrypt.
4. mkdir mysql www
   - Create docker-volumes.
5. sudo docker stack deploy -c traefik-wordpress-mysql.yml app
   - Finally deploy.