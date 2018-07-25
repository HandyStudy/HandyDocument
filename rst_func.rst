reStructuredText常用语法1
=========================

行内样式
--------

粗体显示
>>>>>>>>

规则
  左右两边各加两个*号，*号和文本之间不要留空格

**原文本**
::

**粗体**

**显示**
 **粗体**


斜体显示
>>>>>>>>

规则
  左右两边加*号，*号和文本之间不要留空格

**原文本** 
::

*斜体*

**显示**
 *斜体*


等宽文本
>>>>>>>>

规则
  左右两边各加两个``号

**原文本**
::
  ``等宽文本，hello world！``

**显示信息**

 ``等宽文本，hello world！``


解读文本
>>>>>>>>>>>>>>>>>>>>>>>>>>>

规则
  用`   `把文本引用起来即可。  

**原文本**
::

  这是解读文本： `解读文本，Interpreted Text`

**显示信息**

 这是解读文本： `解读文本，Interpreted Text`



上下标
>>>>>>

规则
  有时要进行数学/化学的表示,在 html 中就需要上/下标( <sub> , <sup>) 的表达, rST 中当然也有:  

**原文本**
::

  H\ :sub:`2`\ O

  E = mc\ :sup:`2`

**显示信息**

 H\ :sub:`2`\ O

 E = mc\ :sup:`2`



换行
>>>>>>>>

规则
  行内文本如果要强制换一行显示，加一个空行即可。

**原文本**
::

  这是一段换行对齐继续写的文字，
  但前面没有加空行，故而会连续显示。

  本行前面加了一个空行，会强制换行显示。

**显示信息**

 这是一段换行对齐继续写的文字，
 但前面没有加空行，故而会连续显示。

 本行前面加了一个空行，会强制换行显示。


分隔符
-------

规则
>>>>>
  分隔符就是一条水平的横线，是由 4 个 - 或者更多组成，需要添加换行。

示范
>>>>>
**原文本**
::

 ----

**显示信息**

----


注释(Comments)
---------------
规则
>>>>>
  注释以 .. 开头，后面接注释内容即可，可以是多行内容，多行时每行开头要加一个空格。

示范
>>>>>
**原文本**
::

    ..
     我是注释内容
     你们看不到我

**显示信息**

..
 我是注释内容
 你们看不到我


定义列表（解释列表）
--------

规则
>>>>>

   定义列表可以理解为解释列表，即名词解释。

   条目占一行，解释文本要有缩进；

      多层可根据多次缩进实现
   
   解释文本加一条空行实现换一行，不加空行的同级接着继续显示。

   条目和解释文本之间，如果不留空行，条目会自动加粗显示，留空行则不会。


示范
>>>>>

**原文本**
:: 

   这里是通过缩进实现的解释文本1！

     这里是通过继续缩进实现的多层解释文本1A！ 

       这里是通过继续缩进实现的多层解释文本1A1！ 

   这里是通过缩进实现的解释文本2！

   这里是通过缩进实现的解释文本3！
    
**显示信息**
   这里是通过缩进实现的解释文本1！

     这里是通过继续缩进实现的多层解释文本1A！ 

       这里是通过继续缩进实现的多层解释文本1A1！ 

   这里是通过缩进实现的解释文本2！

   这里是通过缩进实现的解释文本3！


字段列表
--------
规则
>>>>>
 字段列表以 : 开头，同时也以 : 结尾。

示范
>>>>>

**原文本**
::

    :标题: reStructuredText语法说明

    :作者: zeping

    :时间: 2016年06月21日

    :概述: 这是一篇
     关于reStructuredText

     语法说明

**显示信息**

:标题: reStructuredText语法说明

:作者: zeping

:时间: 2016年06月21日

:概述: 这是一篇
 关于reStructuredText

 语法说明


符号列表
--------
规则
>>>>
   #. 符号列表可以使用 +、-、* 来表示
   #. 下级列表需要至少有两个空格缩进
   #. 上级和它的下级列表需要有一条空行，或者它的下级列表缩进3个空格
   #. 层级不限
   #. 不同层级之间、或者相同层级，可以混用符号


示范
>>>>>

**原文本**
::

   * 一级列表A

      + 二级列表A1
      + 二级列表A2

   * 一级列表B

      + 二级列表B1
      + 二级列表B2

         - 三级列表B21

            * 四级列表B211
            * 四级列表B212
         - 三级列表B22
      + 二级列表B3
   * 一级列表C

**显示信息**
   * 一级列表A

      + 二级列表A1
      + 二级列表A2

   * 一级列表B

      + 二级列表B1
      + 二级列表B2

         - 三级列表B21

            * 四级列表B211
            * 四级列表B212
         - 三级列表B22
      + 二级列表B3
   * 一级列表C



顺序列表
--------
规则
>>>>
  可以使用的枚举有：

  #. 阿拉伯数字: 1, 2, 3, ... (无上限)。
  #. 大写字母: A-Z。
  #. 小写字母: a-z。
  #. 大写罗马数字: Ⅰ,Ⅱ,Ⅲ,Ⅳ, ..., MMMMCMXCIX (4999)。
  #. 小写罗马数字: ⅰ,ⅱ,ⅲ,ⅳ, ..., mmmmcmxcix (4999)。
  #. 枚举列表可以结合 # 自动生成枚举序号。
  
  可以为序号添加前缀和后缀:

  * . 后缀: "1.", "A.", "a.", "I.", "i."
  * () 包起来: "(1)", "(A)", "(a)", "(I)", "(i)"
  * ) 后缀: "1)", "A)", "a)", "I)", "i)"



示范
>>>>>

**原文本**
::

   1. 一级列表A
   
       A) 二级列表A1
       #) 二级列表A2

   #. 一级列表B

       I) 二级列表B1T
       #) 二级列表B2

            a 三级列表B21

                 a. 四级列表B211
                 #. 四级列表B212

            b 三级列表B22

       #) 二级列表B3
   #. 一级列表C

**显示信息**

   1. 一级列表A
   
       A) 二级列表A1
       #) 二级列表A2

   #. 一级列表B

       I) 二级列表B1T
       #) 二级列表B2

            a 三级列表B21

                 a. 四级列表B211
                 #. 四级列表B212

            b 三级列表B22

       #) 二级列表B3
   #. 一级列表C


选项列表
--------
规则
>>>>>
 + 选项列表是一个类似两列的表格，左边是参数，右边是描述信息。
 + 第一列（参数列）必须以 - 或者 / 开头，后面紧跟字符不能留空格
 + ' - ' 或者 ' / ' 及之后的所用字符均作为第一列内容，字符间
   可以由一个空格，加两个空格就是第二列（描述信息列）
 + 当参数选项过长时，参数选项和描述信息各占一行。
 + 选项与参数之间有一个空格，参数选项与描述信息之间至少有两个空格。

示范
>>>>>

**原文本**
::

    -a            command-line option "a" 
    -b file       options can have arguments
                  and long descriptions
    --long        options can be long also
    --input=file  long options can also have
                  arguments
    /V            DOS/VMS-style options too

**显示信息**

-a            command-line option "a" 
-b file       options can have arguments
              and long descriptions
--long        options can be long also
--input=file  long options can also have
              arguments
/V            DOS/VMS-style options too


块(Blocks)
-----------

文字块(Literal Blocks)
>>>>>>>>>>>>>>>>>>>>>>

规则：
  * 文字块就是一段文字信息，原文本是什么，就输出什么。
  * 在段落末尾加上 ::，接着一个空行，然后写文字块。
  * 也可以在一个空行上添加::, 接着一个空行，然后写文字块，这个双冒号行将被忽略。
  * 文字块不能顶头写，要有缩进，到没有缩进的行为止。
  * 常用来输出程序代码、格式原文本等。

**示范1：reStructuredText原文本和显示对照输出**

**原文本**
::

   这是reStructuredText的符号列表：

      * 列表项目1
      * 列表项目2
      * 列表项目3

   这是reStructuredText的顺序列表：

      #. 列表项目1
      #. 列表项目2
      #. 列表项目3

**显示信息**

   这是reStructuredText的符号列表：

      * 列表项目1
      * 列表项目2
      * 列表项目3

   这是reStructuredText的顺序列表：

      #. 列表项目1
      #. 列表项目2
      #. 列表项目3

**示范2：输出程序代码**

如果数据库有问题, 执行下面的 SQL::

 # Dumping data for table `item_table`

 INSERT INTO item_table VALUES (
   0000000001, 0, 'Manual', '', '0.18.0',
   'This is the manual for Mantis version 0.18.0.\r\n\r\nThe Mantis manual is modeled after the [url=http://www.php.net/manual/en/]PHP Manual[/url]. It is authored via the \\"manual\\" module in Mantis CVS.  You can always view/download the latest version of this manual from [url=http://mantisbt.sourceforge.net/manual/]here[/url].',
   '', 1, 1, 20030811192655);



行块(Line Blocks)
>>>>>>>>>>>>>>>>>>

 * 行块对于地址、诗句以及无装饰列表是非常有用的。
 * 行块是以 | 开头，每一个行块可以是多段文本。
 * '|' 前后各有一个空格。

**原文本**
::

    下面是行块内容：
     | 这是一段行块内容
     | 这同样也是行块内容
       还是行块内容

    这是新的一段。

**显示信息**

下面是行块内容：
 | 这是一段行块内容
 | 这同样也是行块内容
   还是行块内容

这是新的一段。


块引用(Block Quotes)
--------------------

规则
>>>>>

 * 块引用是通过缩进来实现的，引用块要在前面的段落基础上缩进。
 * 通常引用结尾会加上出处(attribution)，出处的文字块开头是 --、--- 、—，后面加上出处信息。
 * 块引用可以使用空的注释 .. 分隔上下的块引用。
 * 注意在新的块和出处都要添加一个空行。

示范
>>>>>

**原文本**
::

 下面是引用的内容：
 
    “真的猛士，敢于直面惨淡的人生，敢于正视淋漓的鲜血。”

    --- 鲁迅

 ..

      “人生的意志和劳动将创造奇迹般的奇迹。”

      — 涅克拉索


**显示信息**

 下面是引用的内容：
 
    “真的猛士，敢于直面惨淡的人生，敢于正视淋漓的鲜血。”

    --- 鲁迅

..

      “人生的意志和劳动将创造奇迹般的奇迹。”

      — 涅克拉索


文档测试块(Doctest Blocks)
---------------------------
规则
>>>>>
 * 文档测试块是交互式的Python会话，以 >>> 开始，一个空行结束。
 * 文档测试块和文字块有点类似，都是把一段原文在显示框中原样显示出来。
   文字块是::开头，留一个空行，里面文字块要缩进，不能顶头写。遇顶头写文字结束。
   文档测试块是>>> 开头（注意>>>后有一个空格），里面文字块无需缩进，遇空行结束。

示范
>>>>>

**原文本**
::

 >>> print "This is a doctest block."
 This is a doctest block.

**显示信息**

>>> print "This is a doctest block."
This is a doctest block.

程序块(Doctest Blocks)
---------------------------
规则
>>>>>
  可以 用 .. code-block:: 追加各种语法高亮声明:

示范
>>>>>

**原文本**
::
    .. code-block:: python
        :linenos:

        def foo():
            print "Love Python, Love FreeDome"
            print "E文标点,.0123456789,中文标点,. "

**显示信息**

.. code-block:: python
    :linenos:

    def foo():
        print("Love Python, Love FreeDome")
        print("E文标点,.0123456789,中文标点,. ")


表格(Tables)
------------

网格表(Grid Tables)
>>>>>>>>>>>>>>>>>>>>

**规则**

  * 网格表中使用的符号有：-、=、|、+。

  *  = 用来分隔表头和表体行，- 用来分隔行，| 用来分隔列，+ 用来表示行和列相交的节点。


**原文本**
::

    +------------+------------+-----------+
    | Header 1   | Header 2   | Header 3  |
    +============+============+===========+
    | body row 1 | column 2   | column 3  |
    +------------+------------+-----------+
    | body row 2 | Cells may span columns.|
    +------------+------------+-----------+
    | body row 3 | Cells may  | - Cells   |
    +------------+ span rows. | - contain |
    | body row 4 |            | - blocks. |
    +------------+------------+-----------+


**显示信息**

+------------+------------+-----------+
| Header 1   | Header 2   | Header 3  |
+============+============+===========+
| body row 1 | column 2   | column 3  |
+------------+------------+-----------+
| body row 2 | Cells may span columns.|
+------------+------------+-----------+
| body row 3 | Cells may  | - Cells   |
+------------+ span rows. | - contain |
| body row 4 |            | - blocks. |
+------------+------------+-----------+


简单表(Simple Tables)
>>>>>>>>>>>>>>>>>>>>>>

规则
  简单表相对于网格表，少了 | 和 + 两个符号，只用 - 和 = 表示。


**原文本**
::

    ========  ========  =========
    Inputs                Output
    ------------------  ---------
    A             B       A or B
    ========  ========  =========
    False      False     False
    True       False     True
    False      True      True
    True       True      True
    =====      =====     ======

**显示信息**

========  ========  =========
Inputs               Output
------------------  ---------
A             B       A or B
========  ========  =========
False      False     False
True       False     True
False      True      True
True       True      True
========  ========  =========

CSV表格
>>>>>>>

规则
  * 以.. csv-table:: 开头，后面跟表格标题。
  * 以:header: 定义表头的内容和个数。
  * 以:widths: 定义每列的宽度
  * 空一行之后，每行的数据用逗号,分隔 


**原文本**
::

    .. csv-table:: 我的CSV表格
    :header: "Treat", "Quantity", "Description"
    :widths: 15, 10, 30

    "Albatross", 2.99, "On a stick!"
    "Crunchy Frog", 1.49, "If we took the bones out, it wouldn't be
    crunchy, now would it?"
    "Gannet Ripple", 1.99, "On a stick!"

**显示信息**

.. csv-table:: 我的CSV表格
 :header: "Treat", "Quantity", "Description"
 :widths: 15, 10, 30

 "Albatross", 2.99, "On a stick!"
 "Crunchy Frog", 1.49, "If we took the bones out, it wouldn't be
 crunchy, now would it?"
 "Gannet Ripple", 1.99, "On a stick!"


列表表格
>>>>>>>>>

规则
  * 以.. list-table::开头，后面跟表格标题。
  * 以:widths: 定义每列的宽度
  * 以:header-rows: 定义表头的开始行
  * 空一行之后，每行的数据用一个列表显示 


**原文本**
::

    .. list-table:: 列表表格
      :widths: 15 10 30
      :header-rows: 1

      * - Treat
        - Quantity
        - Description
      * - Albatross
        - 2.99
        - On a stick!
      * - Crunchy Frog
        - 1.49
        - If we took the bones out, it wouldn't be
        crunchy, now would it?
      * - Gannet Ripple
        - 1.99
        - On a stick!

**显示信息**

.. list-table:: 列表表格
  :widths: 15 10 30
  :header-rows: 1

  * - Treat
    - Quantity
    - Description
  * - Albatross
    - 2.99
    - On a stick!
  * - Crunchy Frog
    - 1.49
    - If we took the bones out, it wouldn't be
      crunchy, now would it?
  * - Gannet Ripple
    - 1.99
    - On a stick!



超链接
------

自动超链接
>>>>>>>>>>
  reStructuredText会自动将网址生成超链接。

https://handydocument.readthedocs.io



外部超链接(External Hyperlink)
>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>
  引用/参考(reference)，是简单的形式，只能是一个词语，引用的文字不能带有空格。

**原文本（示范1）**
::

 这篇文章来自我的ReadTheDocs,请参考 reference_。

 .. _reference: https://HandyDocument.readthedocs.io/

**显示信息（示范1）**

这篇文章来自我的ReadTheDocs,请参考 reference_。

.. _reference: https://HandyDocument.readthedocs.io/

**原文本（示范2）**
::

 这篇文章来自我的ReadTheDocs,请参考 `HandyDocument <https://HandyDocument.readthedocs.io/>`_。

**显示信息（示范2）**

这篇文章来自我的ReadTheDocs,请参考 `HandyDocument <https://HandyDocument.readthedocs.io/>`_。



内部超链接|锚点(Internal Hyperlink)
>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>
规则
  * 在每个文档的不同位置，加入一些锚点
  * 格式如下：.. _你的锚点名称:
  * 在其它任意文本中，随时可以使用:ref:`超链接显示信息 <你的锚点名称>`跳转到这个文档的这个位置

**原文本**
::

 更多信息参考 引用文档_

 .. _引用文档:

 更多信息，请参考 `reStructuredText <rstindex>`_。

**显示信息**

更多信息参考 引用文档_

.. _引用文档:

更多信息，请参考 `reStructuredText <rstindex>`_。


匿名超链接(Anonymous hyperlink)
>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>
 词组(短语)引用/参考(phrase reference)，引用的文字可以带有空格或者符号，需要使用反引号引起来。

**原文本**
::

 这篇文章参考的是：`Quick reStructuredText`__。

 .. __: http://handydocument.readthedocs.io

**显示信息**

这篇文章参考的是：`Quick reStructuredText`__。

.. __: http://handydocument.readthedocs.io



间接超链接(Indirect Hyperlink)
>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>
 间接超链接是基于匿名链接的基础上的，就是将匿名链接地址换成了外部引用名_。

**原文本**
::

 HandyStudy_ 是 `我的 GitHub 用户名`__。

 .. _HandyStudy: https://github.com/HandyStudy/

 __ HandyStudy_

**显示信息**

HandyStudy_ 是 `我的 GitHub 用户名`__。

.. _HandyStudy: https://github.com/HandyStudy/

__ HandyStudy_



隐式超链接(Implicit Hyperlink)
>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>
 小节标题、脚注和引用参考会自动生成超链接地址，使用小节标题、脚注或引用参考名称作为超链接名称就可以生成隐式链接。

**原文本**
::

 `行内样式`_，即可生成到行内样式那一节的超链接。

 `分隔符`_，即可生成到分隔符那一节的超链接。

**显示信息**

`行内样式`_，即可生成到行内样式那一节的超链接。

`分隔符`_，即可生成到分隔符那一节的超链接。



替换引用(Substitution Reference)
>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>
 替换引用就是用定义的指令替换对应的文字或图片，和内置指令(inline directives)类似。

**原文本**
::

 这是 |logo| github的Logo，我的github用户名是:|name|。

 .. |logo| image:: https://help.github.com/assets/images/site/favicon.ico
 .. |name| replace:: HandyStudy

 这是一个本地图片 |test_pic|

 .. |logo1| image:: _static/test_pic.jpg

**显示信息**

这是 |logo| github的Logo，我的github用户名是:|name|。

.. |logo| image:: https://help.github.com/assets/images/site/favicon.ico
.. |name| replace:: HandyStudy

这是一个本地图片 |test_pic|

.. |test_pic| image:: _static/test_pic.jpg



脚注引用(Footnote Reference)
>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>
 脚注引用，有这几个方式：有手工序号(标记序号123之类)、自动序号(填入#号会自动填充序号)、自动符号(填入*会自动生成符号)。

 手工序号可以和#结合使用，会自动延续手工的序号。

 # 表示的方法可以在后面加上一个名称，这个名称就会生成一个链接。

**原文本**
::

    脚注引用一 [1]_

    脚注引用二 [#]_

    脚注引用三 [#链接]_

    脚注引用四 [*]_

    脚注引用五 [*]_

    脚注引用六 [*]_

    .. [1] 脚注内容一
    .. [2] 脚注内容二
    .. [#] 脚注内容三
    .. [#链接] 脚注内容四 链接_
    .. [*] 脚注内容五
    .. [*] 脚注内容六
    .. [*] 脚注内容七

**显示信息**

脚注引用一 [1]_

脚注引用二 [#]_

脚注引用三 [#链接]_

脚注引用四 [*]_

脚注引用五 [*]_

脚注引用六 [*]_

.. [1] 脚注内容一
.. [2] 脚注内容二
.. [#] 脚注内容三
.. [#链接] 脚注内容四 链接_
.. [*] 脚注内容五
.. [*] 脚注内容六
.. [*] 脚注内容七


引用参考(Citation Reference)
>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>
 引用参考与上面的脚注有点类似。

**原文本**
::

    引用参考的内容通常放在页面结尾处，比如 [One]_，Two_

    .. [One] 参考引用一

    .. [Two] 参考引用二

**显示信息**

引用参考的内容通常放在页面结尾处，比如 [One]_，Two_

.. [One] 参考引用一

.. [Two] 参考引用二



章节标题(2级标题)
--------

规则(3级标题)
>>>>>

  #. 标题用上标和下标符号表示，最多分六级
  #. 小标符号长度不得小于标题长度
  #. 符号可以自由组合使用，按出现的先后，依次排列
  #. 表示标题的符号有 =、-、`、:、'、"、~、^、_ 、* 、+、 #、<、> 
  #. 符号既可以上标，也可以下标，相同符号，上标比下标高一级
  #. 章节标题是否显示数字需要，在主题树(toctree)中使用:numbered:表示，:numbered:3 表示3级章节标题显示数字序号。

样例(3级标题)
>>>>>

::

    四级标题（示范）
    +++++++++++++++
    五级标题（示范）
    :::::::::::::::
    六级标题（示范）
    ~~~~~~~~~~~~~~

四级标题（示范）
+++++++++++++++
五级标题（示范）
:::::::::::::::
六级标题（示范）
~~~~~~~~~~~~~~