#### review [234. Palindrome Linked List](https://leetcode-cn.com/problems/palindrome-linked-list/) 

回文链表

一, 压入数组比较:

```c++
/**
 * Definition for singly-linked list.
 * struct ListNode {
 *     int val;
 *     ListNode *next;
 *     ListNode() : val(0), next(nullptr) {}
 *     ListNode(int x) : val(x), next(nullptr) {}
 *     ListNode(int x, ListNode *next) : val(x), next(next) {}
 * };
 */
class Solution {
public:
    bool isPalindrome(ListNode* head) {
        vector<int> res;
        if (head == NULL) return false;
        ListNode* cur = head;
        while(cur) {
            res.push_back(cur->val);
            cur = cur->next;
        }
        for (int i = 0, j = res.size() - 1; i < j; i++, j--) {
            if (res[i] != res[j]) return false;
        }
        return true;
    }
};
```

