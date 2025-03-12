``` python
class TreeNode:
    def __init__(self, val=0, left=None, right=None):
        self.val = val
        self.left = left
        self.right = right
```

## Breadth First Search


## Depth First Search

``` python
 #height of tree : recursion of 1 + max(dfs(left), dfs(right))
def maxDepth(self, root: Optional[TreeNode]) -> int:

	if not root:

		return 0



	return 1 + max(self.maxDepth(root.left), self.maxDepth(root.right)))
```