# git log

> 透過git log可查看commit的歷史資訊

### 直接使用git log進行查看

1. 使用`git log`查看commit歷史

```
git log
```

### 使用客製指令查看log

{% hint style="info" %}
因原生git log指令並不方便查看，因此可透過以下指令進行優化
{% endhint %}

1. git log優化指令如下

{% code overflow="wrap" %}
```
git --no-pager log --graph --pretty=format:"%C(auto)%h %<(1)(%ar) %<(1)<%an> \"%s\" %d" && echo ""
```
{% endcode %}

2. 可以透過`alias`做為指令

{% code overflow="wrap" %}
```
alias gitl='git --no-pager log --graph --pretty=format:"%C(auto)%h %<(1)(%ar) %<(1)<%an> \"%s\" %d" && echo ""'
```
{% endcode %}
