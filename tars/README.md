解决ubuntu shell脚本中含有source命令运行时提示 source: not found

测试： 
运行 ls -l /bin/sh 后显示/bin/sh -> dash 
这说明是用dash来进行解析的。

解决方案： 
命令行执行：dpkg-reconfigure dash（需要root权限） 
在界面中选择no 
再运行ls -l /bin/sh 后显示/bin/sh -> bash

最后测试shell脚本，可以正常使用！
