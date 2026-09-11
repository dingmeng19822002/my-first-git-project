# Cherry-pick 练习

## 什么是 cherry-pick？

cherry-pick 可以从其他分支"摘取"特定的提交，应用到当前分支。

## 常用命令

```bash
git cherry-pick <commit-hash>     # 摘取单个提交
git cherry-pick <hash1> <hash2>   # 摘取多个提交
git cherry-pick <hash1>..<hash2>  # 摘取提交范围
```
