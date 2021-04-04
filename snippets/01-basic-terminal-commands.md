// basic commands which can be usefull in day to day for development
> for below commands we have considered default username as `ubuntu` and ipaddress as `12.12.12.12`

```sh
  // to get login in remote server
  sudo ssh -i mysecreatfile.pem ubuntu@12.12.12.12

  // change ownership for file and folder,  -R stands for `recursive`
  sudo chown ubuntu:ubuntu file or sudo chown ubuntu:ubuntu -R directory

  // copy files to remote server
  scp -i mysecreatfile.pem filename.txt ubuntu@12.12.12.12:~/home/backup

  // copy files from remote server, -P stands for port number for ssh if changed
  sudo scp -i mysecreatfile.pem -P 9670 ubuntu@12.12.12.12:~/home/backup/filename.text .

  // to get information about diskspace
  df
  // to check disksize of specific folder or file
  du -sh file/directory or du -sh $(ls) // gives sizeinfo about all files and folders of directory

  // after setup new ubuntu server install below required packages
  sudo apt-get update
  sudo apt-get upgrade
  sudo apt-get install -y wget unzip fontconfig locales gconf-service libasound2 libatk1.0-0 libc6 libcairo2 libcups2 libdbus-1-3 libexpat1 libfontconfig1 libgcc1 libgconf-2-4 libgdk-pixbuf2.0-0 libglib2.0-0 libgtk-3-0 libnspr4 libpango-1.0-0 libpangocairo-1.0-0 libstdc++6 libx11-6 libx11-xcb1 libxcb1 libxcomposite1 libxcursor1 libxdamage1 libxext6 libxfixes3 libxi6 libxrandr2 libxrender1 libxss1 libxtst6 ca-certificates fonts-liberation libappindicator1 libnss3 lsb-release xdg-utils

  // to increase max_map_count, it is usefull incase of `elasticsearch` in ubuntu machines
  sudo sysctl -w vm.max_map_count=262144
  sysctl vm.overcommit_memory = 1

  // to set env variable in system
  export ENV_NAME='environment value'
  // or edit /etc/environment and update file with env variable for permanently.

  // basic and usefull curl commands
  curl -XGET http://12.12.12.12:4000/ or curl http://12.12.12.12:4000
  curl -XPOST -c "data='hello world'" http://12.12.12.12:4000/ -d '{data: \"hello word\"}'
  //  -c stands for cookie
  curl -XPUT -H "Content-Type: application/json" http://12.12.12.12:4000/ -d '{data: "hello word"}'
  curl -XDELETE http://12.12.12.12:4000/user/23

```

**Note
before using `mysecreatfile.pem` for ssh purpose, change file permission to `400`
```sh
 chmod 400 mysecreatfile.pem
```

