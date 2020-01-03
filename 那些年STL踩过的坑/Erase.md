<font size = 6 color = red>Erase</font>

---
## STL中的erase问题

STL中的容器按存储方式分为两类，一类是按以数组形式存储的容器（如：<font color = orange>vector 、deque</font>)；另一类是以不连续的节点形式存储的容器（如：<font color = gree>list、set、map</font>）。在使用erase方法来删除元素时，需要注意一些问题。  

使用迭代器删除list、set 或 map某些元素时可以这样使用：  
`正确使用方法1： `
```
std::list< int> List;
std::list< int>::iterator itList;
for( itList = List.begin(); itList != List.end(); )
{
	if( WillDelete( *itList) )
	{
		itList = List.erase( itList);
	}
	else
		itList++;
	}
}
```
`正确使用方法2：`
```
std::list< int> List;
std::list< int>::iterator itList;
for( itList = List.begin(); itList != List.end(); )
{
	if( WillDelete( *itList) )
	{
		List.erase( itList++);
	}
	else
		itList++;
}
```
deque和vector在使用容器进行删除的时候<font color = red>只能</font>使用下面这种方法：
```
std::vector< int> Vec;
std::vector< int>::iterator itVec;
for( itVec = Vec.begin(); itVec != Vec.end(); )
{
	if( WillDelete( *itVec) )
	{
		itVec = Vec.erase( itVec);
	}
	else
		itList++;
}
```