李雷和韩梅梅坐前后排，上课想说话怕被老师发现，所以改为传纸条。为了不被老师发现他们纸条上写的是啥，，他们约定了如下方法传递信息：

将26个大写英文字母，外加空格，一共27个字符分成三组，每组9个。也就是ABCDEFGHI是第一组，JKLMNOPQR是第二组，STUVWXYZ*是第三组（此处用*代表空格）。

先根据月份数m,一整个分组为单位进行左移，移动(m-1)次。

然后根据日期数d，对每个分组内的字符进行循环左移，移动（n-1）次。

以3月8日为例，首先移动分组3-1=2次，变成：

STUVWXYZ*  ABCDEFGHI  JKLMNOPQR21

然后每组内字符移动8-1 = 7次,最终编码为：

Z*STUVWXY  HIABCDEFG  QRJKLMNOP

对于要传递的信息中的每个字符，用组号和组内序号两个数字来表示。

如果在3月8日传递信息 “HAPPY”，那么H位于第2组的第1个，A位于第二组 第3个 .....一次类推，纸条上会写成：

21，23，39，39，19

输入要求：

每个输入包含两行。第一行使用空格分隔的两个数字，第一个数字是月份，第二个数字是日期。输入保证是一个合法日期。

第二个行为需要编码的字符串，仅由A~Z和空格组成，长度不超过1024个字符

 

输出规范：

对每个输入，打印对应的编码，数字之间用空格分隔，每个输出占一行。

 

输入示例：

1 1

HI

输出示例：

18 19
