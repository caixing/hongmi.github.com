---
layout: post
title: 合并排序
category : algorithm
tags : [algorithm, merge, sort]
---
{% include JB/setup %}

合并排序采用分治法（divide and conquer）  
1. 分解。将n个元素分成两个含n/2个元素的子序列  
2. 解决。用合并排序法对两个字序列进行排序  
3. 合并。合并两个已排序的子序列  
伪码如下（参考算法导论）  
<pre>
    merge-sort(A, p, r)
      if p < r
        then q <floor((p + r) / 2)
             merge-sort(A, p, q)
             merge-sort(A, q + 1, r)
             merge(A, p, q, r)
</pre>
算法复杂度为O(nlogn)

一个scheme实现的版本[m-sort] [1]
[1]: https://gist.github.com/hongmi/5637255	"m-sort"
