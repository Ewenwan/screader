screader
========

The screader is a soure code reading tool based the libclang. It is implemented by the C.

     
     这里是用C语言写的。主要是根据输入的待分析文件或待分析目录，去分析所有输入的文件，列出文件的AST节点信息。同时，screader还可以在文件后面输入要查找的关键字，然后输出关键字所在节点的相关信息。       这个小工具很简单，几乎没有任何实际使用价值，价值主要在演示了如何调用libclang去做AST分析。有初学者想学习这块内容的话，可以作为参考。



How to build the scread:
---------------------------------------------------------
1. You must install the clang on your computer.
   You can follow the doc: http://clang.llvm.org/get_started.html.
   But after you "make", you must "make install".

2. After you install the clang, you can use "clang -v" to check your clang version.

3. Use git clone the source code of scread to you computer.

4. Make directory build under the scread directory.

5. Under the build directory, use the cmd:
   cmake ..
   make

6. Then you can get the scread under the build directory.


How to use the scread:
------------------------------------------------------------

You must come to the directory of the scread.

1. If you want to use the scread to output all the informations of ast nodes:
   You can use it like that: ./scread xxx.cpp(or xxx.c, xxx.h)

2. If you just want to get the keyword information, you can use it like this:
   ./scread xxx.cpp keyword

3. We store some testcase under the scread/test/. So, you can use the scread like this:
   ./scread ../test/Node.h
   ./scread ../test/HelloWorld.cpp printf
