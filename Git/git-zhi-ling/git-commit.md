# git commit

> 用於提交已暫存的變更到本地倉庫

### 透過git commit指令進行提交

1. 使用 `git status` 查看修改過的檔案和暫存區狀態

```
git status
```

2. 使用 `git commit` 提交暫存區的變更

```
git commit -m "Your commit messages..."
```

3. 使用 `git log` 查看提交歷史，確認變更已被記錄

```
git log
```

### 透過 amend參數修改最後一次提交

1. 在做出新的更改後，可以使用 `git commit --amend` 修改上一次的提交

```
git commit --amend
```

2. 使用 `git log` 確認提交歷史已更新

```
git log
```
