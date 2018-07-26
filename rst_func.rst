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


删除线
>>>>>>>>

**原文本**
::
    .. role:: strike
       :class: strike

    :strike:`删除线` 效果

    不留白的\ :strike:`删除线`\ 效果


.. role:: strike
   :class: strike

:strike:`删除线` 效果

不留白的\ :strike:`删除线`\ 效果


下划线
>>>>>>>>

**原文本**
::

    .. role:: ul
       :class: underline

    :ul:`下划线` 效果

    不留白的\ :ul:`下划线`\ 效果

.. role:: ul
   :class: underline

:ul:`下划线` 效果

不留白的\ :ul:`下划线`\ 效果


等宽文本
>>>>>>>>

规则
  左右两边各加两个``号

**原文本**
::
  ``等宽文本，hello world！``

**显示信息**

 ``等宽文本，hello world！``


引言
>>>>>
规则
  用`   `把文本引用起来即可。  

**原文本**
::

  `Handy Document` by Zeping.Long

**显示信息**

 `Handy Document` by Zeping.Long



转义
>>>>>>

规则
  * 反斜线作为转义字符，\  
  * 禁止对后面 \*字符* 做语法解析。

**原文本**
::

  应用转义字符\\，输出转义字符\\

  应用转义字符\\，\*汉字*，直接输出*，而不会输出为斜体

  应用转义字符\\，\**汉字**，直接输出**，而不会输出为粗体

**显示信息**

  应用转义字符\\，输出转义字符\\

  应用转义字符\\，\*汉字*，直接输出*，而不会输出为斜体

  应用转义字符\\，\**汉字**，直接输出**，而不会输出为粗体


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


清除标记空白
>>>>>>>>>>>>

规则
  标记符号前后空白用::

     \ **反斜线**\ 消除

**原文本**
::

  标记符号前后空白\
  用\ **反斜线**\ 消除

**显示信息**

标记符号前后空白\
用\ **反斜线**\ 消除


分割线
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
  注释以 .. 开头，后面接注释内容即可，可以是多行内容，缩进内容也是注释

示范
>>>>>
**原文本**
::

    .. 我是注释内容1
     我是注释内容2
     你们看不到我

**显示信息**

.. 我是注释内容1
 我是注释内容2
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
    样式一：不留空行

    git
      Simple and beautiful.

    hg
      Another DVCS.

    subversion
      VCS with many constrains.

      Why not Git?

    样式二：留空行

    git

      Simple and beautiful.

    hg

      Another DVCS.

    subversion

      VCS with many constrains.

      Why not Git?


**显示信息**

样式一：不留空行	

git
  Simple and beautiful.

hg
  Another DVCS.

subversion
  VCS with many constrains.

  Why not Git?

样式二：留空行

git

  Simple and beautiful.

hg

  Another DVCS.

subversion

  VCS with many constrains.

  Why not Git?


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
   #. 上级和它的下级列表需要有一条空行
   #. 层级不限，列表层级和缩进有关,和具体符号无关。
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
  * 一般是在段落末尾加上 ::，接着一个空行，然后写文字块。
  * 也可以在一个空行上添加 :: , 接着一个空行，然后写文字块，这个双冒号行将被忽略。
  * ::可以放在任何段落的最后。如果::跟在空格字符之后，那么它将被忽略。如果::跟在字符后面，那么它将被转化成单个冒号。
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
  * '|' 符号后有一个空格。
  * 每一个新行都以一个管道符（“|”）开始。
  * 换行符和缩进都会被保留。
  * 连续的行是一个长行的组成部分，它们使用空格取代管道符作为开始。

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
>>>>>>>>>>>>>>>>>>>>>>
规则

 * 块引用是通过缩进来实现的，引用块要在前面的段落基础上缩进。
 * 通常引用结尾会加上出处(attribution)，出处的文字块开头是 --、--- 、—，后面加上出处信息。
 * 块引用可以使用空的注释 .. 分隔上下的块引用。
 * 注意在新的块和出处都要添加一个空行。

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
>>>>>>>>>>>>>>>>>>>>>>>>>>>

规则
 * 文档测试块是交互式的Python会话，以 >>> 开始，一个空行结束。
 * 文档测试块和文字块有点类似，都是把一段原文在显示框中原样显示出来。
   文字块是::开头，留一个空行，里面文字块要缩进，不能顶头写。遇顶头写文字结束。
   文档测试块是>>> 开头（注意>>>后有一个空格），里面文字块无需缩进，遇空行结束。

**原文本**
::

 >>> print "This is a doctest block."
 This is a doctest block.

**显示信息**

>>> print "This is a doctest block."
This is a doctest block.


程序
-----

规则
>>>>

  可以 用 .. code-block:: 追加各种语法高亮声明:

示范
>>>>>

**原文本**
::
    .. code-block:: python
        :linenos:
        :emphasize-lines: 2 

        def foo():
            print "Love Python, Love FreeDome"
            print "E文标点,.0123456789,中文标点,. "

**显示信息**

.. code-block:: python
    :linenos:
    :emphasize-lines: 2 

    def foo():
        print("Love Python, Love FreeDome")
        print("E文标点,.0123456789,中文标点,. ")


图片
-----

规则
>>>>>

  * 格式：.. image:: http链接（也可以是本地相对的文件名）
  * 可以通过height，Width，alt，align对图片显示属性进行设定。
  * 格式：.. figure:: http链接（也可以是本地相对的文件名）

示范
>>>>>

**原文本**
::
    格式一：

    .. image:: _static/test_pic.jpg
       :height: 50px
       :width: 300px
       :alt: 自己写的图片提示信息
       :align: center

    格式二：

    .. figure:: /images/github.png
       :width: 32

       图：GitHub Octocat

    格式三：

    - GitHub Logo: |octocat|
    .. |octocat| image:: /images/github.png
  
    格式四： 

    - 带链接的图片： |imglink|_
    .. |imglink| image:: /images/github.png
    .. _imglink: https://github.com/

    格式五：

    - 下图向右浮动。
    .. image:: /images/github.png
       :align: right



**显示信息**

格式一：

.. image:: _static/test_pic.jpg
   :height: 50px
   :width: 300px
   :alt: 自己写的图片提示信息
   :align: center

格式二：

.. figure:: _static/github.png
   :width: 32

   图：GitHub Octocat

格式三：

- GitHub Logo: |octocat|
.. |octocat| image:: _static/github.png

格式四：   

- 带链接的图片： |imglink|_
.. |imglink| image:: _static/github.png
.. _imglink: https://github.com/

格式五：

- 下图向右浮动。
.. image:: _static/github.png
   :align: right



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
  在文本中直接写入超链接(http,ftp,email均可以），reStructuredText会自动将网址生成超链接。

https://handydocument.readthedocs.io



外部超链接(External Hyperlink)
>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>
规则  
  * 格式：词语后面直接加 _ 符号，注意 _ 符号前不要留空格，词语前面必须有空格，就表示该词语带超链接
  * 包含空格或标点符号的超链接词语，需要使用反引号引用。
  * 然后定义超链接： .. _超链接词语：超链接
  * 也可以直接将超链接加<>符号后，写在超链接词语后面，然后一起用反引号，再加 _ 符号，注意 _ 符号前不要留空格
  * 注意：超链接词语，无论有没有用反引号引用起来，它与其它文字之间都必须有空格

**原文本（示范）**
::

 第一种超链接：这篇文章来自我的 ReadTheDocs_

 .. _ReadTheDocs: https://HandyDocument.readthedocs.io/

 第二种超链接：这篇文章来自我的 `Read The Docs`_

 .. _Read The Docs: https://HandyDocument.readthedocs.io/

 第三种超链接：这篇文章来自我的 `ReadTheDocs <https://HandyDocument.readthedocs.io/>`_


**显示信息**

 第一种超链接：这篇文章来自我的 ReadTheDocs_

 .. _ReadTheDocs: https://HandyDocument.readthedocs.io/

 第二种超链接：这篇文章来自我的 `Read The Docs`_

 .. _Read The Docs: https://HandyDocument.readthedocs.io/

 第三种超链接：这篇文章来自我的 `ReadTheDocs <https://HandyDocument.readthedocs.io/>`_



内部超链接|锚点(Internal Hyperlink)
>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>
规则
  * 定义方法：在每个文档的不同位置，加入一些锚点，格式如下::
  
        .. _锚点名称:
  * 在其它地方，随时可以使用锚点名称跳转到这个位置，这就是内部超链接。
  * 使用方法，有三种::

        1. 锚点名称_
        2. `描述文字 <#锚点名称>`__
        3. :ref:`锚点名称`
  * 锚点可以加在文档的任何位置，因为是 .. 注释符开始的注释，所以本身不会被显示出来。

**原文本**
::

    .. _fig1:

    .. figure:: _static/github.png

       内部跳转图例

    上面定义的位置，可以：

    - 通过 fig1_ 跳转。
    - 或者 `点击这里 <#fig1>`__ 跳转。
    - 或者参见 :ref:`fig1`


**显示信息**

 .. _fig1:

 .. figure:: _static/github.png

    内部跳转图例

 上面定义的位置，可以：

 - 通过 fig1_ 跳转。
 - 或者 `点击这里 <#fig1>`__ 跳转。
 - 或者参见 :ref:`fig1` 



匿名超链接(Anonymous hyperlink)
>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>

  * 如果有两个下划线而不是一个，那么不管是简单引用还是词组引用都可以是匿名的
  * 词组引用(phrase reference)，需要使用反引号引起来，引用的文字可以带有空格或者符号。
  * 本质上，就是多用一个 _ 符号，代替超链接词语


**原文本**
::

 这篇文章来自于： `Read the Docs`__

 .. __: http://handydocument.readthedocs.io

 这篇文章来自于： ReadtheDocs__

 .. __: http://handydocument.readthedocs.io


**显示信息**

这篇文章来自于： `Read the Docs`__

.. __: http://handydocument.readthedocs.io

这篇文章来自于： `ReadtheDocs`__

.. __: http://handydocument.readthedocs.io


间接超链接(Indirect Hyperlink)
>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>
  * 间接超链接是基于匿名链接的基础上的，就是将匿名链接地址换成了外部引用名。
  * 定义方法：__ 外部引用名_

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
  * 小节标题、脚注和引用参考会自动生成超链接地址
  * 可以使用小节标题、脚注或引用参考名称作为超链接名称，这会生成隐式链接
  * 带空格、符号的超链接名称，同样需要反引号引用起来

**原文本**
::

 行内样式_ ，即可生成到行内样式那一节的超链接。

 `文字块(Literal Blocks)`_ ，即可生成到文字块(Literal Blocks)那一节的超链接。

**显示信息**

`行内样式`_ ，即可生成到行内样式那一节的超链接。

`文字块(Literal Blocks)`_ ，即可生成到文字块(Literal Blocks)那一节的超链接。



替换引用(Substitution Reference)
>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>
  * 替换引用就是用定义的指令替换对应的文字或图片，和内置指令(inline directives)类似。
  * 自定义指令，必须用 | 符号引用起来，|自定义的指令名|
  * 自定义指令：.. |自定义的指令名| 内置指令:: 指令内容

**原文本**
::

 这是 |logo| github的Logo，我的github用户名是:|name|。

 .. |logo| image:: https://help.github.com/assets/images/site/favicon.ico
 .. |name| replace:: HandyStudy

 这是一个本地图片 |test_pic|

 .. |test_pic| image:: _static/test_pic.jpg

**显示信息**

这是 |logo| github的Logo，我的github用户名是:|name|。

.. |logo| image:: https://help.github.com/assets/images/site/favicon.ico
.. |name| replace:: HandyStudy

这是一个本地图片 |test_pic|

.. |test_pic| image:: _static/test_pic.jpg



脚注引用(Footnote Reference)
>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>
  * 脚注引用，有这几个方式：有手工序号(标记序号123之类)、自动序号(填入#号会自动填充序号)、自动符号(填入*会自动生成符号)。

  * 手工序号可以和#结合使用，会自动延续手工的序号。

  * # 表示的方法可以在后面加上一个名称，这个名称就会生成一个链接。

**原文本**
::

    reST脚注的多种表示法：

    - 脚注即可以手动分配数字 [1]_ ，
      也可以使用井号自动分配 [#]_ 。

    - 自动分配脚注 [#label]_ 也可以用
      添加标签形式 [#label]_ 多次引用。

    - 还支持用星号嵌入符号式脚注，
      如这个 [*]_ 和 这个 [*]_ 。

    - 使用单词做标识亦可 [CIT2012]_ 。


    .. [1] 数字编号脚注。
    .. [#] 井号自动编号。
    .. [#label] 井号添加标签以便多次引用。
    .. [*] 星号自动用符号做脚注标记。
    .. [*] 星号自动用符号做脚注标记。
    .. [CIT2012] 单词或其他规定格式。

**显示信息**

reST脚注的多种表示法：

- 脚注即可以手动分配数字 [1]_ ，
  也可以使用井号自动分配 [#]_ 。

- 自动分配脚注 [#label]_ 也可以用
  添加标签形式 [#label]_ 多次引用。

- 还支持用星号嵌入符号式脚注，
  如这个 [*]_ 和 这个 [*]_ 。

- 使用单词做标识亦可 [CIT2012]_ 。


.. [1] 数字编号脚注。
.. [#] 井号自动编号。
.. [#label] 井号添加标签以便多次引用。
.. [*] 星号自动用符号做脚注标记。
.. [*] 星号自动用符号做脚注标记。
.. [CIT2012] 单词或其他规定格式。


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
-----------------

规则(3级标题)
>>>>>>>>>>>>>

  #. 标题用上标和下标符号表示，最多分六级
  #. 小标符号长度不得小于标题长度
  #. 符号可以自由组合使用，按出现的先后，依次排列
  #. 表示标题的符号有 =、-、`、:、'、"、~、^、_ 、* 、+、 #、<、> 
  #. 符号既可以上标，也可以下标，相同符号，上标比下标高一级
  #. 章节标题是否显示数字需要，在主题树(toctree)中使用:numbered:表示，:numbered:3 表示3级章节标题显示数字序号。

样例(3级标题)
>>>>>>>>>>>>>

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