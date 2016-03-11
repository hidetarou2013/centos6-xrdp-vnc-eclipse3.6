# centos6-xrdp-vnc-eclipse3.6

centos6-xrdp-vnc-eclipse3.6

## 1.git clone

```sh
$ git clone git@github.com:hidetarou2013/centos6-xrdp-vnc-eclipse3.6.git
```

## 2.docker build

```sh
$ cd centos6-xrdp-vnc-eclipse3.6
$ docker build -t hidetarou2013/centos6-xrdp-vnc-eclipse3.6 .
$ docker build -t hidetarou2013/centos6-xrdp-vnc-eclipse3.6:1920x1024 .
$ docker build -t hidetarou2013/centos6-xrdp-vnc-eclipse3.6:1280x1024 .
$ docker build -t hidetarou2013/centos6-xrdp-vnc-eclipse3.6:1536x1024 .

```

## 3.docker run

### 3.1 run vnc

```sh
$ docker run --name vnc -d -p 5901:5901 hidetarou2013/centos6-xrdp-vnc-eclipse3.6:1920x1024
```

id/password
kioskuser/kioskuser

### 3.2 run xrdp

```sh
$ docker run -d -p 3389:3389 --link vnc --name xrdp kevensen/centos-xrdp
```


