# docker-swarm
a quick setup for my docker swarm

## Setup

1. Install [docker](https://docs.docker.com/engine/install/ubuntu/)
2. Setup a docker swarm
3. Clone this repo
4. Deploy the basic stack from this repo to the swarm `docker stack deploy --compose-file=basic-stack.yml basic`

Now there are 3 things setup for you:

* [Portainer](https://www.portainer.io/)
* [Traefik](https://docs.traefik.io/)
* Docker registry

    To use the registry a few things are needed
   1. To add a user to the registry that cann pull and push, add a `registryusersfile` to the `users` volume
   2. You can now add the registry with your username and password chosen in the `registryusersfile`
   3. To pull images from the registry you have to put the registry address infront of your image name

5. To deploy a new stack add it to the stack templates of portainer (The `whoami-stack` is an example for that)
6. Deploy your added stack!

