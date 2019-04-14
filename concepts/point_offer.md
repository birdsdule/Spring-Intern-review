剑指offer
===
1.[二维数组中的查找](https://www.nowcoder.com/practice/abc3fe2ce8e146608e868a70efebf62e?tpId=13&tqId=11154&tPage=1&rp=1&ru=/ta/coding-interviews&qru=/ta/coding-interviews/question-ranking)<br>
* 暴力搜索，不做赘述
* 对比每一行的头和尾，如果不在区间内直接跳过，如果在区间内(大于等于头，小于等于尾)则挨个扫描其内元素
* 创建一个行列坐标，从右上角开始。如果目标小于当前值，说明说明当前一列都不存在target，因为下面的都比上面的大，所以列坐标减一。如果目标大于当前值，说明这一行都不存在target，因为左面比右面的小，所以行坐标加一。如果等于目标则返回True<br>
2.[替换空格](https://www.nowcoder.com/practice/4060ac7e3e404ad1a894ef3e17650423?tpId=13&tqId=11155&rp=1&ru=/ta/coding-interviews&qru=/ta/coding-interviews/question-ranking)<br>
* python比较简单，直接split再join就可以。但是会出现开头一个空格的情况，所以还是存到一个list里替换比较好
* java 直接扫描str，使用str.charAt(i)获得每个字符，如果是空格则str.replace(i,i+1,"%20")<br>
3.[从尾到头打印链表](https://www.nowcoder.com/practice/d0267f7f55b3412ba93bd35cfa8e8035?tpId=13&tqId=11156&rp=1&ru=/ta/coding-interviews&qru=/ta/coding-interviews/question-ranking)<br>
* python:递归或者挨个写入再reverse或者挨个写到头上
* java: 建立一个栈，然后挨个扫描将val写入栈，最后再推出add到arraylist里<br>
4.[重建二叉树](https://www.nowcoder.com/practice/8a19cbe657394eeaac2f6ea9b0f6fcf6?tpId=13&tqId=11157&rp=1&ru=/ta/coding-interviews&qru=/ta/coding-interviews/question-ranking)<br>
* 前序遍历的第一位作为根，然后把中序遍历以这个值作为分界线分开，左边为左树的中序遍历，右边为右树的中序遍历。开始递归，记得不要多次pop()<br>
5.[用两个栈实现队列](https://www.nowcoder.com/practice/54275ddae22f475981afa2244dd448c6?tpId=13&tqId=11158&rp=1&ru=/ta/coding-interviews&qru=/ta/coding-interviews/question-ranking)<br>
* 栈是先进后出，队列是先进先出，所以要把栈中元素按出栈顺序倒入另一个栈中，就可实现栈的反向。每次pop的时候判断一下，如果stack2为空，则把stack1中的数据倒入<br>
6.[旋转数组的最小数字](https://www.nowcoder.com/practice/9f3231a991af4f55b95579b44b7a01ba?tpId=13&tqId=11159&rp=1&ru=%2Fta%2Fcoding-interviews&qru=%2Fta%2Fcoding-interviews%2Fquestion-ranking&tPage=1)<br>
* 使用三个指针来进行类似二分法or快排的操作，当左指针的数字大于等于右指针的数字是循环，如果中间的值大于左指针，说明还在左边的递增区间，start右移变成mid，然后重新计算mid(start+end)//2。
* 如果中间的值小于右指针，说明mid在右边的递增区间，则右指针左移。直到左右指针相差一个时，说明右指针在左边递增序列的下一个，则是最小值。还有就是如果三个指针的值完全一样，就顺序遍历。<br>
7.[斐波那契数列](https://www.nowcoder.com/practice/c6c7742f5ba7442aada113136ddea0c3?tpId=13&tqId=11160&rp=1&ru=/ta/coding-interviews&qru=/ta/coding-interviews/question-ranking)<br>
* 递归或者循环，递归太慢，dp好一些<br>
8.[跳台阶](https://www.nowcoder.com/practice/8c82a5b80378478f9484d87d1c5f12a4?tpId=13&tqId=11161&rp=1&ru=/ta/coding-interviews&qru=/ta/coding-interviews/question-ranking)<br>
* 和斐波那契额数列一样，当前位置的可能方法为前一级一步跳过来和前前级一步跳两级过来<br>
9.[变态跳台阶](https://www.nowcoder.com/practice/22243d016f6b47f2a6928b4313c85387?tpId=13&tqId=11162&rp=1&ru=/ta/coding-interviews&qru=/ta/coding-interviews/question-ranking)<br>
* 一样，每一级的可能是前面所有的和再+1，化简就是前一位的两倍<br>
10.[矩形覆盖](https://www.nowcoder.com/practice/72a5a919508a4251859fb2cfb987a0e6?tpId=13&tqId=11163&rp=1&ru=/ta/coding-interviews&qru=/ta/coding-interviews/question-ranking)<br>
* 斐波那契数列问题变形<br>
