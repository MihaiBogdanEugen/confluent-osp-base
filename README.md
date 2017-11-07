## Docker base image for the [Confluent Open Source Platform] using [Scala] and [Oracle JDK] ##

### Supported tags and respective Dockerfile links: ###

* ```3.2.2``` _\([3.2.2/Dockerfile]\)_
[![](https://images.microbadger.com/badges/image/mbe1224/docker-confluent-platform-base:3.2.2.svg)](https://microbadger.com/images/mbe1224/docker-confluent-platform-base:3.2.2 "")
* ```3.3.0```, ```latest``` _\([3.3.0/Dockerfile]\)_
[![](https://images.microbadger.com/badges/image/mbe1224/docker-confluent-platform-base:3.3.0.svg)](https://microbadger.com/images/mbe1224/docker-confluent-platform-base:3.3.0 "")

#### All tag names follow the naming convention: #####

```confluent_platform_version```

### About: ### 

#### Summary: ####

- Debian "slim" image variant
- Oracle Java SE Development Kit (JDK) 8u144 addded, without MissionControl, VisualVM, JavaFX and JRE
- Oracle Java Cryptography Extension added
- Scala 2.11.11 added
- Python 2.7.9-1 & pip 9.0.1 added
- SHA 256 sum checks for all downloads
- JAVA\_HOME and SCALA\_HOME environment variables set up
- Utility scripts added:
    - [Confluent utility belt script ('cub')] - a Python CLI for a Confluent tool called [docker-utils]
    - [Docker utility belt script ('dub')]

#### More details: ####

This image was created with the sole purpose of offering the [Confluent Open Source Platform] running on top of [Oracle JDK].
Therefore, it follows the same structure as the one from the original [repository]. More precisely:
- tag ```3.2.2``` follows branch [3.2.x], and 
- tags ```3.3.0``` and```latest``` follow branch [3.3.x]

### Usage: ###

Build the image
```shell
docker build -t mbe1224/cconfluent-platform-base /3.3.0/
```

As for running it, *one shouldn't need to do this directly* - this image is intented to be *extended*. Check out the following images:

- [mbe1224/docker-confluent-platform-kafka]
- [mbe1224/docker-confluent-platform-rest-proxy]
- [mbe1224/docker-confluent-platform-registy]
- [mbe1224/docker-confluent-platform-zookeeper]

### Dual licensed under: ###

* [MIT License]
* [Oracle Binary Code License Agreement]

   [docker-utils]: <https://github.com/confluentinc/cp-docker-images/tree/master/java>
   [Confluent Open Source Platform]: <https://www.confluent.io/product/confluent-open-source/>
   [Oracle JDK]: <http://www.oracle.com/technetwork/java/javase/downloads/index.html>
   [Scala]: <https://www.scala-lang.org/>
   [3.2.2/Dockerfile]: <https://github.com/MihaiBogdanEugen/docker-confluent-platform-base/blob/master/3.2.2/Dockerfile>
   [3.3.0/Dockerfile]: <https://github.com/MihaiBogdanEugen/docker-confluent-platform-base/blob/master/3.3.0/Dockerfile>
   [Confluent utility belt script ('cub')]: <https://raw.githubusercontent.com/confluentinc/cp-docker-images/df0091f5437113d2764cabb7433eee25fba6a4b6/debian/base/include/cub>
   [Docker utility belt script ('dub')]: <https://raw.githubusercontent.com/confluentinc/cp-docker-images/df0091f5437113d2764cabb7433eee25fba6a4b6/debian/base/include/dub>   
   [repository]: <https://github.com/confluentinc/cp-docker-images>
   [3.2.x]: <https://github.com/confluentinc/cp-docker-images/tree/3.2.x>
   [3.3.x]: <https://github.com/confluentinc/cp-docker-images/tree/3.3.x-quickstart-fix>
   [mbe1224/docker-confluent-platform-kafka]: <https://hub.docker.com/r/mbe1224/docker-confluent-platform-osp-kafka/>
   [mbe1224/docker-confluent-platform-rest-proxy]: <https://hub.docker.com/r/mbe1224/docker-confluent-platform-osp-kafka/>
   [mbe1224/docker-confluent-platform-schema-registy]: <https://hub.docker.com/r/mbe1224/docker-confluent-platform-schema-registy/>
   [mbe1224/docker-confluent-platform-zookeeper]: <https://hub.docker.com/r/mbe1224/docker-confluent-platform-zookeeper/>   
   [MIT License]: <https://raw.githubusercontent.com/MihaiBogdanEugen/docker-confluent-platform-base/master/LICENSE>
   [Oracle Binary Code License Agreement]: <https://raw.githubusercontent.com/MihaiBogdanEugen/docker-confluent-platform-base/master/Oracle_Binary_Code_License_Agreement%20for%20the%20Java%20SE%20Platform_Products_and_JavaFX>