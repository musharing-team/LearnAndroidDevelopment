# XML 基础

> XML，可拓展标记语言。

`XML` 是一种专门用来传输、储存数据的语言，它具有很强的”自我描述性“（即看到就知道在说啥），并且它以纯文本描述数据，这意味着 XML 可以独立于硬软件系统。

## XML 树结构

一个简单的 XML 实例如下：

```xml
<?xml version="1.0" encoding="UTF-8"?>
<note>
    <from>Foo</from>
    <to>Bar</to>
    <body>
        <title>A Note</title>
        <content>This is a note of nothing.</content>
    </body>
</note>
```

可见，它具有清晰的树结构，即 XML 文档总是由类似下面这样的片段组成的：

```xml
<root>
    <child>
        <subchild>
            ...
        </subchild>
    </child>
</root>
```

## XML 与 HTML

**XML** 和 *HTML* 相似，但又有诸多不同。

HTML 是专门用来显示数据的，而 XML 重在 储存、描述和传输数据；

HTML中定义了很多具有特殊含义的标签（如，`<p>`代表一个段落），而 **XML 中没有预定的标签**，一切都靠自行定义。

## XML 语法规则

* 必须具有根元素（有一个包含着其他所有元素的根）。
* 需要具有 XML 声明，即在首行写一句 `<?xml version="1.0" encoding="UTF-8"?>`，用来指明 XML 版本和编码。
* 所有的标签必须有关闭标签。（例如`<p>...</p>`、`<br />`）
* XML 大小写敏感
* 必须正确嵌套。（不能 `<b><i>...</b></i>`，而应该`<b><i>...</i></b>`）
* 属性值必须加引号。（不能 `<note num=12>`，而应该`<note num="12">`）
* 实体引用：

```
<   &lt;
>   &gt;
&   &amp;
'   &apos;
"   &quot;
```

* 注释 `<!--注释内容-->`
* 空格不会被删减（和HTML中不同）
* XML 以 `LF` 储存换行

【注】常用的换行符有两种 `CR`回车，和 `LF`换行。

Windows 以 `CR`+`LF` 换行；

Unix 和 Mac 以 `LF` 换行；

早期也有的 Mac 以 `CR` 换行。