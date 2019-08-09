# Infrastructure for Agile Partner's DDD/CQRS/ES² workshop

## Tools & components

Throughout the workshop, we will be using:

* [EventStore](https://eventstore.org/) for event persistence and event subscriptions
* [Redis](https://redis.io/) as a read model

## Docker

Install [docker](https://www.docker.com/) and [docker-compose](https://docs.docker.com/compose/) and the run the following command to start the environment.

```sh
docker-compose up
```

### Check everything is running

#### EventStore

Open [EvenStore Admin Console](http://localhost:2113). You should see a login screen. You can log in the console by using the defaults username and password.

* username: `admin`
* password: `changeit`

#### Redis

First you need to install Redis CLI. The easiest way for that is to use [npm](https://www.npmjs.com/).

```sh
npm install -g redis-cli
```

Look [here](https://redislabs.com/blog/get-redis-cli-without-installing-redis-server/) for more information.

```sh
rdcli -h localhost -p 6379
```

You should get a prompt

```sh
localhost:6379>
```

You can test that you can set and get from Redis

```sh
localhost:6379> set Foo Bar
OK
localhost:6379> get Foo
Bar
localhost:6379>
```

To exit the prompt, just type `exit`.
