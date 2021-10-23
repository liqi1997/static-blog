---
title: "冒泡排序"
date: 2021-10-22T22:04:13+08:00
---

## 简介
冒泡排序从数组第一个元素开始，不断跟后一个元素进行比较，如果前面的数值大于后面的数值，则交换位置，然后接着从第二个元素开始，一直向后比较，不断循环至数组倒数第二个元素，完成一轮循环后，数组最后一个元素则是最大值。

接着从头开始进行第二轮循环，一直到数组倒数第三个元素。

循环此过程，直到只剩第一个元素和第二个元素进行比较。

冒泡排序的特点是每一轮循环都是将当前剩下元素中最大的元素找出来，如果不巧首轮循环中，最大的元素就是第一个元素，则该元素会一直移动到最后一个元素，像水冒泡一样冒出来。

## 实现代码
```c
#include <stdio.h>

int main() {
    
    int list[5] = {100, 30, -42, 0, 80};
    int length = sizeof(list) / sizeof(int);
    for (int i = 0; i < length - 1; i++) {
        
        for (int j = 0; j < length - 1 - i; j++) {
            if (list[j] > list[j + 1]) {
                int temp = list[j + 1];
                list[j + 1] = list[j];
                list[j] = temp;
            }   
        }
        
    }
    
    for (int i = 0; i < length; i++) {
        printf("%d ", list[i]);
    }
    printf("\n");

    return 0;
}
```