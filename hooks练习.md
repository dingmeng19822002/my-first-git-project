# Git Hooks 练习

## 什么是 Git Hooks？

Hooks 是在 Git 操作的特定时刻自动执行的脚本。

## 常用 Hooks

### pre-commit
提交前执行，可用于代码检查：
```bash
#!/bin/sh
# .git/hooks/pre-commit

# 运行代码格式检查
npm run lint
if [ $? -ne 0 ]; then
    echo "代码检查失败，提交被阻止"
    exit 1
fi
```

### pre-push
推送前执行，可用于运行测试：
```bash
#!/bin/sh
# .git/hooks/pre-push

# 运行测试
npm test
if [ $? -ne 0 ]; then
    echo "测试失败，推送被阻止"
    exit 1
fi
```

### commit-msg
检查提交信息格式：
```bash
#!/bin/sh
# .git/hooks/commit-msg

commit_msg=$(cat $1)
if ! echo "$commit_msg" | grep -qE "^(feat|fix|docs|style|refactor|test|chore):"; then
    echo "提交信息格式错误！应该以 feat:, fix:, docs: 等开头"
    exit 1
fi
```

## 如何启用

1. 进入 `.git/hooks` 目录
2. 创建或编辑 hook 脚本
3. 给脚本添加执行权限：`chmod +x pre-commit`

## 注意事项

- Hooks 不会被 git 提交（在 .git 目录中）
- 团队共享可以用 husky 等工具
- 可以用 `git commit --no-verify` 跳过 hooks
