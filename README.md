# CleanCode:代码简洁之道阅读笔记

    阅读本书的目的：学习书中的列举的原则和标准，培养实际项目中的代码习惯。

## 第一章：整洁代码
  ### 整洁代码应该具备的特征：
    1.代码逻辑简单直白，使得缺陷难以隐藏；
    2.尽量减少依赖关系，便于维护；
    3.依据某种分层策略完善错误处理代码；
    4.性能调至最优，避免由他人优化引发的混乱；
    5.履行单一职能原则，高内聚，类与类之间低耦合。
    6.有单元测试和验收测试；
    7.命名清晰无歧义；
    8.尽量“少”：类，方法，函数等

  ### 两条重要原则：
    1.尽量让代码易读，开发时减少读的时间。
    2.童子军军规：“让营地比你来时更干净”。
## 第二章：有意义的命名
  ### 命名原则：
    1.名副其实：命名直接反映代码的功能，无需多余的解释；
    2.避免误导：避免使用与本意相悖的词；
    3.有意义的区分：杜绝name1,name2这样的区分；
    4.避免使用编码：不能乱用前缀；
    5.避免思维映射：避免使用歧义和联想的词汇；
    6.概念相合，专业，具有针对性。
  ### 具体命名：
    1.类名：名词或名词短语；
    2.方法名：动词或者动词短语；
    3.语境：良好命名的类、函数、参数相互联系提供语境；

## 第三章：函数
  ### 原则
      1.短小，只做一件事。
      2.抽象层级：要确保函数只做一件事，函数中的语句都要在同一抽象层级上。
      3.自顶向下读代码：抽象层级由总至分的逐级展开。
      4.switch语句：尽量避免switch，switch中的跳转不符合单一职能原则。
      5.使用描述性的名称。
      6.函数参数：最理想的参数数量是零，有足够的理由才能用三个以上参数，更多参数需要封装成类。
      7.函数返回值：对于转换类的函数，必须有返回值，对应其表述。
      8.对于一元函数，函数和参数应当形成一种非常良好的动词/名词对形式。
      9.无副作用：函数承诺只做一件事，如果进行其他事避免时序性耦合及顺序依赖。

  ### 错误处理
      1.从指令式函数返回错误码轻微违反了指令与询问分隔的规则。
      2.最好把try和catch代码块的主体部分抽离出来，另外形成函数
      3.错误处理就是一件事，处理错误的函数不该做其他事
      4.依赖磁铁：其他许多类都得导入和使用它，如一些错误码枚举类。







