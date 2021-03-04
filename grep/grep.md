grep -i 
不区分大小写

grep -n 
显示行号

grep 'linux.*' filename   
简单正则表达式

grep  -F 'linux.*' filename     
禁止正则表达式

grep "linux | LINUX" filename   
竖线是扩展正则，无法过滤

grep -E "linux | LINUX" filename  
使用扩展正则

grep -c "linux" filename
只统计行数，不显示内容

grep -o "linux" filename
只显示匹配内容，不是整行内容

