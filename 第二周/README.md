移动开发第二周作业
Jason数据结构调研小短文
简介：Jason全称Javascript Object Notation ，轻量级的数据交换格式，采用完全独立于语言的文本格式，被称为理想的数据交换语言，易于人阅读和便携，同时也易于及其解析；解析便捷、 快速，并且相同数据用JSON编辑所占的内存更小。
json格式采用key:value的方式记录数据，非常直观，比XML简洁，因而大受欢迎
JSON规定的格式：
1)数据在键值对中
2) 数据由逗号分隔
3) 花括号保存对象
4) 方括号保存数组

Jason有两种表示结构：对象和数组

1）对象结构以"{"大括号开始，以"}"大括号结束。中间部分由以","来分割开键值对（key/value）

[
  {"name":"Duke","age":"33","gender":"female"}
]

其中：关键字需要是字符串，而值可以是其他任何数据，比如：字符串，数值，布尔值，对象或者是null。

2）数组结构以"["方括号开始，"]"方括号结束。中中间部分由以","来分割对象。
简单 JSON 示例
最简单的：
{ "Name": "Mike" }
多个名称/值对串在一起时：
{ "Name": "Mike", "Gender": "Male", "email": "Mike@gmail.com" }
明确地表示以上三个值都是同一记录的一部分；花括号使这些值有了某种联系。

值的数组
当需要表示一组值时，JSON 不但能够提高可读性，而且可以减少复杂性。例如，假设您希望表示一个人名列表。

{
     "people": [
          { "firstName": "Brett", "lastName":"McLaughlin", "email": "brett@newInstance.com" },
          { "firstName": "Jason", "lastName":"Hunter", "email": "jason@servlets.com" },
          { "firstName": "Elliotte", "lastName":"Harold", "email": "elharo@macfaq.com" }
]}
在这个示例中，只有一个名为 people 的变量，值是包含三个条目的数组，每个条目是一个人的记录，其中包含姓名、性别和电子邮件地址。上面的示例演示如何用括号将记录组合成一个值。除此以外，也可以使用相同的语法表示多个值（每个值包含多个记录）：
{
 "programmers": [
      { "firstName": Mike", "gender": "Male", "email": "Mike@gmail.com" },
      { "firstName": "Jason", " gender ":" Male ", "email": "jason@servlets.com" },
      { "firstName": "Elliotte", " gender ":" Male ", "email": "elharo@macfaq.com" }
     ],
 
"authors": [
      { "firstName": "Isaac", " gender ": " Male ", "genre": "science fiction" },
      { "firstName": "Tad", " gender ": " Male ", "genre": "fantasy" },
      { "firstName": "Frank", " gender ": " Male ", "genre": "christian fiction" }
     ],
 
"musicians": [
      { "firstName": "Eric", "gender": "Male", "instrument": "guitar" },
      { "firstName": "Sergei", "gender": "Female", "instrument": "piano" }
     ]
}
总结
简单地说，JSON 可以将 JavaScript 对象中表示的一组数据转换为字符串，然后就可以在函数之间轻松地传递这个字符串。JavaScript 很容易解释它，而且 JSON 可以表示比名称/值对更复杂的结构。例如，可以表示数组和复杂的对象，而不仅仅是键和值的简单列表。JSON 是 JavaScript 原生格式，这意味着在JavaScript 中处理 JSON 数据不需要任何特殊的 API 或工具包。
如果使用 JSON，只需调用一个简单的函数，就可以获得经过格式化的数据，可以直接使用了。对于其他数据格式，需要在原始数据和格式化数据之间进行转换。


