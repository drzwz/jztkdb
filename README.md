# jztkdb
call kdb+/q from JZT formulas

## jztkdb功能

    实现[金字塔(JZT)软件](http://www.weistock.com)的dll公式，可以将jzt数据传到kdb计算并返回计算结果，可以实现复杂的计算。

## 使用方法

1、下载安装kdb+/q。

2、修改qfml.q里的函数。

3、把qfml.q提制到q目录。启动q qfml.q -p 5001  。 如果有用户验证，需要在用户密码文件（如qusers文件）中添加用户密码：fml:input_fml_pwd。

4、把c.dll复制到JZT安装目录（如d:\jzt），不是fmlDLL目录！！！   注意：32位jzt，复制jzt32bit里的c.dll，64位jzt复制jzt64bit里的c.dll。

5、把jztkdb.dll复制到JZT下的FmlDLL目录!!!。 注意：32位jzt，复制jzt32bit里的jztkdb.dll，64位jzt复制jzt64bit里的jztkdb.dll。

6、在JZT中建立一公式，运行模式为序列模式。如：

mktid:=STRFIND('`XX`SH`SZ`ZJ`SQ`DQ`ZQ`WH`HZ`HK`CB`CM`AR`NM`NB`SG`KS`IP`LF`LS`DT`MO`SN`TQ`TJ`TW`ML`NE`XH`$$',MARKETLABEL(),1);

r:"jztkdb@CALC"(mktid,5000,1.2); {第二个参数为加载了qfml.q的kdb的端口号，第三个参数为.fml.f函数的索引号，表示要调用.fml.f[1.2]函数}

