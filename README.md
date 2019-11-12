# REPL :Swift交互式解释器
Xode 6.1引入了另外一种以交互式的方式来体验Swift的方法。
Read Eval RintLoop,简称 REPL。
直接在命令行输入swift命令就可以打开REPL,在REPL里可以书写各种Swift代码



 1> let a = "1"
a: String = "1"

  2> Int(a)   //将a 转换为Int型，REAL会定义一个变量（$R0）指向这个转换之后值
$R0: Int? = 1

  3> let b = $R0 + 50
error: repl.swift:3:9: error: value of optional type 'Int?' must be unwrapped to a value of type 'Int'
let b = $R0 + 50
        ^

repl.swift:3:9: note: coalesce using '??' to provide a default when the optional value contains 'nil'
let b = $R0 + 50
        ^
        (   ?? <#default value#>)

repl.swift:3:9: note: force-unwrap using '!' to abort execution if the optional value contains 'nil'
let b = $R0 + 50
        ^
           !


  3>  let b = $R0! + 50
  b: Int = 51
    4>   func addTwoNumber(num1:Int,num2:Int)->Int{return num1 + num2}
    5>  let sum = addTwoNumber(num1:100,num2:50)
    sum: Int = 150
    
    
    
其它命令：
退出  :quit
帮助  :help
将光标移动到当前行的开始处   Control+A
将光标移动到当前行的结束处    Control+ E


