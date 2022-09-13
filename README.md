# kong-api-gateway-example

This is just a really simple example of a system management made with kong and konga. 

Basically, i've used kong as an api gateway, to manage 3 fake go services that i made.
The idea is that, kong is gonna receive all the requests, and then, make that request reach 
the right service.


## How to run the project
First of all, you gotta create a dedicated network for this project to work, basically, both our services 
and kong itself will be in that network so that it's easy to manage the request coming back and fourth. You can 
create such an network by running the command: 

```bash
sudo docker network create kong-net
```
After that, you can go to the kong directory and run docker-compose:

```bash
sudo docker-compose up -d
```

Some seconds later, everything should be up and running and them you can, finally, start up your web servers. To do that, go back to the root directory and run:

```bash
sudo docker-compose up -d
```

Finally, you can access konga and configure your services at:

> http://localhost:1337

Your kong is gonna listen at: 
> http://localhost:8000

That project was inspired by Wesley Willians, at [original project](https://youtu.be/_2GRXgYswhI), TKSM 
