# Git Diff 练习

## 什么是 Diff？

Diff 用于查看文件的差异。

## 基础用法

### 工作区 vs 暂存区
```bash
git diff
```

### 暂存区 vs 最后一次提交
```bash
git diff --staged
# 或
git diff --cached
```

### 两个提交之间的差异
```bash
git diff commit1 commit2
```
