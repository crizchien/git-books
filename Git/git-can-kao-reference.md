# Git參考（Reference）

> 參考是Git中用於追蹤提交（commits）的指針，通常用於記錄特定的檢查點，如提交、分支或標籤的位置。

參考分為下列幾種：

* **分支（Branch）**
* **HEAD**
* **標籤（Tag）**

![](<.gitbook/assets/git-第 2 页.drawio.png>)

### 分支（Branch）

***

* Branch指向該Branch的最新commit。

可以透過查看.git內的檔案，確認Branch指向該分支最新的commit

```
ls .git/refs/heads/   # 底下包含所有分支
cat .git/refs/heads/main   # 查看main指向的commit
```



### HEAD

***

* HEAD指向目前所在的Branch

可以透過查看.git內的檔案，確認HEAD指向當前Branch

```
cat .git/HEAD   # 查看當前指向的Branch
```



### 標籤（Tag）

***

* 通常用於標記特定的發佈版本（如v1.0、v2.0等）。
* 標籤在創建後通常是固定不變的，它指向特定的提交不會隨著新提交而變化。

可以透過查看.git內的檔案，確認Tag指向的commit

```
ls .git/refs/tags/   # 底下包含所有tag
cat .git/refs/tags/v1.0.0   # 查看tag指向的commit
```
