docker配置
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
>  2.本地文件需要放在 ~ 目录
~~~
  work.zip
~~~

3.挂载命令

~~~
docker run -d --name work_api -v /root/workplace/www/:/data/www/pworks.iot-sw.net/ -v /root/workplace/conf/:/data/conf/ -v /root/workplace/log/:/data/log/ -v /root/workplace/pears/:/usr/lib/php/pear/parking_meter/ -v /root/workplace/nginx/:/etc/nginx/conf.d/ -p 8888:80 pworks.iot-sw.net

~~~
