# Invert Binary Tree ✌️
## https://leetcode.com/problems/invert-binary-tree

Invert a binary tree.
```
Example:

Input:

     4
   /   \
  2     7
 / \   / \
1   3 6   9

Output:

     4
   /   \
  7     2
 / \   / \
9   6 3   1
```


## Implementation :

```java
/**
 * Definition for a binary tree node.
 * public class TreeNode {
 *     int val;
 *     TreeNode left;
 *     TreeNode right;
 *     TreeNode(int x) { val = x; }
 * }
 */
class Solution {
   public TreeNode invertTree(TreeNode root) {
	if(root == null)
	   return null;
	invertTree(root.left);
	invertTree(root.right);
	swapChildren(root);
	return root;
   }
	 
   private void swapChildren(TreeNode node) {
	if(node == null)
	    return;
	TreeNode temp = node.left;
	node.left = node.right;
	node.right = temp;
   }
}

```
