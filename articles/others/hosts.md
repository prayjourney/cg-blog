# 详述`hosts`文件的作用及修改`hosts`文件的方法

## 1 什么是`hosts`文件？


　　`hosts`是一个没有扩展名的系统文件，其基本作用就是将一些常用的网址域名与其对应的 IP 地址建立一个关联“ 数据库 ”。当用户在浏览器中输入一个需要登录的网址时，系统会首先自动从`hosts`文件中寻找对应的 IP 地址，一旦找到，系统就会立即打开对应网页，如果没有找到，则系统会将网址提交 DNS 域名解析服务器进行 IP 地址的解析。

## 2 `hosts`文件的作用


### 2.1 加快域名解析


　　对于经常访问的网站，咱们可以通过在`hosts`文件中配置域名和 IP 的映射关系，提高域名的解析速度。由于有了映射关系，当咱们输入域名后，计算机就能够快速解析出 IP 地址，而不用请求网络上的 DNS 服务器。

### 2.2 构建映射关系


　　在很多单位中，都会有自己局域网，而且还会有不同的服务器提供给公司的成员使用。但由于局域网中一般很少架设 DNS 服务器，因此在访问这些服务器时，就需要输入难记的 IP 地址，这对大家来说相当麻烦。因此，咱们可以分别给这些服务器取个容易记住的名字，然后在`hosts`文件中建立 IP 映射，这样在以后访问的时候，只要输入这个服务器的名字就 OK 啦！

### 3.3 屏蔽垃圾网站


　　现在有很多网站，在不经过咱们同意的时候，就将各种各样的插件安装到咱们的计算机中，其中不乏病毒和木马。对于这些网站，咱们就可以利用`hosts`文件把这些网站的域名映射到一个错误的 IP 或本地计算机的 IP 地址上，这样就可以达到禁止访问的目的啦！

## 4 修改`hosts`文件的方法


由于 hosts 文件属性系统文件，因此需要管理员权限才能对其进行修改。

 - **第一种方法**：先将权限修改成管理员权限，然后在对其进行修改。
 - **第二种方法**：先将`hosts`文件复制到桌面，这时就不需要管理员权限了，因此可以对其进行修改了，等修改之后，在将其拖回原目录，替换就可以啦！

在 iOS 系统中中，`hosts`文件的位置为：`~/private/etc`

在 Windows 系统中，`hosts`文件的位置为：`C:\Windows\System32\drivers\etc`

**`hosts`文件修改示例：**

```
202.108.22.5 www.baidu.com
```
如上所示，咱们在本地的`hosts`文件中，将百度的 IP 地址与百度的域名建立了映射关系，也就起到了“加快域名解析”的作用，因为不需要再去请求 DNS 服务器啦！此外，如果咱们想要对其进行注释的话，直接在前面加`#`符号就可以，例如：
```
#202.108.22.5 www.baidu.com
```










