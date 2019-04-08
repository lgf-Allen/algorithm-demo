# algorithm-demo
The repository includes some algorithm problems and their solutions.

## 1. 集合问题

- 15个教徒和15个非教徒在深海上遇险，必须将一半的人投入海中，其余的人才能幸免遇难，于是想了一个办法:30个人围成一圆圈，从第一个人开始依次报数，每数到第九个人就将他扔入大海，如此循环进行直到仅余15个人为止。问怎样排法，才能使每次投入大海的都是非教徒。

- 解法：

```
public static void main(String[] args) {
        List<Integer> person = new ArrayList<>();
        for (int i = 1; i <= 30; i++) {
            person.add(i);
        }
        int callNo = 1;
        // list中元素不大于15
        while (person.size() > 15) {
            Iterator<Integer> iterator = person.iterator();
            while (iterator.hasNext()){
                Integer no = iterator.next();
                // 遇到为9时从数组中剔除出去
                if(callNo++ == 9){
                    System.out.println(no);
                    iterator.remove();
                    callNo = 1;
                }
            }
        }
    }
```
## 2. 链表
### 2.1 链表分类
 - 单链表
 - 双链表
 - 有序链表
 - 双向链表
### 2.2 常用链表算法
 - 单链表反转
 - 链表中环的检测
 - 两个有序的链表合并
 - 删除链表倒数第n个节点
 - 求链表的中间节点



