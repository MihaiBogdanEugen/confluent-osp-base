# [Confluent Open Source Platform] base Docker image using [Oracle JDK] #

### Supported tags and respective Dockerfile links: ###

* ```jesse-slim-8u144-2.11.11-3.2.2``` _\([jesse-slim-8u144-2.11.11-3.2.2/Dockerfile]\)_
[![](https://images.microbadger.com/badges/image/mbe1224/confluent-osp-base:jesse-slim-8u144-2.11.11-3.2.2.svg)](https://microbadger.com/images/mbe1224/confluent-osp-base:jesse-slim-8u144-2.11.11-3.2.2 "")
* ```jesse-slim-8u144-2.11.11-3.3.0```, ```latest``` _\([jesse-slim-8u144-2.11.11-3.3.0/Dockerfile]\)_
[![](https://images.microbadger.com/badges/image/mbe1224/confluent-osp-base:jesse-slim-8u144-2.11.11-3.3.0.svg)](https://microbadger.com/images/mbe1224/confluent-osp-base:jesse-slim-8u144-2.11.11-3.3.0 "")

#### All tag names follow the naming convention: ####

```debian_image_tag``` + '-' + ```java_version``` + '-' + ```scala_version``` + '-' + ```confluent_platform_version```

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
- tag ```jesse-slim-8u144-2.11.11-3.2.2``` follows branch [3.2.x], and 
- tags ```jesse-slim-8u144-2.11.11-3.3.0``` and```latest``` follow branch [3.3.x]

### Usage: ###

Build the image
```shell
docker build -t mbe1224/confluent-osp-base .
```

As for running it, *one shouldn't need to do this directly* - this image is intented to be *extended*. Check out the following images:

- [mbe1224/confluent-osp-kafka]
- [mbe1224/confluent-osp-rest-proxy]
- [mbe1224/confluent-osp-schema-registy]
- [mbe1224/confluent-osp-zookeeper]

### Dual licensed under: ###

* [Apache License]
* [Oracle Binary Code License Agreement]

   [docker-utils]: <https://github.com/confluentinc/cp-docker-images/tree/master/java>
   [Confluent Open Source Platform]: <https://www.confluent.io/product/confluent-open-source/>
   [Oracle JDK]: <http://www.oracle.com/technetwork/java/javase/downloads/index.html>
   [jesse-slim-8u144-2.11.11-3.2.2/Dockerfile]: <https://github.com/MihaiBogdanEugen/confluent-osp-base/blob/jesse-slim-8u144-2.11.11-3.2.2/Dockerfile>
   [jesse-slim-8u144-2.11.11-3.3.0/Dockerfile]: <https://github.com/MihaiBogdanEugen/confluent-osp-base/blob/jesse-slim-8u144-2.11.11-3.3.0/Dockerfile>
   [Confluent utility belt script ('cub')]: <https://raw.githubusercontent.com/confluentinc/cp-docker-images/df0091f5437113d2764cabb7433eee25fba6a4b6/debian/base/include/cub>
   [Docker utility belt script ('dub')]: <https://raw.githubusercontent.com/confluentinc/cp-docker-images/df0091f5437113d2764cabb7433eee25fba6a4b6/debian/base/include/dub>   
   [repository]: <https://github.com/confluentinc/cp-docker-images>
   [3.2.x]: <https://github.com/confluentinc/cp-docker-images/tree/3.2.x>
   [3.3.x]: <https://github.com/confluentinc/cp-docker-images/tree/3.3.x>
   [mbe1224/confluent-osp-kafka]: <https://hub.docker.com/r/mbe1224/confluent-osp-kafka/>
   [mbe1224/confluent-osp-rest-proxy]: <https://hub.docker.com/r/mbe1224/confluent-osp-kafka/>
   [mbe1224/confluent-osp-schema-registy]: <https://hub.docker.com/r/mbe1224/confluent-osp-schema-registy/>
   [mbe1224/confluent-osp-zookeeper]: <https://hub.docker.com/r/mbe1224/confluent-osp-zookeeper/>   
   [Apache License]: <https://raw.githubusercontent.com/MihaiBogdanEugen/confluent-osp-base/master/LICENSE>
   [Oracle Binary Code License Agreement]: <https://raw.githubusercontent.com/MihaiBogdanEugen/confluent-osp-base/master/Oracle_Binary_Code_License_Agreement%20for%20the%20Java%20SE%20Platform_Products_and_JavaFX>