# jztkdb
call kdb+/q from JZT formulas

## jztkdb����

    ʵ��[������(JZT)���](http://www.weistock.com)��dll��ʽ�����Խ�jzt���ݴ���kdb���㲢���ؼ�����������ʵ�ָ��ӵļ��㡣

## ʹ�÷���

1�����ذ�װkdb+/q��

2���޸�qfml.q��ĺ�����

3����qfml.q���Ƶ�qĿ¼������q qfml.q -p 5001  �� ������û���֤����Ҫ���û������ļ�����qusers�ļ���������û����룺fml:input_fml_pwd��

4����c.dll���Ƶ�JZT��װĿ¼����d:\jzt��������fmlDLLĿ¼������   ע�⣺32λjzt������jzt32bit���c.dll��64λjzt����jzt64bit���c.dll��

5����jztkdb.dll���Ƶ�JZT�µ�FmlDLLĿ¼!!!�� ע�⣺32λjzt������jzt32bit���jztkdb.dll��64λjzt����jzt64bit���jztkdb.dll��

6����JZT�н���һ��ʽ������ģʽΪ����ģʽ���磺

mktid:=STRFIND('`XX`SH`SZ`ZJ`SQ`DQ`ZQ`WH`HZ`HK`CB`CM`AR`NM`NB`SG`KS`IP`LF`LS`DT`MO`SN`TQ`TJ`TW`ML`NE`XH`$$',MARKETLABEL(),1);

r:"jztkdb@CALC"(mktid,5000,1.2); {�ڶ�������Ϊ������qfml.q��kdb�Ķ˿ںţ�����������Ϊ.fml.f�����������ţ���ʾҪ����.fml.f[1.2]����}

