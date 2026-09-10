# IRIS-memory-configuration-wizard-Docker
The OEX package just uses a modest IRIS instance in Docker   
As the related Pull Request was ignored for years, it is  published here 
### Prerequisites
Make sure you have [git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git) and [Docker desktop](https://www.docker.com/products/docker-desktop) installed.
### Installation
Clone/git pull the repo into any local directory
```
$ git clone https://github.com/r-cemper/memory-configuration-wizard-Docker.git
```
To build and start the container run:
```
$ docker compose up -d && docker compose logs -f
```
To open IRIS console Terminal do:
```
$ docker-compose exec iris iris session iris
USER>
```
or using **iterm**
```
http://localhost:42773/iterm/
```
To access IRIS System Management Portal
```
http://localhost:42773/csp/sys/UtilHome.csp
```
### How to use it  
All user documentation is found in [original repo](https://github.com/bdeboe/isc-mem-config/blob/main/README.md)     
- [Launch Configurator](http://localhost:42773/csp/mem-config/configurator.html)

### IRIS restart in Docker
enter docker console
```
$ docker-compose exec iris bash
irisowner@a87ea46f602b:/opt/irisapp$ iris stop iris quietly restart
```
