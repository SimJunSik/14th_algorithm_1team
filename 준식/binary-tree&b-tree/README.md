* Binary Tree

> ����Ʈ���� �� ��尡 �ڽĳ�带 �ִ� 2�� ������ Ʈ���� �ǹ�
> ���� ����Ʈ��, ���� ����Ʈ��, ��ȭ ����Ʈ�� �� ����
> ���� �켱 ��ȸ
>- ������ȸ : root -> left -> right������ ��ȸ
```
    def pre_order_traversal(self):
        def _pre_order_traversal(root):
            if root is None:
                pass
            else:
                print(root.data)
                _pre_order_traversal(root.left)
                _pre_order_traversal(root.right)
        _pre_order_traversal(self.root)
```
>- ������ȸ : left -> root -> right������ ��ȸ
```
    def in_order_traversal(self):
        def _in_order_traversal(root):
            if root is None:
                pass
            else:
                _in_order_traversal(root.left)
                print(root.data)
                _in_order_traversal(root.right)
        _in_order_traversal(self.root)
```
>- ������ȸ : left -> right -> root������ ��ȸ
```
    def post_order_traversal(self):
        def _post_order_traversal(root):
            if root is None:
                pass
            else:
                _post_order_traversal(root.left)
                _post_order_traversal(root.right)
                print(root.data)
        _post_order_traversal(self.root)
```

> �ʺ� �켱 ��ȸ
>- ���� ��ȸ : �� �� root node���� ���� ������ �湮
```
    def level_order_traversal(self):
        def _level_order_traversal(root):
            queue = [root]
            while queue:
                root = queue.pop(0)
                if root is not None:
                    print(root.data)
                    if root.left:
                        queue.append(root.left)
                    if root.right:
                        queue.append(root.right)
        _level_order_traversal(self.root)
```




* B-Tree
