test.txt
```
I love linux
I LOVE Linux
I Love LINUX
good good study
day day up
```

sed -n "/love/p" test.txt
-n 只打印匹配到的行
/love/ 匹配的字符串
/p  打印命令
text.txt    文件名


sed -n -e "/love/p" -e "/LOVE/p" test.txt
-e 多个条件


sed -r 扩展正则表达式
sed -n -r "/love|LOVE/p" test.txt

/pattern/cmd
只要匹配到的行都执行命令

/pattern1/,/pattern2/cmd
从匹配到模式1行开始，到匹配到模式2的行结束，
中间的行(包括开始结束行)执行命令


sed "/I/a xxxx" test.txt
/a  换行追加xxxx

sed "/I/i YYYY" test.txt
/i 在上一行追加

sed "s/old/new/" test.txt
s/ 替换old成new

sed "s/old/new/g" test.txt
/g 每一行每一个都替换
