# TLDsDb
Top-level Domains Database，互联网顶级域数据库

数据来源：[IANA — Root Zone Database](http://www.iana.org/domains/root/db)

## 为什么建立此项目？

为了方便处理域名字符串。比如，验证域名合法性、截取字符串中的域名后缀等等。

验证域名合法性常见的方法是使用正则表达式。但正则表达式并不能识别域名最后两个字段是域名后缀还是用户定义字段。比如，`.abc.com`、`.123.kr`、`.com.cn`、`.co.kr`以及`.com.ph`等等。正则表达式捕获子字符串，结合顶级域数据就能得到以下结果：

1. `.abc.com` 是域名
2. `.123.kr` 是域名
3. `.com.cn` 是域名后缀(通用顶级域 + 国家顶级域)
4. `.co.kr` 是域名后缀(通用顶级域 + 国家顶级域)
5. `.com.ph` 是域名后缀(通用顶级域 + 国家顶级域)


## 文件结构说明

* allinone.txt：所有互联网顶级域数据
* country-code.txt：仅包括`国家代码`顶级域数据
* generic.txt：仅包括`通用`顶级域数据
* test.txt：仅包括`测试`顶级域数据
* country-code-dns-name.txt：仅包括国际化国家代码顶级域的DNS名称
