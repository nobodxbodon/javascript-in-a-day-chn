## 共享协议
本作使用[署名-非商业使用-禁止演绎](https://creativecommons.org/licenses/by-nc-nd/4.0/)协议共享。

# JavaScript编程一天入门

## 前言

每一讲建议时间30分钟左右. 如果卡住(比如超过一小时), 请在代码库开issue. 目的是让总时间控制在8小时左右, 让"一天入门"更符合实际.

## 目录

## 一 开编

从一句废话开始吧, 没有JavaScript, 就没有今天的网络花花世界. 它的前世今生虽不在这里评论, 但确实非常曲折精彩. 请有兴趣的自行了解.

不同于其他一些编程语言需要在编程前花点时间安装和设置, 比如Java. JavaScript编程是几乎可以立刻开始的, 只要你的电脑上装了一个网页浏览器. 火狐(Firefox), Chrome, IE都提供控制台(Console)功能. 本文将用Chrome. (起先用的是火狐, 但在控制台输入中文代码时, 发现它的代码提示功能和中文输入法有冲突)

打开控制台后, 上半部是输出, 取决于你当前打开的页面是什么, 内容也许是空白, 也许是一堆错误或者警告, 可以无视之, 以后就会都看懂的. 关键是下半部(默认高度只有一行), 有个 >> 的提示符号(其他浏览器可能是单个 >). 这里就是我们开始第一个程序的地方.

先问个好吧:
```
console.log("你好");
```
回车运行后, 可以看到输出部分除了重复这个程序, 还输出了这样两行(不同浏览器格式也许不同):
```
    你好
<-  undefined
```
"你好"是代码运行后打出的. <- 指向的是返回值. undefined的意思是没有返回任何值. 那怎样能返回一个值呢? 试试1+1:
```
1+1;
```
运行后, 看到结果是:
```
<- 2
```
接下去, 为了本人省力起见, 运行结果之前的<-将不再重复.

想知道二十年前就开始人人喊打的网络弹窗是怎样做的吗? 试试下面:
```
alert("确定要离开网站吗?");
```

再试试把上面几句组合起来,或者重复几遍放在一行里看看是什么效果? 恭喜! 你已经可以写出无穷个JavaScript程序了.

当然, 为了拯救眼睛, 不可能所有的程序都一行搞定. 在控制台里, shift + 回车可以做到换行但不执行代码. 

扩展资料: 解释器与编译器的区别, JavaScript的历史

## 二 熟能生巧

下面做一件非常简单的事, 根据一个人的岁数, 算算出生之后过了几个月. 比如20岁
```
20*12;
```
如果觉得程序的"回答"太"精简"和生硬了,那么人性化一些吧:
```
console.log("20岁的人已经过了" + 20*12 + "个月咯");
```
问题是, 如果想知道十年后, 二十年后的情况, 就要把两处"20"的值改掉, 再运行. 这种麻烦可要不得!
```
function 过了几个月(岁数) {
  console.log(岁数 + "岁的人已经过了" + 岁数*12 + "个月咯");
}
```
而后我们可以这样运行:
```
过了几个月(30);
```
这就是定义一个函数和调用这个函数的例子.

注: (取自网络) "函数”一词是转译词．是我国清代数学家李善兰在翻译《代数学》（1895年）一书时，把“function”译成函数的．中国古代“函”字与“含”字通用，都有着“包含”的意思，李善兰给出的定义是：“凡式中含天，为天之函数. ”

"过了几个月"包含了"岁数", 它就是"岁数"的函数.

## 三 记忆

```
var 大学毕业年份 = 2017;
var 高中毕业年份 = 大学毕业年份 - 4;
var 初中毕业年份 = 高中毕业年份 - 3;
var 小学毕业年份 = 初中毕业年份 - 3;
var 上小学年份 = 小学毕业年份 - 6;
"我学了" + (大学毕业年份 - 上小学年份) + "年";
```
上面的所有年份都有个名称, 而且有个对应值. 想让程序记住什么的话, 就给它起个名字, 后面就可以用了. 俗称变量. 那么是任何地方都能用吗?

不是. 上一节介绍了函数, 它内部定义的变量, 只有这个函数内部可以引用

(待续)

## 造个人

function 人类(姓名, 年龄) {
  this.姓名 = 姓名;
  this.年龄 = 年龄;
  this.自我介绍 = function(){
    console.log("我叫" + 姓名 + ", 今年" + 年龄 + "岁");
  }
}


## DOM

下面的程序能读取控制台所在网页的网址:
```
document.URL
```
比如在本文的github项目首页打开控制台后运行的结果就是:
```
"https://github.com/nobodxbodon/javascript-in-a-day-chn"
```


