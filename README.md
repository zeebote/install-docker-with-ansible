# Install docker with ansible
This installation is based on instruction of Docker official [website](https://docs.docker.com/engine/install/ubuntu/)<br>
The install included 3 files: <br>
**daemon.json** which is used to custom docker service settings. You can get a complete daemon.json configure [here](https://docs.docker.com/engine/reference/commandline/dockerd/#daemon-configuration-file)<br>
**override.conf** is used to configure remote access to docker<br>
**ansible-nodes** is list of node (ubuntu 18.04, or 20.04) that you want install docker to. You must update this with your env. <br>
To run the installation make sure you have all files on the same folder with the play-book yaml<br>
This script assume you already configure access from your ansible host to your nodes:<br>
<br>
ansible-playbook -i ansible-nodes instdocker-play.yml --ask-become-pass
