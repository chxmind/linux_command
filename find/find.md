
find . -name filename
在当前目录查找文件名

find . -iname filename
在当前目录查找文件名，大小写不敏感

find ~ -empty
查找所有大小为空的文件


find ~ -size 7k
查找等于7k的文件

find ~ -size +6k
大于6k
find ~ -size -6k
小于6k

find ~ -size +6k -size -8k
大于6k
小于8k