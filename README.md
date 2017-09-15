docker配置
>一些命令
~~~
$ docker load < xpface.iot-sw.net.rar  //解压rar文件并build镜像
$ docker run -d --restart=always -p 80:80 -v /data/www:/data/www xpface.iot-sw.net
$ docker ps
~~~
=============
> 1.挂载目录

~~~
      本地目录                 Docker目录
"/root/workplace/www/:/data/www/pworks.iot-sw.net/",
"/root/workplace/conf/:/data/conf/",
"/root/workplace/log/:/data/log/",
"/root/workplace/pears/:/usr/lib/php/pear/parking_meter/",
"/root/workplace/nginx/:/etc/nginx/conf.d/"

~~~
>  2.work.zip解压后的文件需要放在 ~ 目录
~~~
  work.zip
~~~

3.挂载命令

~~~
docker run -d --name work_api -v /root/workplace/www/:/data/www/pworks.iot-sw.net/ -v /root/workplace/conf/:/data/conf/ -v /root/workplace/log/:/data/log/ -v /root/workplace/pears/:/usr/lib/php/pear/parking_meter/ -v /root/workplace/nginx/:/etc/nginx/conf.d/ -p 8888:80 pworks.iot-sw.net

~~~

~~~
$docker exec -it 容器名 bash //进入容器内
$docker inspect 容器名 //查看容器的详细信息
~~~
