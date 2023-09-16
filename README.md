# nexus-setup

it is very simple to run nexus as a docker container

and minimum 4vcpu and 16gb ram required


docker run -d -p 8081:8081 -p 8083:8083 --name nexus -v nexus-data:/nexus-data sonatype/nexus3

and 8081 is to access from the outside for nexus gui

and 8083 is to used as a docker registry port

and where ever you are running docker container you have to configure the ip of the nexus and port which we are mapped to the nexus docker registry

sudo vi /etc/docker/daemon.json

{
    "insecure-registries": ["nexusip:8083"]
}


restart docker

