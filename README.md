# os
系统知识
第一步：打开命令行界面并且确认gcc.exe确实可用

键盘win + r   （ 这里的r是run的意思）

输入cmd,回车，你就看到了命令行

输入gcc -v       --如果返回了结果，那么继续，如果不识别，那么请立刻参考本文的“附录”

第二步：写程序

在你的E盘，信件文件夹，命名为myc

在E:\myc内部，右键 → 新建 → 文本文档

你会看到下面的：
新建文本文档.txt.png
新建文本文档.txt.png

如果你没看到.txt这个文件扩展名，那么你需要简单设置一下，请你百度“win7系统如何显示文件的扩展名”或者“win8系统如何显示文件扩展名”。

在这个.txt内部输入下面的代码：

#include<stdio.h>
int main()
{
    double a,b;
    printf("请输入第一个实数a = \n");
    scanf("%lf",&a);
    printf("请输入第一个实数b = \n");
    scanf("%lf",&b);
    printf("a和b的和 = a + b =\t %f\n",a+b);
    printf("a和b的差 = a - b =\t %f\n",a-b);
    printf("a和b的积 = a × b =\t %f\n",a*b);
    printf("a和b的商 = a ÷ b =\t %f\n",a/b);
    return 0;
}

关闭并且保存。
重命名这个文件：把新建文本文档.txt改成test001.c.
第三步：编译运行这个test001.c

在你打开的cmd窗口依次运行下面的命令

E:

cd myc

gcc test001.c

这里的cd是change directory的意思。此时你会发现生成了一个新的文件a.exe

输入命令

.\a.exe

你就开始执行已经编译好的程序了。
自然，你也可以直接双击这个a.exe来运行它

附录：
当你输入gcc时，之所以你看到了：

    不是内部或外部命令，也不是可运行的程序或批处理文件。

是因为你没有在自己的环境变量之中添加gcc.exe的路径。于是系统完全不知道去哪里寻找gcc.exe。
做法如下：

    我的电脑 → 右键 → 属性 → 高级系统设置 → 高级 → 环境变量 → 在系统变量之中找到path→ 点击编辑 → 在后面加入类似下面的路径;C:\TDM-GCC-64\bin;C:\Program Files (x86)\Dev-Cpp\MinGW64\bin → 确定 → 确定
    [！！！这是我的pc上的，你的电脑上的路径不一定是这个哦！！！]
    并且注意前面的英文分号;隔开

这里，在我的电脑上：
1.gcc.exe编译器位于C:\TDM-GCC-64\bin
2.x86_64-w64-mingw32-gcc.exe编译器位于C:\Program Files (x86)\Dev-Cpp\MinGW64\bin 于是，我加入这样的路径：

    ;C:\TDM-GCC-64\bin;C:\Program Files (x86)\Dev-Cpp\MinGW64\bin

你的电脑上具体在哪里，你可以自己找一下。也可以安装一个神奇的软件名字叫everything，用这个everything软件搜一下gcc.exe就可以看到了。

当然了你的电脑上最好先存在C语言的一个编译器。只要你装了vc++6.0或者dev-c++或者什么别的，都会有的。

此外，下面有cd命令的其他用法：

D:              进入D盘
C:              进入C盘
cd myc      --可以进入到名字为myc的目录（必须C盘存在这个文件夹）
cd..         可以返回上一层目录
cd\         返回到根目录
cd d:\myc   进入D盘的名字为myc的目录
cd /?        查看cd命令的具体用法。

作者：masakakaikai
链接：http://www.jianshu.com/p/ff6f2a2bf75a
來源：简书
著作权归作者所有。商业转载请联系作者获得授权，非商业转载请注明出处。
