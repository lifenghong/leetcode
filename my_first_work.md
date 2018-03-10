## 题目  
 > Write a program to find the node at which the intersection of two singly linked lists begins.
  
## 示例 

``` 
A:          a1 → a2
                   ↘
                     c1 → c2 → c3
                   ↗            
B:     b1 → b2 → b3
```

## 分析：

#### 运用链表，若两个单独链接的列表都为空，无交集；重点在于判断不为空的情况，遍历链表寻找节点相交，（但刚开始我认为只是数字相同即可，所以试了几次也没有出来）后来有具体分析：
```
A:          a1 → a2
                   ↘
                     c1 → c2 → c3
                   ↗            
B:     b1 → b2 → b3
   a1 a2 c1 c2 c3 b1 b2 b3 c1 c2 c3
   b1 b2 b3 c1 c2 c3 a1 a2 c1 c2 c3
```
## 代码：
```C++
/**
* Definition for singly-linked list.
* struct ListNode {
*     int val;
*     ListNode *next;
*     ListNode(int x) : val(x), next(NULL) {}
* };
*/
class Solution {
public:
    ListNode *gNode(ListNode *headA, ListNode *headB) 
{
    ListNode *p1 = headA;
    ListNode *p2 = headB;
    if(p1!=p2)
    return NULL;
    else
    if(p1!=NULL&&p2!=NULL&&p1!=p2)
    {
    	p1=p1->next;
    	p2=p2->next;
    	if(p1==p2)
    	return p2;
    	if(p1=NULL)
    	p1=headA;
    	if(p1=NULL)
    	p2 = headB;
    }
    return p1;
};
```
## 总结：
#### 因为链表这一块比较薄弱，所以在试着联系指针链表还有结构体这一块，最近会逐步练习，慢慢由简入难。
