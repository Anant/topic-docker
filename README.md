# topic-docker
A quality knowledge base and tutorial on Docker for CIO/CTO or those who want to be. 

A curated set of topics and readings on [Docker](http://docker.com/) packages and resources. Maintained by Rahul Singh of [Anant](http://anant.us). Feel free contact me if you'd like to collaborate on this and other awesome lists. 

## Knowledgebase in a Docker container using Raneto

This docker container is to setup Knowledgebase available in a container to start your centralised documentation in seconds.

### How to use docker container

The simple and quick way to use this container is as follows.

**Software required to use docker container**

- Docker (Tested version 1.13.0)

**Steps to use container**

- Pull the [Raneto](https://hub.docker.com/r/appsecco/raneto) image from the docker hub

```
docker pull appsecco/raneto
```

- Clone the repostiory for sample configuration and content

```
git clone https://github.com/xingh/topic-docker.git

cd topic-docker
```

- Make changes for configuration if required in `config/config.default.js`

- Then you are ready to run the Knowledgebase

```
docker run -v `pwd`/content/:/data/content/ -v `pwd`/config/config.default.js:/opt/raneto/example/config.default.js -p 3000:3000 -d appsecco/raneto
```

- Then navigate to [http://localhost:3000](http://localhost:3000)

- If you want to add more content to the Knowledgebase. Just add your directories (or) markdown files to the `content` folder in host system. It will update automatically


---


Please feel free to make a pull request. I'm also available on Twitter at [@xingh](https://twitter.com/xingh). My goal is to make this type of KB a template repository for more content similar to the awesome lists.