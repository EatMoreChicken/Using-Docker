# Using-Docker
Personal notes on installing and using Docker.

## Installing Docker

_Large portion of the installation process if from [DigitalOcean](https://www.digitalocean.com/community/tutorials/how-to-install-and-use-docker-on-ubuntu-16-04). I will be leaving notes to explain the process as much as I can._

Add GPG key for Docker's repository:

`curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -`

Add Docker repository to our APT resources:

`sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"`

Update our database to reflect the changes we made:

`sudo apt-get update`

Install Docker:

_The `-y` tag will automatically reply yes to prompts populated during the installation process._

`sudo apt-get install -y docker-ce`

Check the status for Docker:

`sudo systemctl status docker`

You should see something like this:
```
● docker.service - Docker Application Container Engine
   Loaded: loaded (/lib/systemd/system/docker.service; enabled; vendor prese
   Active: active (running) since Sun 2019-02-10 13:30:09 EST; 12s ago
     Docs: https://docs.docker.com
 Main PID: 19167 (dockerd)
    Tasks: 14
   CGroup: /system.slice/docker.service
           └─19167 /usr/bin/dockerd -H fd://
```
