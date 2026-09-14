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
