DAL:

少的:deletelist()
datarowtomodel（只有getmodel里面用到了）
不同的:getmodel

可以添加的:



BLL:
少的:getrecordcount,getlistbypage
可以添加的:getlistbypage，getlistbypageorderbyid（id就是primaykey）
不同的:getmodellist(可以去用datarowtomodel)

deletebyfiled(field,value) (但是这个函数需要很多类型的判断，比如int就是where in 1,2,字符串类型要加'')
这个做公共函数，deletelistbyfiled() //类似于deletelist,替换一个值而已
deletelist来调用这个函数，只是这里field是id

updatelist（简单的对update封装）
addlist
getfieldlist(field,hasnullorempty)

比较标准的几个:OrdersBll,deletelist的


小瑕疵：
date的处理
add的时候，guid的处理，已经实现


//1.修正Add方法对于Guid列全部使用new Guid()，对于string的主键返回true or false
//2.增加对Guid类型主键的Add返回值
//3.增加对Guid类型主键的deletelist
//4.修正datarowtomodel里面，string没有非空判断(插入若为null会="")
//5.实现GetListByPage()
//6.针对整形主键实现list操作，add,update,delete