<font size = 6 color = red>Vector</font>

# 1. 相关介绍  
    vector<T>容器是包含T类型元素的序列容器，和array<T,N>容器相似，不同的是vector<T>容器的大小可以自动增长，从而可以包含任意数量的元素；因此类型参数T不再需要模板参数N。只要元素个数超过vector当前容量，就会自动分配更多的空间。只能在容器尾部高效的删除或者添加元素。

# 2. 创建vector<T>容器
下面是一个生成存放double类型元素的vector<T>容器示例：
```
    std::vector<double> Values；
```

## 2.1 分配空间
