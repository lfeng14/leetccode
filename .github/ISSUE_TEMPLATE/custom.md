---
name: Custom issue template
about: Describe this issue template's purpose here.
title: ''
labels: ''
assignees: ''

---

#### 题目
<img width="542" alt="image" src="https://github.com/lfeng14/leetccode/assets/144297355/cff64213-287d-4ddb-b4f0-c1d673f7f16d">


#### 思路
- 头尾指针，碰到非字母数字往中间移动，直到头尾都是字符或者数字，判断转小写后是否相等，不相等则返回False，相等则继续走上面的逻辑；当头尾指针相遇跳出循环，返回True。
- 源码
```
class Solution:
    def isPalindrome(self, s: str) -> bool:
        end = len(s) - 1
        start = 0
        while start < end:
            print("1 {} {}".format(start, end ))
            while start < end and not s[start].isalpha() and not s[start].isdigit():
                start = start + 1
            while  start < end and not s[end].isalpha() and not s[start].isdigit():
                end = end - 1
            print("2 {} {}".format(start, end ))
            if start < end and s[start].lower() != s[end].lower() :
                return False
            else:
                end = end - 1
                start = start + 1
        return True
```

#### 参考
- [neetcode题目](hhttps://neetcode.io/problems/is-palindrome)
