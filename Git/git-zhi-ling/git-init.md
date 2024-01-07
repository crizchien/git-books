# git init

> 建立第一個git資料夾

簡單兩個步驟即可建立一個local的git資料夾

1. 建立資料夾

<pre><code><strong>mkdir git-dir
</strong></code></pre>

2. 初始化git資料夾

```
cd git-dir
git init
```

3. 檢查當前目錄底下是否長出.git資料夾

```
ls -la
```

{% hint style="info" %}
.git目錄是用來存放git相關資訊，因此可以判斷目錄內是否有.git來查看當前目錄是否被git控管
{% endhint %}
