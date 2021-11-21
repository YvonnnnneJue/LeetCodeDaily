# LeetCodeDaily

### C++ 语言基础:

#### 1. 动态数组类型 vector

```c++
// initialize
vector<int> res; 

vector<int> res(n); 

vector<int> res{1,2,3};

vector<vector<int> >dp; 

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



