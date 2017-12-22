# Mac 下 PHPStorm 配置 Web Server

> 不想把PHP文件放在本机的Apache根目录下运行, 希望无论PHP文件放在哪个目录下都能使用Web Server 运行. 

> 每个Project需要单独配备一次


> 参考: [phpstorm 配置 webserver ，配置根目录](http://makaidong.com/cythical-l-zc/8966_12576338.html)

----

## 步骤一: PHP CLI Interpreter 配置

> CLI Interpreter 命令行形式的PHP解释器

File -> Default Setting -> Languages & Frameworks -> PHP

![Languages & Frameworks -> PHP](images/webserver01)

<br>

![PHP CLI](images/webserver02)

![PHP CLI Success](images/webserver03)


### 解决php.ini不存在问题

> php.ini是PHP解释器的初始文件, 负责配置PHP的各种行为和功能。

> 使用phpinfo()函数查看的就是php.ini文件的内容.

> php.ini.default 是 php.ini文件的模板, 是为了防止php.ini文件改动后需要恢复默认设置而保留的文件. 可以直接复制php.ini.default文件用于php.ini文件.

![php.ini](images/php01)

![php.ini](images/php02)


```
注意:
	配置好php.ini文件后, 需要重新配置PHPStorm 中的 CLI Interpreter, 之前配置好的无法识别到php.ini文件.

```

-----

## 步骤二: PHP Built-in Web Server

Run -> Edit Configurations

![Built-in Web Server](images/build01)

![Built-in Web Server](images/build02)

----

## 步骤三: Deployment 

> 从菜单栏进入配置页面  和 `commond` + `,`  进入配置页面稍有不同.

使用 `commond` + `,`  进入配置页面

![deployment](images/deployment01)

![deployment](images/deployment02)

![deployment](images/deployment03)

![deployment](images/deployment04)

-----

## 测试


![测试](images/final01)

![测试](images/final02)

![测试](images/final03)


### 结果

![成功](images/success)


