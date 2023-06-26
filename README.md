# docker-rocketmq
**RocketMq with Docker Compose** 

Using Docker Compose to create an rocketmq.

## Prerequisite

+ Install [Docker][1] and [Docker Compose][2] in your testing environment

## Start with following steps

+ (1) Start rocketmq

```
docker-compose up -d
```

The result is 

```
Creating docker-rocketmq ... done 
```

+ (2) Check the status of rocketmq

```
docker-compose ps
```

The result is 

```
  Name                 Command               State                                                        Ports
--------------------------------------------------------------------------------------------------------------------------------------------------------------------
mqbroker    sh mqbroker -n mqnamesrv:9 ...   Up      0.0.0.0:10909->10909/tcp,:::10909->10909/tcp, 0.0.0.0:10911->10911/tcp,:::10911->10911/tcp, 10912/tcp, 9876/tcp
mqconsole   sh -c java $JAVA_OPTS -jar ...   Up      0.0.0.0:19876->8080/tcp,:::19876->8080/tcp
mqnamesrv   sh mqnamesrv                     Up      10909/tcp, 10911/tcp, 10912/tcp, 0.0.0.0:9876->9876/tcp,:::9876->9876/tcp
```

+ (3) View rocketmq management console on : http://hostname:19876 .


[1]: https://www.docker.com
[2]: https://docs.docker.com/compose/

## License

Apache 2.0 license
