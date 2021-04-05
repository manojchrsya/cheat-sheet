#### Create custom commands in ubuntu or mac

> Sometimes we may have to use command in order to execute script or build project.
> we also use some commands in case of services like `docker`, `nginx`, `apache` etc.

for example, suppose we have to stop and start docker container's of project
```sh
 // we can use `&&` oprator for multiple commands and execute in one go.
 sudo docker-compose stop && sudo docker-compose up -d
```

now, we have few options
- we can write long command every time in order to restart the containers.
- we can use `cntrl + r` to search the last used command.
- you can also use `up` and `down` arrow to find the exact command. 😌

or better we can use `alias` in our system. ok now what is this `alias`?

usually `alias` are use to create some custom shortcut to execute your set of commands.
to get list of all available `alias`, directly execute `alias` in **terminal**.




