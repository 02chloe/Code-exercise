

- [刷题笔记](#刷题笔记)
    - [刷题频次：](#刷题频次)
    - [Python 基本入门的网站：](#python-基本入门的网站)
    - [基本问题：](#基本问题)
    - [语法入门题目列表：](#语法入门题目列表)
    - [二分法](#二分法)
    - [多指针](#多指针)
    - [宽度优先搜索](#宽度优先搜索)
    - [二叉树与递归](#二叉树与递归)
    - [深度优先搜索](#深度优先搜索)
    - [数据结构](#数据结构)
- [ML Systems Design Interview Guide](#ml-systems-design-interview-guide)

 
# 概述：

DS面试（这里主要是指偏engineering的，非analytics）主要分为以下几个部分：Machine learning（包含ML case），statistics concept，coding（包括SQL和算法）， A/B testing（causal inference），Deep learning/NLP/CV/推荐系统等advanced topics（与简历project相关问题）。重要性排序大致是：ML>stat>Coding>AB test = DL/NLP> other topics. 
#### 参考
[短期快速上岸DS intern](https://www.1point3acres.com/bbs/forum.php?mod=viewthread&tid=846396&ctid=229383)
# 刷题笔记
- [胖头龙算法刷题笔记](https://www.1point3acres.com/bbs/forum.php?mod=viewthread&tid=678970&page=1&authorid=682747)
### 刷题频次： 
30 * 10 + 100 * 8 + 300 * 5 这样不仅学习效果更好，对于面试准备也更友善

### Python 基本入门的网站：
- [W3schools](https://www.w3schools.com/python/):这个自带iteractive的在线编译器，比较方便。
- [Tutorialspoint](https://www.tutorialspoint.com/python/index.htm):这个也差不多，没有编译器。
- [官方文档](https://docs.python.org/3/)：用来查询API的用法，很实用。
- [Google代码风格规范](https://google.github.io/styleguide/pyguide.html)：一开始会看不明白，几十题之后再回来读，然后自觉向规范靠拢。

### 基本问题：
1. 变量，基本数据类型，逻辑运算符号
2. 控制语句，if else
3. 循环结构，for, while, continue, break
4. 基本数据操作，int，float和常用的数学运算，不同数据类型之间的转换
5. 基本数据结构，理解hashmap，set，tree,  linked list的概念，理解Python 中 string，list，tuple，dict, set，linked list的增删改查
6. 高级数据结构，Counter, defaultdict, OrderedDict, queue, deque, stack, heap, bisect的概念和在python中的用法
7. 其他常见方法，sort, enumerate, map, filter, lambda
8. 函数的使用，参数的传递，引用的传递，递归的基本概念
9. 基本的面向对象，Class, Object，理解引用，deep copy的概念，通过自定义__lt__,  __gt__, __eq__来控制数据结构的排序。

### 语法入门题目列表：

这些题主要是帮助熟悉语法，所以没有用特别高的优先级。(Lintcode)

37. [Reverse 3-digit Integer](https://www.lintcode.com/problem/37/)
214. [Max of Array](https://www.lintcode.com/problem/214/)
283. [Max of 3 Numbers](https://www.lintcode.com/problem/283/)
146. [Lower to uppercase II](https://www.lintcode.com/problem/146/)
241. [String to Integer](https://www.lintcode.com/problem/241/)
449. [Char to Integer](https://www.lintcode.com/problem/449/)
463. Sort Integers
484. Swap Two Intergers in Array
485. Generate ArrayList with Given Size
225. Find Node in Linked List
466. Count Linked List Nodes
483. Convert Linked List to Array List
454. Rectangle Area
478. Simple Calculator
366. Fibonacci
632. Binary Tree Maximum Node
40. Implement Queue by Two Stacks
492. Implement Queue by Linked List
494. Implement Stack by Two Queues
495. Implement Stack

### 二分法
#### 朴素二分法
    必背：  
    704. Binary Search   

    核心：  
    34. Find First and Last Position of Element in Sorted Array  
    702. Search in a Sorted Array of Unknown Size 

    重点：  
    153. Find Minimum in Rotated Sorted Array  
    154. Find Minimum in Rotated Sorted Array II  
    278. First Bad Version  
    658. Find K Closest Elements
#### 条件二分法：
- 33,81; 4,74,162; 302,852

#### 答案二分法：
- 75,1283; 69,Lint-586,lint-183,lint-437,lint-438

### 基本问题：
1. 基本思想？（有序的数据，每次通过判断逻辑排除掉一部分的答案，直到触发终止条件）
2. 二分法实现模板（可以递归，可以迭代；一般以迭代为主）
3. 移动两个指针（start与end）的含义？移动条件是什么（筛选掉一部分数据的依据）？循环的截止条件？
4. 数据中是否有重复数字？对结果有什么影响？
5. 为什么你选择的模板中使用start < end 或者 start <= end 或者 start + 1 < end 作为终止条件？这样写是如何避免死循环的？不这么写在什么情况下会出现死循环？
6. 在处理逻辑中，当前结果>, <, = 目标值时分别如何处理？移动指针的依据是什么？
7. 循环退出后是否需要额外处理？
8. 如果遇到corner case根本没进主循环，你的代码是否能正常工作？
9. 为什么Java需要写 mid = start + (end - start) / 2 而 Python可以直接写 mid = (start + end) // 2 ？
10. 如何理解从基本的朴素二分，到相对复杂的条件二分，到更加抽象的答案二分？（在一个显性有序数组中一次砍掉一部分 -->  在一组有规律的数据上利用判断条件逐步缩小范围  -->  在一个有序的抽象模型里，利用不断的"猜测+检验"逐步逼近最终结果）

### 多指针
#### 数组
#### 链表
#### 区间
#### 回文串
#### 滑动窗口
#### 流
#### 前项和
#### 和差问题

#### 基本问题
1. 多指针是一个非常广泛的概念，并不是一个固定的算法。但基本上是通过一些变量的控制与循环把问题的复杂度控制在一两层for循环之内。可以用在数组、链表、区间、滑动窗口、流、回文串、和差问题等多个场景。（前项和其实并不完全是指针问题，但也归并在这里）。
2. Quick Sort和Merge Sort的基本原理与实现，排序的稳定性问题
3. Quick Select的实现与复杂度
4. 同向指针与相向指针的使用场景
5. 不同场景下循环终止条件？
6. 两数之和，之差，特定条件下（大小于某值等）的计数问题
7. 三数或三数以上之和的通用写法（两数之和+搜索）
8. 数组有没有排序？是否需要排序？
9. 数组有没有去重？是否需要去重？
10. 离线数据（内存中，有限长）还是在线数据（无法放入内存，长度未知）？
11. 链表操作中dummy node与previous node的使用技巧
12. 链表的中点，判断是否有环，寻找环的交叉点

### 宽度优先搜索
#### 基本问题
1. 如果复杂程度类似， 面试中尽量优先使用BFS
2. BFS主要几种场景： 层级遍历，拓扑排序，图上搜索（包括二叉树，矩阵）
3. Queue的使用技巧，BFS的终止条件？
4. 什么时候使用分层？什么时候不需要？实现的时候的区别在哪里？
5. 拓扑排序的概念？如何判断是否存在拓扑排序？是否存在唯一的拓扑排序？找到所有拓扑排序？
6. 什么时候需要使用set记录访问过的节点？（为什么二叉树上的BFS往往不需要set？）什么时候需要map记录到达过的节点距离？
7. 如何在矩阵中遍历下一步的所有节点？如果每次可能走不止一步怎么办（Maze II）？
8. 为什么BFS解决的基本都是简单图（边长为1）问题？如果边长不为1，该怎么办？
9. BFS的时空复杂度估算？
10. 如何使用双向BFS进行优化？

#### 二叉树
#### 拓扑排序
#### 矩阵
#### 图

### 二叉树与递归
#### 基本问题
1. 理解二叉树、平衡二叉树、二叉搜索树的关系和概念。
2. 理解递归的概念和方法，递归三要素。
3. 在解决递归问题的时候，有时可以返回多个值（Python），或者用一个额外的class包装多个值（Java）。
4. 熟练掌握用递归和非递归的方式分别前序、中序、后序遍历二叉树的方法。
5. 理解掌握分治和遍历的区别和联系。
6. 理解掌握top-down, buttom-up的思路。
7. 理解掌握二叉树上的Iterator。

#### 二叉树前中后序遍历（需要熟练掌握非递归方式）
#### 反向复原二叉树
#### Iterator相关
#### 判断树的形态
#### 子树相关问题
#### 路径相关问题
#### LCA问题（Lowest Common Ancestor）
#### 其他

### 深度优先搜索
#### 基本问题：
1. DFS中递归的基本要素
2. 终止条件的选择；回溯；剪枝
3. 什么时候需要排序？
4. 如何去除重复元素？一个元素允许使用多次的情况？
5. 在图上进行DFS如何避免回到重复节点
6. 识别一个隐式图，并使用DFS
7. 在某些情况下，利用记忆化搜索进行优化

#### 排列组合
#### 二叉树
#### 图

### 数据结构
#### 基本问题：
1. 本章按照数据结构分类一些问题，和之前按算法分类的题目相比可能会有重复，因为一道题可能有多个标签。
2. 对于每种数据结构，需要先学习掌握其基本原理，优缺点，复杂度，和对应语言中的API用法。对于其基本的实现方式也要了解。
3. Array，Matrix，String，Hash都是一些常用的数据结构，一般在各种题里都会用到，这里主要列举一些没有涉及到其他算法的题目。
4. Linked List往往自成一类，会涉及到一些pointer操作，需要细心。
5. Queue一般用在BFS里面比较多，这里不单独列举了。
6. Heap， Stack往往和其他知识点混用，但自己单独出题也可以。
7. Trie，Union Find， Sweep Line的套路比较明显，需要记住模板。
8. Binary Index Tree 和Segment Tree涉及到的题目有限，需要记住模板。Segment Tree解法一般来说可以覆盖BIT能解决的问题，但是BIT写起来短一些。
9. 复合数据结构里面LRU和LFU相对比较重要。其他的在掌握基本数据结构即复杂度之后，可以随机应变。

#### Array & Matrix
#### String
#### Linked List
#### Hash
#### Heap
#### Stack堆
#### Monotonic Stack
#### Trie
#### Union Find
#### Sweep Line
#### Binary Index Tree & Segment Tree
#### Complex Data Structure
#### 动态规划

# Machine learning
## ML Systems Design Interview Guide
[ML Systems Design Interview Guide](http://patrickhalina.com/posts/ml-systems-design-interview-guide/)







