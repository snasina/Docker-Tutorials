# How-to-Install-Docker-on-Ubuntu-18.04
![docker](https://user-images.githubusercontent.com/24427856/71299521-b3bf5380-23b3-11ea-9874-08157123687a.PNG)


Docker is a platform which packages an application and all its dependencies together in the form of containers. This containerization aspect of Docker ensures that the application works in any environment.
Docker Compose is a tool for defining and running multi-container Docker applications. It allows users to launch, execute, communicate, and close containers with a single coordinated command.

In this tutorial, we will cover how to install Docker CE(Community Edition) on Ubuntu 18.04.

### Prerequisites

Ubuntu 18.04 64-bit operating system
A user account with sudo privileges
Docker software repositories (optional)

## 1.Update Software Repositories
As usual, it’s a good idea to update the local database of software to make sure you’ve got access to the latest revisions.

```sudo apt-get update```

## 2.Remove any older installations of Docker that may be on your system

```sudo apt remove docker docker-engine docker.io```

## 3.Make sure you have the necessary packages to allow the use of Docker’s repository

```sudo apt install apt-transport-https ca-certificates curl software-properties-common```

## 4.Add Docker’s GPG key

```curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -```

## 5.Verify the fingerprint of the GPG key

```sudo apt-key fingerprint 0EBFCD88```

## 6.Add the stable Docker repository

```sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"```

## 7.Update your package and install Docker CE

```
sudo apt update
sudo apt install docker-ce
```

## 8.Add your limited Linux user account to the docker group(To run Docker commands without sudo):

```sudo usermod -aG docker $USER```

## 9.Check Docker Version
To verify the installed Docker version number, enter:

```
docker --version
docker-compose --version
```

## 10.Start and Automate Docker

```
sudo systemctl start docker
sudo systemctl enable docker
sudo systemctl status docker
```

## 11.Uninstalling Docker
Before uninstalling Docker remove all containers, images, volumes, and networks.
You can uninstall Docker as any other package installed with apt:

```
sudo apt purge docker-ce
sudo apt autoremove
```
[a relative link](https://snasina.github.io/How-to-Install-Docker-on-Ubuntu-18.04/)


Will see how to use docker in our next tutorial...Stay tuned.....
