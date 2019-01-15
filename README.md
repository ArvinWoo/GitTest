[DataTables官方网站](https://datatables.net)

--------

### 基本的使用：

- 1、DataTables的默认配置：
```
$(document).ready(function(){
	 $('#example').dataTable();
});//初始化DataTables
```

示例：http://www.guoxk.com/html/DataTables/Zero-configuration.html

	得到：Printer

**类型**

- 串：
   ‘.’点缀JavaScript对象符号：
   		如果字符串中包含‘.’可以使用\\来转义它，
   []数组表示法：
   		使用name[,]将原数组中提供一个以逗号分隔的列表。将数据与两个括号之间提供的字符结合起来。否则返回原始数组源。
   ()功能符号：

- 整数：作为数据源数组索引处理。默认是逐列递增

#### **function render(data,type,row,meta)该方法返回时用来请求的数据。**
如果给出这个方法，只要调用该数据。此方法都会执行。

- data(单元格的数据,基于columns.data)，
- type(请求的类型调用数据，用于render正交数据支持)String类型的。
	- filter:获取datatable应用于在此单元格进行过滤的值。
	- display:在表格中显示的值。
	- type:用于类型检测的值。通常匹配sort值。
	- sort:获取在此单元格上进行排序的数据。
	- undefined:获取单元格原始数据。
- row(该行的完整数据源)
- meta(包含有关请求的单元格附加信息对象)该对象包含一下属性：
	- row:请求的单元格的行索引
	- col:请求的单元格的列索引
	- settings:DataTables.Settings有问题的表的对象。如果需要，这可以用来获得一个API实例。

####  **columnDefs**
所有列默认值为null（_all所有列的意思，[0,1]第一列和第二列）

#### **lengthMenu**
更改列表的长度。默认[10，25，50，100]

#### **dom**
定义表格控件元素，使其在页面上以什么顺序出现。
内置选项：
表格内置控制元素在DataTables是有如下：

```
"dom" : 'rt<"floatl mt5"l><"floatl mt5"i><"floatr mt5"p><"clear">'
//定义表格控件元素，使其在页面上以什么顺序出现。
```

- l - 变长输入控制[一页展示多少数据]
- f - 过滤输入[搜索栏过滤输入]
- t - 这个表格
- i - 表格信息摘要[共有多少页第多少页]
- p - 分页控制[第几页选择]
- r - 处理显示单元
 
