# python-AI-6-
python+AI笔记(6)
# 一阶-三章-判断语句综合案例
import random
num=random.randint(1,10)

guess_num=int(input("请输入您要猜测的数字:"))

#2.通过if判断语句进行数字的猜测
if guess_num==num:
    print("恭喜，第一次就猜中了")
else:
    if guess_num>num:
        print("你猜的数字大了")
    else:
        print("你猜测的数字小了")
    guess_num=int(input("请再次输入你要猜测的数字:"))

    if guess_num==num:
        print("恭喜，第二次猜中了")
    else:
        if guess_num>num:
            print("你猜的数字大了")
        else:
            print("你猜测的数字小了")
            
        guess_num=int(input("请再次输入你要猜测的数字:"))
        if guess_num==num:
            print("第三次猜中了)
        else:
            print("三次机会用完了，没有猜中")

# 一阶-四章- while循环的基础应用
i=0
while i<100:  #条件判断语句的结果必须是bool类型
    print("bala")
    i+=1

# 一阶-四章- 1-100求和讲解
sum=0
i=1
while i<=100:
    sum+=i
    i+=1
print(f"1-100累加的和是：{sum}")

# 一阶-四章- while循环猜数字案例
#获取范围在1-100中的随机数字
import random
num=random.randint(1,100)
#定义一个变量记录猜测次数
count=0
#通过一个bool类型的变量，做循环是否继续的标记
flag=True
while flag:
    guess_num=int(input("请输入你猜测的数字:"))
    count+=1
    if guess_num==num:
        print("猜中了")
        #设置为Flase就是终止循环的条件
        flag=False
    else:
        if guess_num>num:
            print("你猜的大了")
        else:
            print("你猜的小了")

print(f"你总共猜测了{count}次")

# 一阶-四章-while循环的嵌套应用
#外层 表白100天的控制
#内层 每天表白都送10支玫瑰花的控制
i=1
while i<=100:
    print(f"今天是第{i}天，准备表白。。。")
    #内层循环控制变量
    j=1
    while j<=10:
        print(f"送给小妹的第{j}支玫瑰")
        j+=1
    print("bala")
    i+=1
print(f"坚持到第{i-1}天，成功")
