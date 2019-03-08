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

> ����Ʈ���� Ȯ���ؼ� �� ���� ���� �ڽ��� ���� �� �ְ� �Ϲ�ȭ
> �ڽ� ���� ���� �Ϲ�ȭ�� �ϸ鼭 �ϳ��� ������ �� ���� ����Ǵ� �� �Ӹ� �ƴ϶� Ʈ���� ������ �ڵ����� ���ߴ� �������� ����
> ���� ������ �ܼ��ϸ鼭�� ȿ����
> �� ��忡 M���� �ڷᰡ ��ġ�Ǹ� M�� B-Tree��� ��
>- 5�� B-Tree�� ���, �ڽĳ�尡 �ִ� 5���� ���� �ǹ�
>- B-Tree�� ������ ������ ���ߴ� Ʈ���̱� ������ �־��� ��쿡�� O(logN)�� �˻� ������ ����

> �뷮�� �����͸� ó���ؾ� �ϴ� �˻� ������ ���, �ϳ��� ��尡 ���� �����͸� �����°� ū ����
> �뷮�� �����ʹ� �޸� ���ٴ� HDD or SSD�� ����Ǿ�� �ϴµ�, �̰͵��� �� ������ ������� �ϱ� ����
> ����
>- �� ���� 1024byte ��� 2byte�� ������ 1024byte�� ������ ����¿� ���� ����� ����
>- �׷��ٸ� �ϳ��� ��带 1024byte�� �ǵ��� �����Ѵٸ� ����� �鿡�� �ſ� ȿ������ ����
>- �̷� �������� ���� DBS�� �ε��� ���� ������� �ֿ�ǰ� ����

> ��Ģ
>- ����� �ڷ���� N�̶�� �ڽ��� ���� N+1�̾�� �Ѵ�
>- �� ����� �ڷ�� ���ĵ� ���¿��� �Ѵ�
>- ����� �ڷ�Dk�� ���� ����Ʈ���� Dk���� ���� �����̰� ������ ����Ʈ���� Dk���� ū �����̾�� �Ѵ�
>- Root ���� ��� 2���̻��� �ڽ��� ������ �Ѵ�
>- Root ��带 ������ ��� ���� ��� M/2���� �ڷḦ ������ �־�� �Ѵ�
>- �ܺ� ���(leaf node)�� ���� ����� ���̴� ��� ����(�ܺγ��� ��� ���� ������ �ִ�)
>- �Է��ڷ�� �ߺ��� �� ����

> B-Tree�� ����
>- ���ο� ���Ҵ� leaf node�� ����
>- node�� overflow�� �߻��Ǹ� ����� t-1��° key(�߰���)�� parent�� �ø��� ��带 ����

> B-Tree�� ����
>- ���� ����� ��� node�� ����
>- �ٸ�, ������ �ϱ� ���켭�� leaf node�� �ش� ���Ҹ� �̵����Ѿ� ��
>- https://potatoggg.tistory.com/174
