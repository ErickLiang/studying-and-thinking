# -*- coding:utf-8 -*-
import random

'''
    给定一个无序，不重复的1-10000的列表，随机删除两个
    找到删除的两个数    
'''

maxRange = 10000

def findDelNum(list1,list2):
    # 未删的为1 删的为2
    pos = []
    for index in range(0,maxRange):
        if index == len(list2) -1:
            pos.append(index)
        if list2[index] != list1[index]:
            pos.append(index)
            list2.insert(index,list1[index])
    return pos

def main():
    # 生成1-10000的列表，无序，唯一
    my_list = list(range(maxRange))
    random.shuffle(my_list)

    #随机删除两个
    new_list = my_list.copy()
    new_list.pop(random.randint(0,maxRange))
    new_list.pop(random.randint(0,maxRange - 1))

    #找出删除的数
    res = findDelNum(my_list,new_list)
    print(my_list[res[0]],my_list[res[1]])

if __name__ == '__main__':
    main()
