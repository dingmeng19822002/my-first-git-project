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

### 查看特定文件的差异
```bash
git diff HEAD~2 HEAD -- 文件名.md
```

## 高级用法

### 只看统计信息
```bash
git diff --stat
```

### 单词级别的差异
```bash
git diff --word-diff
```
