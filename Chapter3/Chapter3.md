<notice>教程读者请不要直接阅读本文件，因为诸多功能在此无法正常使用，请移步至[程谱 coderecipe.cn](https://coderecipe.cn/learn/5)学习完整教程。如果您喜欢我们的教程，请在右上角给我们一个“Star”，谢谢您的支持！</notice>
搜索
======
**搜索**（searching）在这里指的是从数组中找出指定的内容所在的位置，同样的，对于AP，我们只需要理解这几个算法的意义和异同即可~

顺序搜索
------
**顺序搜索**（sequential searching）就是把数组从头到尾搜索一遍，直到找到所要找的元素或者搜索完所有元素为止。

以下是顺序搜索在Java里的一种实现：
```java
/***
    @param elements an array containing the items to be searched
    @param target the item to be found in element.
    @return an index of target in elements if foun; -1 otherwise;
    ***/
public static  int sequentialSerach(int[] elements, int target) {
    for (int j = 0; j < elements.length; j++)
        if (elements[j == target]) //String uses equals()
            return j;
    return -1;
}
```

二叉搜索
-----
**二叉搜索**（binary search）是一种高效率的检索方法。将搜索范围逐渐一步一步二分（分为两部分）减小到只剩下一个。

其思想就是我们查看一个数组中间的内容，如果比我们想要的大，那么我就在左边搜索，
如果比我们想要的小，我们就在右边搜索。然后在缩小后的搜索范围查看判断后数组中间的数，就这样依次进行下去，直到找到结果或者全部搜索完成。不过，利用二进制搜索的数组必须是排列好的，否则比如先排序才行。

```java
/***
    @param elements. an array containing the items to be searched.
            Precondition: items in elements are sorted in ascending order.
    @param target. the item to be found in elements.
    @return an index of target in elements if target found; -1 otherwise.
***/
public static int binarySearch(int[] elements, int target) {
    int left = 0;
    int right = elemetns.length - 1;
    while (left <= right) {
        int middle = (left + right) / 2;
        if (targetr < elements[middle]
            right = middle - 1;
        else if (target > elements[middle])
            left = middle + 1;
        else 
            return middle
        
    }
    return -1;
}
```

小练习
------
让我们来练习一下我们刚学习的知识吧。
<lab lang="java" parameters="filename=Hello.java">
<notice>练习环境在此无法显示，请移步至[程谱 coderecipe.cn](https://coderecipe.cn/learn/5)查看。</notice>
public class Hello {
  public static void main(String[] args) {
      // 在这里输入代码
  }
}
</lab>
