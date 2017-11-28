## Docker base image for the [Confluent Open Source Platform] using [Oracle JDK] ##

### Supported tags and respective Dockerfile links: ###

* ```3.2.2``` _\([3.2.2/Dockerfile]\)_
[![](https://images.microbadger.com/badges/image/mbe1224/confluent-base:3.2.2.svg)](https://microbadger.com/images/mbe1224/confluent-base:3.2.2 "")
* ```3.3.0``` _\([3.3.0/Dockerfile]\)_
[![](https://images.microbadger.com/badges/image/mbe1224/confluent-base:3.3.0.svg)](https://microbadger.com/images/mbe1224/confluent-base:3.3.0 "")
* ```3.3.1```, ```latest``` _\([3.3.1/Dockerfile]\)_
[![](https://images.microbadger.com/badges/image/mbe1224/confluent-base:3.3.1.svg)](https://microbadger.com/images/mbe1224/confluent-base:3.3.1 "")

*All tag names follow the naming convention of the [Confluent Open Source Platform]*

### Summary: ###

- Debian "slim" image variant
- Oracle JDK 8u152 addded, without MissionControl, VisualVM, JavaFX, ReadMe files, source archives, etc.
- Oracle Java Cryptography Extension added
- Python 2.7.9-1 & pip 9.0.1 added
- SHA 256 sum checks for all downloads
- JAVA\_HOME environment variable set up
- Utility scripts added:
    - [Confluent utility belt script ('cub')] - a Python CLI for a Confluent tool called [docker-utils]
    - [Docker utility belt script ('dub')]

### Details: ###

This image was created with the sole purpose of offering the [Confluent Open Source Platform] running on top of [Oracle JDK].
Therefore, it follows the same structure as the one from the original [repository]. More precisely:
- tag ```3.2.2``` follows branch [3.2.x], and 
- tags ```3.3.0```, ```3.3.1``` and```latest``` follow branch [3.3.x]

### Usage: ###

Build the image
```shell
docker build -t mbe1224/confluent-base ./3.3.1/
```

As for running it, *one shouldn't need to do this directly* - this image is intented to be *extended*. Check out the following images:

- [mbe1224/confluent-kafka]
- [mbe1224/confluent-rest-proxy]
- [mbe1224/confluent-schema-registry]
- [mbe1224/confluent-zookeeper]

### Dual licensed under: ###

* [MIT License]
* [Oracle Binary Code License Agreement]

   [docker-utils]: <https://github.com/confluentinc/cp-docker-images/tree/master/java>
   [Confluent Open Source Platform]: <https://www.confluent.io/product/confluent-open-source/>
   [Oracle JDK]: <http://www.oracle.com/technetwork/java/javase/downloads/index.html>
   [3.2.2/Dockerfile]: <https://github.com/MihaiBogdanEugen/docker-confluent-base/blob/master/3.2.2/Dockerfile>
   [3.3.0/Dockerfile]: <https://github.com/MihaiBogdanEugen/docker-confluent-base/blob/master/3.3.0/Dockerfile>
   [3.3.1/Dockerfile]: <https://github.com/MihaiBogdanEugen/docker-confluent-base/blob/master/3.3.1/Dockerfile>
   [Confluent utility belt script ('cub')]: <https://raw.githubusercontent.com/confluentinc/cp-docker-images/df0091f5437113d2764cabb7433eee25fba6a4b6/debian/base/include/cub>
   [Docker utility belt script ('dub')]: <https://raw.githubusercontent.com/confluentinc/cp-docker-images/df0091f5437113d2764cabb7433eee25fba6a4b6/debian/base/include/dub>   
   [repository]: <https://github.com/confluentinc/cp-docker-images>
   [3.2.x]: <https://github.com/confluentinc/cp-docker-images/tree/3.2.x>
   [3.3.x]: <https://github.com/confluentinc/cp-docker-images/tree/3.3.x>
   [mbe1224/confluent-kafka]: <https://hub.docker.com/r/mbe1224/confluent-kafka/>
   [mbe1224/confluent-rest-proxy]: <https://hub.docker.com/r/mbe1224/confluent-rest-proxy/>
   [mbe1224/confluent-schema-registry]: <https://hub.docker.com/r/mbe1224/confluent-schema-registry/>
   [mbe1224/confluent-zookeeper]: <https://hub.docker.com/r/mbe1224/confluent-zookeeper/>   
   [MIT License]: <https://raw.githubusercontent.com/MihaiBogdanEugen/docker-confluent-base/master/LICENSE>
   [Oracle Binary Code License Agreement]: <https://raw.githubusercontent.com/MihaiBogdanEugen/docker-confluent-base/master/Oracle_Binary_Code_License_Agreement%20for%20the%20Java%20SE%20Platform_Products_and_JavaFX>