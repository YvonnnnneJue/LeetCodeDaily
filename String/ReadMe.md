# 常见的字符串类型题目
> 匹配
> 
> 子串
> 
> 前缀/后缀
> 
> 回文串: 
> 1. 双指针,i:头, j;尾. s[i] == s[j], i++, j--
> 2. 字典序中, 每一个字符最多出现一个奇数,其余为偶数. 因此一增一减 rest.size() <= 1;
> 
> 子序列: 双指针

# C++ string 标准库
```c++
1. size() 返回字符串字符个数。

2. find(ch, start = 0) like js indexOf

3. rfind(ch) like js lastIndexOf

3. substr(start, len) 可以从字符串的 start（从 0 开始）截取一个长度为 len 的字符串（缺省 len 时代码截取到字符串末尾）。

5. append(s) 将 s 添加到字符串末尾。or push_back();

6. append(s, pos, n) 将字符串 s 中，从 pos 开始的 n 个字符连接到当前字符串结尾。

7. replace(pos, n, s) 删除从 pos 开始的 n 个字符，然后在 pos 处插入串 s。

8. erase(pos, n) 删除从 pos 开始的 n 个字符。

9. insert(pos, s) 在 pos 位置插入字符串 s。
```