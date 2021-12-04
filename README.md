# LeetCodeDaily

### C++ 语言基础:

#### 1. 动态数组类型 vector

```c++
// initialize
vector<int> res; vector<int> res(n); vector<int> res{1,2,3};vector<vector<int> >dp; 

/**
*	member function
*/

bool is empty()
// the length of vector
size_type size();

// return the last element;
reference back();

// return the first element;
reference front();

// add element at the end
void push_back(const value_type& val);
// c++11. 
void emplace_back (Args&&... args);

// delete last element
void pop_back(const value_type& val);

void insert (iterator position, const value_type& val);

iterator erase (const_iterator position);
iterator erase (const_iterator first, const_iterator last);

// clear content
void clear() noexcept;

// swap content. like vector1 <-> vector2
void swap (vector& x); 

```

```c++
排序一个vector: nums = [[1,1,2], [2,3,5]]
sort(nums.begin(), nums.end(), [&](auto& a, auto& b) {
  return a[0] < b[1] // 从小到大
});

void iota( ForwardIterator first,ForwardIterator last, T value );
// 用顺序递增的值赋值指定范围内的元素
std::iota(foo.begin(), foo.end(), 0);// 将从 0 开始的 n 次递增值赋值给 foo
// out: 0 1 2 3 .... 15
```



#### 判断数字和文字以及大小写转换

<cctype>头文件.

1. isalpha(), 判断是否为字母, 

```c++
cout<<isalpha('a'); //返回非零
cout<<isalpha('2'); //返回0
```

2. isalnum, 判断是否为字母或者数字

```c++
cout<<isalnum('a'); //输出非零
cout<<isalnum('2'); // 非零
cout<<isalnum('.'); // 零
```

3. islower(), 判断是否小写 issupper(). 判断是否大写
4. tolower, toupper
