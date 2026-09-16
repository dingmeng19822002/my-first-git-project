# Git Bisect 练习

## 什么是 Bisect？

Bisect 使用二分查找法，快速定位引入 bug 的提交。

## 使用场景

当你发现代码有 bug，但不知道是哪个提交引入的时候。

## 基本流程

```bash
# 1. 开始 bisect
git bisect start

# 2. 标记当前版本为坏的
git bisect bad

# 3. 标记一个已知好的版本
git bisect good <commit-hash>

# 4. Git 会自动切换到中间的提交
# 测试后标记：
git bisect good  # 如果这个版本是好的
# 或
git bisect bad   # 如果这个版本是坏的

# 5. 重复步骤 4，直到找到第一个坏提交

# 6. 结束 bisect
git bisect reset
```

## 自动化 Bisect

可以用脚本自动测试：
```bash
git bisect run ./test.sh
```
