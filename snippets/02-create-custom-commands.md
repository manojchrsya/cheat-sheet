#### Create custom commands in ubuntu or mac

> Sometimes we may have to use command in order to execute script or build project.
> we also use some commands while using other services like `docker`, `nginx`, `apache` etc.

for an example, suppose we have to stop and start docker container's of a project.
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


to create new `alias`,we need to update `.bashrc` file or if you are using `oh-my-zsh` then edit `.zshrc` file.

```sh
vim ~/.zshrc
// add below entry in file
restart-project = "cd ~/project-path && sudo docker-compose stop && sudo docker-compose up -d"

//  after save and exit from file
source ~/.zshrc // to make an effect new created alias
```

now we just have to execute `restart-project` in terminal.
