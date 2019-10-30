<<注意运行目录>>

启动进程：start nginx
关闭进程：./nginx.exe -s quit
查看进程：tasklist -fi "imagename eq nginx.exe"
杀掉进程：taskkill -im nginx.exe -f


window下nginx注册成服务：
nginx-service.exe
nginx-service.xml
nginx-service.exe.config
运行./nginx-service.exe install

服务启动后正常，但是关闭存在问题：
使用./nginx.exe 启动后，使用./nginx.exe -s quit只能关闭一个进程，另外一个进程还在运行。
只能使用start nginx 启动服务器
Image Name                     PID Session Name        Session#    Mem Usage
========================= ======== ================ =========== ============
nginx.exe                   196048 Services                   0      7,336 K
nginx.exe                   196092 Services                   0      7,800 K

Image Name                     PID Session Name        Session#    Mem Usage
========================= ======== ================ =========== ============
nginx.exe                   195976 Services                   0      7,556 K


只能手动启动、关闭进程：
nginx-start.bat
nginx-stop.bat


