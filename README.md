# Autoproxy-pac

### pac规则

pac文件采用通配符的格式

```
  "||github.com",
  "||githubusercontent.com",
  "||forexample.com",
```

不要用中文输入法，切换到英文模式。 **||** 适用于匹配开头，形如 **||google.com** ，则表示以 **任意内容 + google.com + 任意内容** 都会触发代理规则，如果要增加自己的常用网站规则，这样写上去就行了，不要忘记了句尾逗号。

pac文件可以参考 `https://github.com/xfcycc/pac/blob/main/pac.txt`

### 简单的捕捉流量地址的方法

开启日志，开启全局代理，关闭无关软件，再访问网址，一般会出现如 **Connect github.com:443 via XXXXXXXXX** 的文字，反复尝试，将这些网址加入pac规则即可。