sort filename
默认第一列排序

sort filename -t ":"
分隔符 :

sort filename -t ":" -k 4
:分隔符分割，按第四列排序

sort filename -t ":" -k 3 -n
-n 按照数字进行排序

sort filename -t ":" -k 3 -n -r
-r 逆序排序

sort filename -t ":" -k 3 -h
-h 将数据按照单位转换后排序，K，M，G等，不能与-n同时使用

sort filename -t ":" -k 3 -n -u
-u 去重


sort filename -t ":" -k 3 -n -o filename
-o 将结果写入文件
