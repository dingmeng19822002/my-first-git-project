# Git Worktree 练习

## 什么是 Worktree？

Worktree 允许你在同一个仓库中同时检出多个分支到不同的目录。

## 使用场景

- 同时开发多个功能
- 在不影响当前工作的情况下快速修复 bug
- 比较不同分支的代码

## 基本命令

```bash
# 创建新的 worktree
git worktree add ../project-feature2 feature2

# 查看所有 worktree
git worktree list

# 删除 worktree
git worktree remove ../project-feature2

# 清理无效的 worktree
git worktree prune
```

## 实战示例

```bash
# 主目录正在开发功能 A
cd /path/to/project

# 突然需要修 bug，创建新 worktree
git worktree add ../project-hotfix hotfix

# 在新目录修 bug
cd ../project-hotfix
# 修改、提交...

# 完成后删除
git worktree remove ../project-hotfix
```

## 优点

- 不需要 stash 或提交未完成的工作
- 不需要重新克隆仓库
- 共享 .git 目录，节省空间
