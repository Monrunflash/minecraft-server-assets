# Minecraft Server Service

This repository provides a `minecraft.service` file that can be used to manage a Minecraft server as a systemd service. It allows you to easily start, stop, and manage the Minecraft server on your system. Additionally, it demonstrates the process of creating a service user called `minecraft` with the home directory set to `/opt/minecraft` to allocate and execute the Minecraft server.

## Getting Started

To use the `minecraft.service` file and set up the Minecraft server as a service, follow these steps:

1. Clone this repository or download the `minecraft.service` file.

2. Copy the `minecraft.service` file to the appropriate systemd directory:

	```shell
	sudo cp minecraft.service /lib/systemd/system/
	sudo chown root: /lib/systemd/system/minecraft.service
	```

3. Create the minecraft user with the home directory in /opt/minecraft:

	```shell
	sudo useradd -r -m -d /opt/minecraft minecraft
	```
4. Check that you have a minecraft folder with the server called **minecraft-server** inside


5. Enable, Start and Verify the Minecraft server service:
	
	```shell
	sudo systemctl enable minecraft.service
	sudo systemctl start minecraft.service
	sudo systemctl status minecraft.service
	```


