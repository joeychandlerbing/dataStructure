# 数据结构和算法
## 排序
  对于冒泡排序和选择排序来说，数据状况对这两种排序的时间复杂度是没有影响的，即使数据有序但仍要走两种排序的流程，只是不交换，对于插入排序如果数组有序时间复杂度为O(n),最坏的情况时间复杂度为o(n^2)。
## 对数器
**对数器的好处:**
- 验证自己的算法是否正确
- 较快的检验自己的算法错误在哪里
- 较快的检验贪心算法而不是证明

**对数器所需:**
1. 产生测试用例的产生器,长度随机，值随机，用于测试
2. 准备一个绝对正确不要求时间复杂度的方法
3. 大样本测试
4. 验证自己写的算法是否与绝对正确的方法的结果是否一致
## 递归
本质上是通过系统栈实现的。
master公式:T(N)=aT(N/b)+O(n^d)
1. 如果log(b,a)>d,复杂度为O(N^log(b,a));
2. 如果log(b,a)=d,复杂度为O(N^d *logN);
3. 如果log(b,a)<d,复杂度为O(N^d);
## 小和问题
在一个数组中，每一个元素左边比当前元素值小的元素值累加起来，叫做这个数组的小和例如：[2,3,4,1,5]
2左边比2小的元素：无
3左边比3小的元素：2
4左边比4小的元素：2，3
1左边比1小的元素：无
5左边比5小的元素：2,3,4,1
小和small_sum = 2 + 2 + 3 + 2 + 3 + 4 + 1 = 17
可理解为从当前数开始，找到右侧所有比当前数大的数，累加起来。
1. 在每个索引处遍历左边，找到所有比它小的数。时间复杂度为O(N^2)
2. 使用归并排序,在排序的过程中计算小和。
*归并排序*:将数组划分成左右两个部分，先将左数组排好序，再将右数组排好序，再左右部分进行外排。
**得到合并过程产生的小和，再加上两个子序列的小和之和，如果不加上左右两序列的小和，得到的小和只是最后一部的小和**

 

