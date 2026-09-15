# Rebase 练习

## 什么是 rebase？

rebase 可以让提交历史更清晰整洁。

## rebase vs merge

- merge：保留所有分支历史，会创建合并提交
- rebase：将当前分支的提交"移动"到目标分支之后

## 常用命令

```bash
git rebase main        # 将当前分支 rebase 到 main
git rebase -i HEAD~3   # 交互式 rebase 最近 3 个提交
git rebase --continue  # 解决冲突后继续 rebase
git rebase --abort     # 取消 rebase
```

## 练习场景

今天我们在这个分支上练习 rebase 操作。

### 第一步：创建多个提交
我们会创建几个提交，然后练习交互式 rebase 来整理它们。

## Rebase 的优点

1. 保持提交历史线性化
2. 更容易理解项目演进过程
3. 避免不必要的合并提交

## 注意事项

⚠️ **不要对已经推送到远程的提交进行 rebase**，这会给团队协作带来麻烦。

## 实战示例

### 场景一：整理本地提交
当你在本地做了很多小提交，想在推送前整理成几个有意义的提交。

### 场景二：更新分支基础
当 main 分支有新的提交时，将你的功能分支 rebase 到最新的 main 上。

## 小贴士

- 使用 `git log --oneline` 查看简洁的提交历史
- 交互式 rebase 时，使用 `pick`、`squash`、`reword` 等命令
