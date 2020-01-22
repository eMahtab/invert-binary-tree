# Invert Binary Tree
## https://leetcode.com/problems/invert-binary-tree

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
   public static TreeNode invertTree(TreeNode root) {
	     if(root == null)
	    	 return null;
	     invertTree(root.left);
	     invertTree(root.right);
	     swapChildren(root);
	     return root;
	 }
	 
	 public static void swapChildren(TreeNode node) {
		 if(node == null)
			 return;
		 TreeNode temp = node.left;
		 node.left = node.right;
		 node.right = temp;
	 }
}

```
