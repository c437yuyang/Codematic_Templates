DAL:

�ٵ�:deletelist()
datarowtomodel��ֻ��getmodel�����õ��ˣ�
��ͬ��:getmodel

������ӵ�:



BLL:
�ٵ�:getrecordcount,getlistbypage
������ӵ�:getlistbypage��getlistbypageorderbyid��id����primaykey��
��ͬ��:getmodellist(����ȥ��datarowtomodel)

deletebyfiled(field,value) (�������������Ҫ�ܶ����͵��жϣ�����int����where in 1,2,�ַ�������Ҫ��'')
���������������deletelistbyfiled() //������deletelist,�滻һ��ֵ����
deletelist���������������ֻ������field��id

updatelist���򵥵Ķ�update��װ��
addlist
getfieldlist(field,hasnullorempty)

�Ƚϱ�׼�ļ���:OrdersBll,deletelist��


С覴ã�
date�Ĵ���
add��ʱ��guid�Ĵ����Ѿ�ʵ��


//1.����Add��������Guid��ȫ��ʹ��new Guid()������string����������true or false
//2.���Ӷ�Guid����������Add����ֵ
//3.���Ӷ�Guid����������deletelist
//4.����datarowtomodel���棬stringû�зǿ��ж�(������Ϊnull��="")
//5.ʵ��GetListByPage()
//6.�����������ʵ��list������add,update,delete