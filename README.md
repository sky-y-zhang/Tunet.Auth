# Tunet.Auth

tunetAuth is a python script to login https://auth4.tsinghua.edu.cn and(or) https://auth6.tsinghua.edu.cn
this script use selenium firefox headless to login

selenium firefox need geckodriver, you can download from: https://github.com/mozilla/geckodriver/releases, 
uncompress and put into PATH.


```bash
// do login
tunetAuth 

// do logout
tunetAuth -o
```
tunetAuth will use ~/.TsinghuaNet/netTHUAuth
```json
{
  "username": "username",
  "password": "password"
}
```

if you want login in automatically, you can
```bash
* * * * * (ping -c 1 -W 1 info.tsinghua.edu.cn|| tunetAuth) >/dev/null 2>&1 
```
and add it to crontab

if you want to connect Internet, please see 
https://github.com/guzhaoyuan/net.tsinghua.git
```bash
* * * * * (ping -c 1 -W 1 baidu.com || netTHU -o) >/dev/null 2>&1 
```
Enjoy it.
