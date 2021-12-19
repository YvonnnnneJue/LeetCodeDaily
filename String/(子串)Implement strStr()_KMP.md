
![](../../../images/2021-12-19-19-44-31.png)

[有限状态机之 KMP 字符匹配算法
](https://labuladong.gitee.io/algo/3/26/96/)
```c++
class Solution {
public:
    int strStr(string haystack, string needle) {
        if (!needle.size()) return 0; // wa1 
        int i = 0;  int j = 0;
        int len = needle.size();
        for (; i < haystack.size(); i++) {
            if (haystack[i] != needle[0]) continue;
            bool flag = true;
            while(j < len) {
                if (i+j > haystack.size()) return -1; // overflow wa 2,原数组长度不够
                if (haystack[i+j] != needle[j]) flag = false;
                j++;
            }
            j = 0;
            if (flag) return i;
        }
        return -1;
    }
};
```