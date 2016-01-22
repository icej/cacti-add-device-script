结合cacti官方提供的脚本,做了更适合批量导入主机及监控服务的操作.
提供IP列表制定需要增加的服务别名就可以批量添加。
(run with cacti office scripts, it can easy add many servers and monitor services to cacti)
```
示例:
php xpdinitcacti.php -f server.txt -t linux -p xpd -g mysql
-f Ip列表,一行一个ip( ip list, one line one ip)
-t 相当于主机模版的别名,主机使用linux模版,linux模版对应的主机id号,用--list-graph-templates获得,记id号不容易,记别名就容易多了 (a server template alias)
-p 产品线名称前缀,产生的主机名称就会是:产品线名称-服务-ip (prefix)
-g 监控的服务,自己定义的服务别名,对应了一堆自己可用的监控服务模版Id号,比如mysql代表几个mysql监控服务常用的模版(services alias)
```


原文:http://hi.baidu.com/icej/blog/item/16a56ff0affdd2c97831aaa4.html