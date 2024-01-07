# git add

> 將修改過或還沒被追蹤的檔案加入到暫存區等待後續commit

### 透過git add指令將檔案加入暫存區

1. 透`git status`查看修改過或還沒被追蹤的檔案

```
git status
```

2. 將檔案加入暫存區

```
git add .  # 將當前目錄以下全部檔案加入
git add --all  # 將全部檔案加入
git add ${file_name}  # 將特定檔案加入
```

3. 透過`git status`查看目前狀態

```
git status
```

### 透過git restore --stage將檔案移出暫存區

1. 透`git status`查看已加入暫存區的檔案

```
git status
```

2. 將檔案移出暫存區

```
git restore --stage .  # 將當前目錄底下全部檔案移出
git restore --stage ${file_name}  # 將特定檔案移出
```

3. 透過`git status`查看目前狀態

```
git status
```
