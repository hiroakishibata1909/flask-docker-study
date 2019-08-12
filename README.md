# How to use

## Install Docker for Mac

https://qiita.com/kurkuru/items/127fa99ef5b2f0288b81

## Execute Flask application
0. Confirm necessary files
```
$ git clone https://github.com/hiroakishibata1909/flask-docker-study.git

$ cd Docker/
$ ls -la
total 24
drwxr-xr-x 3 ec2-user ec2-user 4096 Aug 12 02:54 .
drwxr-xr-x 3 ec2-user ec2-user 4096 Aug 12 02:54 ..
-rw-r--r-- 1 ec2-user ec2-user 1762 Aug 12 02:54 app.py
-rw-r--r-- 1 ec2-user ec2-user  415 Aug 12 02:54 Dockerfile
-rw-r--r-- 1 ec2-user ec2-user   13 Aug 12 02:54 requirements.txt
drwxr-xr-x 2 ec2-user ec2-user 4096 Aug 12 02:54 uploads
$ pwd
/home/ec2-user/flask/Docker
```

1. Create docker image
```
$ docker build -t flask-fargate:ver3 .

$ docker images flask-fargate:ver3
REPOSITORY          TAG                 IMAGE ID            CREATED             SIZE
flask-fargate       ver3                93dbd8d03df9        25 seconds ago      435MB
```

2. Execute docker process (Execute python program)
```
$ docker run -d -p 5000:5000 flask-fargate:ver3
275bf3446449991a978ee638c438d8df4758fb027568ccf5988b7bc3ee802922 

$ docker ps
CONTAINER ID        IMAGE                COMMAND             CREATED             STATUS              PORTS                    NAMES
275bf3446449        flask-fargate:ver3   "python app.py"     2 minutes ago       Up 2 minutes        0.0.0.0:5000->5000/tcp   quizzical_brattain
```

3.  Access Flask Web application on blowser
```
http://localhost:5000
```

4. Stop docker process (Stop python program)
```
$ docker stop 275bf3446449
```

# Flask Reference

## Flask on EC2
install flask to EC2 instance

https://dev.classmethod.jp/server-side/language/flask-for-python-on-ec2/

## Flask on Docker(ECS)

https://qiita.com/oyngtmhr/items/45a0d3158e6dccb0882d
http://containertutorials.com/docker-compose/flask-simple-app.html


## CodeDeploy

https://dev.classmethod.jp/server-side/language/flask-for-python-on-ec2/

## Web Domain
https://qiita.com/yamanoku/items/c4f9c28d79f981afc40f

# GAN  Reference
https://qiita.com/hrs1985/items/050acb15ce33675f07ec
https://qiita.com/hrs1985/items/926f9c4e635aac659675#_reference-8ce0bd626428b5d00bcc  
https://qiita.com/pekatuu/items/d9bd133b453c314ab31d

## Keras-GAN
https://github.com/eriklindernoren/Keras-GAN
https://github.com/eriklindernoren/Keras-GAN/tree/master/cyclegan