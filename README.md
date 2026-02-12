# DSA-Patterns-Roadmap

<img width="784" alt="image" src="https://github.com/user-attachments/assets/e5112266-3e6b-432b-bfd3-397fa148fc5d" />


## DSA Patterns and Practice Questions

# 1. Fast and Slow Pointer

## 1. Linked List Cycle II 
```text
🧠 Idea

Detect whether a cycle exists in the linked list using two pointers.
If a cycle is found:
Reset slow to head.
Move both slow and fast one step at a time (->next).
The node where both pointers meet again is the starting node of the cycle.
Return that node.
```

## **2. Remove Nth Node from the End of List**
### **Apporach-1**
```text
1.Calculate Total lenth of LL
2.Go to l-n node
3.Break the link
```
### **Apporach-2**
```text
1.slow,fast -> take fast pointer n time ahead
2.While fast->next is not null go to next node for slow 
3.Break the link
```
## 3. Find the Duplicate Number  ✨
**Technique:** Fast and Slow Pointer (Floyd’s Cycle Detection)

---

### 🧠 Pseudocode

```text
slow ← nums[0]
fast ← nums[0]

do
    slow ← nums[slow]
    fast ← nums[nums[fast]]
while slow ≠ fast

slow ← nums[0]

while slow ≠ fast
    slow ← nums[slow]
    fast ← nums[fast]

return slow
```

<img width="454" height="942" alt="image" src="https://github.com/user-attachments/assets/430dbab8-7943-4e42-9308-fa7d42e432a5" />


## 4.**Palindrome Linked List** ##
### **Apporach-1**
```text
1.Take a vector store all the LL
2.one pointer from 0 another from size-1
3.check they are equal or not if not return false
```
### **Apporach-2**
```text
1.slow,fast -> take fast pointer 2 step ahead until it become null (slow 1 step ahead ,reaches to mid)
2.reveres the linked list form slow to end (using prev,curr,next pointers)
3.Travers and check for each node in both LL
```

# 2. Overlapping Intervals

## **2.1 Merge Intervals** 
```text
        1.sort 
        sort(intervals.begin(),intervals.end());
        vector<vector<int>>ans;

        //2.assginging ans with first element
        ans.push_back(intervals[0]);

         [[1,4],[2,3]] ->tricky case

        for(int i=1;i<intervals.size();i++){
            vector<int>temp;
            //used vector.back()
            if(ans.back()[1]>= intervals[i][0]){
                //max of previous 1 st element and curr 0th element
                ans.back()[1]=(max(intervals[i][1],ans.back()[1]));
            }else{
                temp.push_back(intervals[i][0]);
                temp.push_back(intervals[i][1]);
                ans.push_back(temp);
            }
        }
        return ans;        
```

## **2.2 Insert Interval**
### **Apporach-1**
```text
1.Add newInterval at begining and sort the interval
2.Apply Merge interval directly 
Here Problem is it will be O(nlog n) it can be optimized.....
```
### **Apporach-2**
```text
1.Optimization required ......
```

## **2.2 My Calendar II**
## **2.3 Minimum Number of Arrows to Burst Balloons**
## **2.4 Non-overlapping Intervals**


## 3. Prefix Sum
| Problem |
|---------|
| Find the middle index in array |
| Product of array except self |
| Maximum product subarray |
| Number of ways to split array |
| Range Sum Query 2D |

## 4. Sliding Window
| Category | Problem |
|----------|---------|
| Fixed Size | Maximum Sum Subarray of Size K |
| | Number of Subarrays having Average Greater or Equal to Threshold |
| | Repeated DNA sequences |
| | Permutation in String |
| | Sliding Subarray Beauty |
| | Sliding Window Maximum |
| Variable Size | Longest Substring Without Repeating Characters |
| | Minimum Size Subarray Sum |
| | Subarray Product Less Than K |
| | Max Consecutive Ones |
| | Fruits Into Baskets |
| | Count Number of Nice Subarrays |
| | Minimum Window Substring |

## 5. Two Pointers
| Problem |
|---------|
| Two Sum II - Input Array is Sorted |
| Dutch National Flag: Sort Colors |
| Next Permutation |
| Bag of Tokens |
| Container with most water |
| Trapping Rain Water |

## 6. Cyclic Sort (Index-Based)
| Problem |
|---------|
| Missing Number |
| Find Missing Numbers |
| Set Mismatch |
| First Missing Positive |

## 7. Reversal of Linked List (In-place)
| Problem |
|---------|
| Reverse Linked List |
| Reverse Nodes in k-Group |
| Swap Nodes in Pairs |

## 8. Matrix Manipulation
| Problem |
|---------|
| Rotate Image |
| Spiral Matrix |
| Set Matrix Zeroes |
| Game of Life |

## 9. Breadth First Search (BFS)
| Problem |
|---------|
| Shortest Path in Binary Matrix |
| Rotten Oranges |
| As Far From Land as Possible |
| Word Ladder |

## 10. Depth First Search (DFS)
| Problem |
|---------|
| Number of Closed Islands |
| Coloring a Border |
| DFS from boundary: Number of Enclaves |
| Shortest time: Time Needed to Inform all Employees |
| Cyclic Find: Find Eventual Safe States |

## 11. Backtracking
| Problem |
|---------|
| Permutation II |
| Combination Sum |
| Generate Parenthesis |
| N-Queens |
| Sudoku Solver |
| Palindrome Partitioning |
| Word Search |

## 12. Modified Binary Search
| Problem |
|---------|
| Search in Rotated Sorted Array |
| Find Minimum in Rotated Sorted Array |
| Find Peak Element |
| Single element in a sorted array |
| Minimum Time to Arrive on Time |
| Capacity to Ship Packages within 'd' Days |
| Koko Eating Bananas |
| Find in Mountain Array |
| Median of Two Sorted Arrays |

## 13. Bitwise XOR
| Problem |
|---------|
| Missing Number |
| Single Number II |
| Single Number III |
| Find the Original array of Prefix XOR |
| XOR Queries of a Subarray |

## 14. Top 'K' Elements
| Problem |
|---------|
| Top K Frequent Elements |
| Kth Largest Element |
| Ugly Number II |
| K Closest Points to Origin |

## 15. K-way Merge
| Problem |
|---------|
| Find K Pairs with Smallest Sums |
| Kth Smallest Element in a Sorted Matrix |
| Merge K Sorted Lists |
| Smallest Range Covering Elements from K Lists |

## 16. Two Heaps
| Problem |
|---------|
| Find Median from Data Stream |
| Sliding Window Median |
| IPO |

## 17. Monotonic Stack
| Problem |
|---------|
| Next Greater Element II |
| Next Greater Node in Linked List |
| Daily Temperatures |
| Online Stock Span |
| Maximum Width Ramp |
| Largest Rectangle in Histogram |

## 18. Trees
| Category | Problem |
|----------|---------|
| Level Order Traversal | Level order Traversal |
| | Zigzag Level order Traversal |
| | Even Odd Tree |
| | Reverse odd Levels |
| | Deepest Leaves Sum |
| | Add one row to Tree |
| | Maximum width of Binary Tree |
| | All Nodes Distance K in Binary tree |
| Tree Construction | Construct BT from Preorder and Inorder |
| | Construct BT from Postorder and Inorder |
| | Maximum Binary Tree |
| | Construct BST from Preorder |
| Height related | Maximum Depth of BT |
| | Balanced Binary Tree |
| | Diameter of Binary Tree |
| | Minimum Depth of BT |
| Root to leaf path | Binary Tree Paths |
| | Path Sum II |
| | Sum Root to Leaf numbers |
| | Smallest string starting from Leaf |
| | Insufficient nodes in root to Leaf |
| | Pseudo-Palindromic Paths in a Binary Tree |
| | Binary Tree Maximum Path Sum |
| Ancestor problem | LCA of Binary Tree |
| | Maximum difference between node and ancestor |
| | LCA of deepest leaves |
| | Kth Ancestor of a Tree Node |
| Binary Search Tree | Validate BST |
| | Range Sum of BST |
| | Minimum Absolute Difference in BST |
| | Insert into a BST |
| | LCA of BST |

## 19. Dynamic Programming
| Category | Problem |
|----------|---------|
| Take / Not take (0/1 Knapsack) | House Robber II |
| | Target Sum |
| | Partition Equal Subset Sum |
| | Ones and Zeroes |
| | Last Stone Weight II |
| Infinite Supply | Coin Change |
| | Coin Change II |
| | Perfect Squares |
| | Minimum Cost For Tickets |
| Longest Increasing Subsequence | Longest Increasing Subsequence |
| | Largest Divisible Subset |
| | Maximum Length of Pair Chain |
| | Number of LIS |
| | Longest String Chain |
| DP on Grids | Unique Paths II |
| | Minimum Path Sum |
| | Triangle |
| | Minimum Falling Path Sum |
| | Maximal Square |
| | Cherry Pickup |
| | Dungeon Game |
| DP on Strings | Longest Common Subsequence |
| | Longest Palindromic Subsequence |
| | Palindromic Substrings |
| | Longest Palindromic Substring |
| | Edit Distance |
| | Minimum ASCII Delete Sum for Two Strings |
| | Distinct Subsequences |
| | Shortest Common Supersequence |
| | Wildcard Matching |
| DP on Stocks | Buy and Sell Stocks II |
| | Buy and Sell Stocks III |
| | Buy and Sell Stocks IV |
| | Buy and Sell Stocks with Cooldown |
| | Buy and Sell Stocks with Transaction Fee |

## 20. Graphs
| Category | Problem |
|----------|---------|
| Topological Sort | Course Schedule |
| | Course Schedule II |
| | Strange Printer II |
| | Sequence Reconstruction |
| | Alien Dictionary |
| Union-Find | Number of Operations to Make Network Connected |
| | Redundant Connection |
| | Accounts Merge |
| | Satisfiability of Equality Equations |

## 21. Greedy
| Problem |
|---------|
| Jump Game II |
| Gas Station |
| Bag of Tokens |
| Boats to Save People |
| Wiggle Subsequence |
| Car Pooling |
| Candy |

## 22. Design Data Structure
| Problem |
|---------|
| Design Twitter |
| Design Browser History |
| Design Circular Deque |
| Snapshot Array |
| LRU Cache |
| LFU Cache |


Courtesy:
https://neetcode.io | 
https://leetcode.com
