# Git SHA-1

### Git 中 SHA-1 的計算過程

***

Git 使用 SHA-1 散列函數為其對象（如提交、樹、blob、標籤）生成一個 40 字元的十六進制數字串，以提供每個對象的唯一識別碼。以下是該過程的詳細步驟：

**步驟 1: 數據準備**

每種類型的 Git 對象均按照特定格式準備其內容。舉例來說，blob 對象（用於存儲文件數據）的格式為 `"blob {內容大小}\0{內容}"`，其中：

* `{內容大小}` 是對象內容的字節長度。
* `\0` 是一個空字符，用於分隔元數據和實際內容。

**步驟 2: 計算 SHA-1**

對格式化後的數據字符串進行 SHA-1 散列計算，產生一個 160 位（40 字元）的十六進制數字串。這個數字串將作為該 Git 對象的唯一標識符。

**步驟 3: 存儲與引用**

計算得出的 SHA-1 值用於在 Git 的對象數據庫中存儲和引用對應的對象。每個對象的 SHA-1 散列值都是唯一的，即使是在不同的存儲庫中也是如此。



### Git SHA-1計算範例 (shell)

***

透過使用git hash-object指令來算出hash值

```
echo -e "Hello, I'm Criz." | git hash-object --stdin
```

不透過git hash-object指令來算出hash值

```
data_len=$(echo -e "Hello, I'm Criz." | wc -c)
echo -e "blob ${data_len}\0Hello, I'm Criz." | sha1sum
```

以上兩種算出來的hash值應為相同
