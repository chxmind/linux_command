awk '{print}' filename
仅打印


awk -F ':' '{print $1}' filename
-F ':' 以冒号拆分
$1 打印第一列


akw -F ':' 'NR==2{print $2}' filename
NR==2 第2行


akw -F ':' 'NR==1, NR==3{print $2}' filename
NR==1,NR==3 从第一行到第三行


awk -F ':' 'NF=1{print}' filename
NF=1 只处理前1列，注意是一个等于号


awk -F ':' '/xiaoli/{print}' filename
/xiaoli/ 正则表达时，匹配xiaoli的行


awk -F ':' 'BEGIN{printf "xuehao\txingming\tyuwen\tyingyu\tshuxue\n"} {printf "%d\t%s\t%d\t%d\t%d\n", $1,$2,$3,$4,$5}' filename
BEGIN 前置操作


awk -F ':' 'BEGIN{printf "xuehao\txingming\tyuwen\tyingyu\tshuxue\n"} {printf "%d\t%s\t%d\t%d\t%d\n", $1,$2,$3,$4,$5} END{print "this is a table"}' filename
END 追加一行

