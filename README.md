# mongodb-js

This tutorial follows these youtube

- https://www.youtube.com/watch?v=a3H9rIj07sk&list=PL4cUxeGkcC9h77dJ-QJlwGlZlTd4ecZOA&index=15
- https://www.youtube.com/watch?v=gGNquGHqpNI&list=PL4cUxeGkcC9h77dJ-QJlwGlZlTd4ecZOA&index=16
- https://www.youtube.com/watch?v=5a6h41PVsD0&list=PL4cUxeGkcC9h77dJ-QJlwGlZlTd4ecZOA&index=17

## Where is my mongodb database ?

It is running on an ubuntu server with an ip address of 192.168.0.10

Tutorial : https://www.youtube.com/watch?v=SNgaUYu5o1o 

```
user@ubuntu:~$ sudo systemctl status mongod.service
[sudo] password for user:
● mongod.service - MongoDB Database Server
     Loaded: loaded (/usr/lib/systemd/system/mongod.service; disabled; preset: enabled)
     Active: active (running) since Sat 2025-03-22 00:32:19 UTC; 19h ago
       Docs: https://docs.mongodb.org/manual
   Main PID: 4365 (mongod)
     Memory: 206.7M (peak: 270.6M)
        CPU: 4min 5.219s
     CGroup: /system.slice/mongod.service
             └─4365 /usr/bin/mongod --config /etc/mongod.conf

Mar 22 00:32:19 ubuntu systemd[1]: Started mongod.service - MongoDB Database Server.
Mar 22 00:32:19 ubuntu mongod[4365]: {"t":{"$date":"2025-03-22T00:32:19.886Z"},"s":"I",  "c":"CONTROL",  "id":7484500, "ctx":"main","msg":"Environment variable MONGODB_CONFIG_OVERRIDE_NOFORK == 1, overriding \>
```

```
user@ubuntu:~$ sudo ss -tuln
Netid               State                 Recv-Q                Send-Q                                    Local Address:Port                                Peer Address:Port               Process
udp                 UNCONN                0                     0                                            127.0.0.54:53                                       0.0.0.0:*
udp                 UNCONN                0                     0                                         127.0.0.53%lo:53                                       0.0.0.0:*
udp                 UNCONN                0                     0                                    192.168.0.10%ens18:68                                       0.0.0.0:*
tcp                 LISTEN                0                     4096                                      127.0.0.53%lo:53                                       0.0.0.0:*
tcp                 LISTEN                0                     4096                                         127.0.0.54:53                                       0.0.0.0:*
tcp                 LISTEN                0                     4096                                            0.0.0.0:27017                                    0.0.0.0:*
tcp                 LISTEN                0                     4096                                                  *:22                                             *:*
user@ubuntu:~$
```

## How to run a web server

`npm run server`

```
Node.js v20.12.2
[nodemon] app crashed - waiting for file changes before starting...
[nodemon] restarting due to changes...
[nodemon] starting `node app.js`
app listening on port 3000
```

## How to view data on web browser

http://localhost:3000/books

![Screenshot (79)](https://github.com/user-attachments/assets/faafa9a7-c948-4dca-99ef-ceb0c30c94c8)


## Reference

- https://www.mongodb.com/try/download/community ( install it on ubuntu server )
- https://www.mongodb.com/try/download/shell ( run it on ubuntu server
- https://www.mongodb.com/try/download/compass ( run it on windows or anything server with GUI )


