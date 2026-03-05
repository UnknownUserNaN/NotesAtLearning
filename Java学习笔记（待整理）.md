1. Java中仍然沿用了C中的强制类型转换语法，但是也有“拆箱”和“装箱”的方法来实现更加安全的类型转换。“装箱”和“拆箱”主要是实现对基本数据类型（int、char、bool等）的面向对象的操作（如int转Integer，char转Character），JDK1.5后实现了自动的“装箱”和“拆箱”。此外，每个包装类型都有相应的parse方法（如Integer的parseInt方法），用于实现类型转换。
2. 四舍五入使用Math中的round函数。Math包中含有许多数学函数。
3. Java的封装数据类型Integer，会预先创建-128~128（包含端点）的Integer对象。因此，对-128~128内的int值“装箱”时会直接返回预先创建好的Integer对象，超出该范围后才会返回一个新创建的对象。
4. Java中的“\=\=”运算符，对于类对象，只会比较等号两侧的对象是否为同一个地址（即是否是同一个对象）。如果要检查两个类对象的值是否相等，则要调用该类对象的equals之类的方法。比如对于String，则要调用其equals方法。
5. Java的输入检查器Scanner类（隶属于java.util.Scanner），在初始化时为其传入一个流（通常是System.in），然后使用next系方法（如nextInt，nextDouble）来获取流中的数据。不过，当数据流中已经没有数据时，使用next方法会报错，因此在取数据之前，要使用hasNext方法来检查流中是否有数据。
6. Java的String类的matches方法可以检查当前字符串是否满足正则表达式字符串的格式规定，返回结果是一个布尔值。
7. Java的String类的format方法可以通过指定格式字符串的方式，将各类数值转换成对应的字符串（支持前导零、小数位数等设计）。
8. Java的类定义中，要修改其类成员时，要显式地写出this指针。这一点与Python中的设计相同。
9. Java中，使用extends关键字声明父类，使用implements关键字声明接口。子类的构造方法中，可以使用super关键字来调用父类的构造方法（super()）和其他成员方法（super.xxx()）。
10. Java中，默认将所有不显式写出父类的类视为Object的子类。因此，如果想让某个函数接受一个较为“广泛”的参数类型，可以将它的类型改为Object。
11. Java中，使用instanceof运算符进行类型检查，其运算结果为bool型。
12. Java中，默认每个实例化对象都可以通过getClass方法访问到它的类，默认每个类都可以通过getClass和getSimpleName方法调用到该类的“名字”字符串。
13. Java中的抽象方法使用abstract显式声明，要求其子类必须实现该方法。子类进行实现时需要通过重写（override）的方法完成，并推荐在前面加上“@Override”的注解。
14. Java中防止一个方法被子类重写时，需要使用final关键字修饰。
15. Java中的String对象不可以修改。要实现动态的修改，需要使用StringBuilder类对象，使用其append、insert等方法，然后使用toString方法转出对象。
16. 