#FTB Infinity Evolved 2.5 Server Dockerfile

## What the purpose of this image is:
The purpose of this image is to provide a means of quickly creating a Minecraft Feed the Beast Infinity Evolved server running version 2.5.

## What this Docker Build does:
1. Sets environment variables for:
	Downloaded version of FTB Server
	The Launch Wrapper version

2. It then downloads the required version of FTB via curl. To change the version downloaded, simply replace FTB_INFINITY_URL with the link to the version you want.

3. The image then unzips and installs, passing in environment variables for Minecraft base version, Java OPTS and the name of the startup jar.

## Using this Image:

This image inherits usage features from dlord/minecraft. For full instructions, head to [the parent repository](https://github.com/dlord/minecraft-docker)

To create an instance of the server running in a container:
```
docker run \
    --name ftb-infinity \
    -p 25565:25565 \
    -d \
    -e DEFAULT_OP={YOUR_MINECRAFT_USERNAME} \
    -e MINECRAFT_EULA=true \
    4lexnz/ftbinfinity
```

Seriously, there's a bunch more useful features that are inherited from the base image. Go check it out.