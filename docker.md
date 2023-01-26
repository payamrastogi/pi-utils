#### How to install Docker on Raspberry Pi
Step 1: Update the Raspberry Pi

Before installing Docker, you will want to make sure your Raspberry Pi is up-to-date. 
To do this, open a terminal window and type the following command:

```shell
sudo apt-get update
sudo apt-get upgrade
```
Note: if curl is not installed, install curl package by running the following command in your termina
```shell
sudo apt install curl
```

Step 2: Install Docker

To install Docker on your Raspberry Pi, you will first need to add the Docker package repository to your system. To do this, type the following command in your terminal window:

```shell
curl -sSL https://get.docker.com | sh
```

Step 3: Add the Pi user to the Docker group

By default, the Pi user is not a member of the Docker group. To add the Pi user to the Docker group, type the following command:

```shell
sudo usermod -aG docker pi
```

Step 4: Start the Docker service

Now that Docker is installed and the Pi user is a member of the Docker group, you can start the Docker service. To do this, type the following command:

```shell
sudo systemctl start docker
```

Step 5: Test the installation

To test that Docker is working properly on your Raspberry Pi, you can run the following command:

```shell
docker run hello-world
```
This command will download and run a test container, which will display a message indicating that Docker is working correctly.

Note: You may see a warning message that states that the Docker daemon is not running on your system. This is expected, as the Docker daemon is not running in the background by default on the Raspberry Pi.

Step 6: Enable the Docker service

To enable the Docker service so that it starts automatically on boot, type the following command:

```shell
sudo systemctl enable docker
```
You have successfully installed and configured Docker on your Raspberry Pi. You can now run and manage Docker containers.

(optional) Step 7: To install docker compose, type the following command:

```shell
sudo apt install -y python3-pip libffi-dev
sudo pip3 install docker-compose
```



```shell
sudo docker-compose stop #to stop the container
sudo docker-compose rm # to delete the container

sudo docker images # to list the pulled images 
sudo docker rmi # to delete multiple images
```