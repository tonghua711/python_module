json  用于字符串和python基本数据类型之间的转换
（JavaScript Object Notation）是一种轻量级的数据交换格式，易于人阅读和编写。

json 模块提供了四个功能：dumps、dump、loads、load

json.loads()   将已编码的 JSON 字符串解码为 Python 对象
json.dump()  将 Python 对象编码成 JSON 字符串

语法
json.dumps(obj, skipkeys=False, ensure_ascii=True, check_circular=True, allow_nan=True, cls=None, indent=None, separators=None, encoding="utf-8", default=None, sort_keys=False, **kw)


python 原始类型向 json 类型的转化对照表：

Python			JSON
dict			object
list, tuple			array
str, unicode		string
int, long, float		number
True			true
False			false
None			null




json.loads 语法
json.loads用于解码JSON数据。该函数返回Python字段的数据类型
语法
json.loads(s[, encoding[, cls[, object_hook[, parse_float[, parse_int[, parse_constant[, object_pairs_hook[, **kw]]]]]]]])


json 类型转换到 python 的类型对照表：

JSON			Python

object			dict
array			list
string			unicode
number (int)		int, long
number (real)		float
true			True
false			False
null			None

使用第三方库：Demjson
Demjson 是 python 的第三方模块库，可用于编码和解码 JSON 数据，包含了 JSONLint 的格式化及校验功能。

Github 地址：https://github.com/dmeranda/demjson

官方地址：http://deron.meranda.us/python/demjson/

环境配置
在使用 Demjson 编码或解码 JSON 数据前，我们需要先安装 Demjson 模块。本教程我们会下载 Demjson 并安装：

$ tar -xvzf demjson-2.2.3.tar.gz
$ cd demjson-2.2.3
$ python setup.py install

JSON 函数
函数		描述
encode		将 Python 对象编码成 JSON 字符串
decode		将已编码的 JSON 字符串解码为 Python 对象
encode
		Python encode() 函数用于将 Python 对象编码成 JSON 字符串。

语法
demjson.encode(self, obj, nest_level=0)

decode
Python 可以使用 demjson.decode() 函数解码 JSON 数据。该函数返回 Python 字段的数据类型。

语法
demjson.decode(self, txt)