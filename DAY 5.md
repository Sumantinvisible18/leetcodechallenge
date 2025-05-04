# 🔁 Leetcode 234: Palindrome Linked List 

## ✅ Problem Statement

Given the head of a singly linked list, return `true` if it is a **palindrome** or `false` otherwise.

A palindrome is a sequence that reads the same backward as forward.

---

## 💡 Approach

Today’s challenge comes with a twist — solve it, push it to GitHub, and explain it!

To solve this problem efficiently:
- I used the **fast and slow pointer** technique to reach the middle of the list.
- Then I **reversed the second half** of the list.
- Finally, I **compared** the first half and the reversed second half to check if they match.

This way, I was able to check if the list is a palindrome in **O(n) time** and **O(1) space**, without using any extra memory like arrays or stacks.

---

## 🔧 How It Works (Quick Steps)

1. Use `fast` and `slow` pointers to find the middle of the list.
2. If the list has odd length, skip the middle element.
3. Reverse the second half of the list.
4. Compare node-by-node from the start and from the reversed half.
5. Return `true` if all matched; else `false`.

---

## 📦 Files in This Repo

- `main.cpp` → Contains my full C++ solution.
- `README.md` → This file 😄
- `video_explanation.mp4` (or [Watch here](# 🔁 Leetcode 234: Palindrome Linked List

## ✅ Problem Statement

Given the head of a singly linked list, return `true` if it is a **palindrome** or `false` otherwise.

A palindrome is a sequence that reads the same backward as forward.

---

## 💡 Approach

Today’s challenge comes with a twist — solve it, push it to GitHub, and explain it!

To solve this problem efficiently:
- I used the **fast and slow pointer** technique to reach the middle of the list.
- Then I **reversed the second half** of the list.
- Finally, I **compared** the first half and the reversed second half to check if they match.

This way, I was able to check if the list is a palindrome in **O(n) time** and **O(1) space**, without using any extra memory like arrays or stacks.

---

## 🔧 How It Works (Quick Steps)

1. Use `fast` and `slow` pointers to find the middle of the list.
2. If the list has odd length, skip the middle element.
3. Reverse the second half of the list.
4. Compare node-by-node from the start and from the reversed half.
5. Return `true` if all matched; else `false`.

---

## 📦 Files in This Repo

- `https://leetcode.com/problems/palindrome-linked-list/` → Contains my full C++ solution.
- `README.md` → This file 😄
- `video_explanation.mp4` (or [Watch here](https://yourvideolink.com)) → My short video explaining the approach.

---

## 🚀 How to Run My Code

Make sure you have a C++ compiler like `g++` installed.

THE CODE 
class Solution {
 public:
  bool isPalindrome(ListNode* head) {
    ListNode* slow = head;
    ListNode* fast = head;

    while (fast != nullptr && fast->next != nullptr) {
      slow = slow->next;
      fast = fast->next->next;
    }

    if (fast != nullptr)
      slow = slow->next;
    slow = reverseList(slow);

    while (slow != nullptr) {
      if (slow->val != head->val)
        return false;
      slow = slow->next;
      head = head->next;
    }

    return true;
  }

 private:
  ListNode* reverseList(ListNode* head) {
    ListNode* prev = nullptr;
    while (head != nullptr) {
      ListNode* next = head->next;
      head->next = prev;
      prev = head;
      head = next;
    }
    return prev;
  }
};


 

