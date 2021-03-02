1、xlsxwriter模块的简单使用：

   xlsxwriter模块主要用来生成excel表格，插入数据、插入图标等表格操作。

   1.1 基本功能

```python
import xlsxwriter  # 导入模块

workbook = xlsxwriter.Workbook('new_excel.xlsx')  # 新建excel表

worksheet = workbook.add_worksheet('sheet1')  # 新建sheet（sheet的名称为"sheet1"）

headings = ['Number', 'testA', 'testB']  # 设置表头

data = [
    ['2017-9-1', '2017-9-2', '2017-9-3', '2017-9-4', '2017-9-5', '2017-9-6'],
    [10, 40, 50, 20, 10, 50],
    [30, 60, 70, 50, 40, 30],
]  # 自己造的数据

worksheet.write_row('A1', headings)

worksheet.write_column('A2', data[0])
worksheet.write_column('B2', data[1])
worksheet.write_column('C2', data[2])  # 将数据插入到表格中

workbook.close()  # 将excel文件保存关闭，如果没有这一行运行代码会报错查看生成excel的结果：
```

　　查看生成excel的结果：

​    ![img](https://images2018.cnblogs.com/blog/1215888/201803/1215888-20180329163220700-1012976018.png)

  1.2 将excel中插入折线图   



```python
import xlsxwriter                     #导入模块

workbook = xlsxwriter.Workbook('new_excel.xlsx')   #创建新的excel

worksheet = workbook.add_worksheet('sheet1')        #创建新的sheet

headings = ['Number','testA','testB']             #创建表头

data = [
    ['2017-9-1','2017-9-2','2017-9-3','2017-9-4','2017-9-5','2017-9-6'],
    [10,40,50,20,10,50],
    [30,60,70,50,40,30],
]                                                       #自己造的数据

worksheet.write_row('A1',headings)

worksheet.write_column('A2',data[0])
worksheet.write_column('B2',data[1])
worksheet.write_column('C2',data[2])                    #将数据插入到表格中

chart_col = workbook.add_chart({'type':'line'})        #新建图表格式 line为折线图
chart_col.add_series(                                   #给图表设置格式，填充内容
    {
        'name':'=sheet1!$B$1',
        'categories':'=sheet1!$A$2:$A$7',
        'values':   '=sheet1!$B$2:$B$7',
        'line': {'color': 'red'},
    }
)

chart_col.set_title({'name':'测试'})
chart_col.set_x_axis({'name':"x轴"})
chart_col.set_y_axis({'name':'y轴'})          #设置图表表头及坐标轴

chart_col.set_style(1)

worksheet.insert_chart('A10',chart_col,{'x_offset':25,'y_offset':10})   #放置图表位置

workbook.close()
```



  生成图表如下图

  ![img](https://images2018.cnblogs.com/blog/1215888/201803/1215888-20180329171447835-35825186.png)

 2、xlsxwriter模块常用功能介绍：

 2.1、设置单元格的格式：

 2.1.1、通过字典的方式直接设置格式。     



```python
workfomat = workbook.add_format({
    'bold':  True,                 #字体加粗
    'border':1,                    #单元格边框宽度
    'align':    'center',          #对齐方式
    'valign':   'vcenter',         #字体对齐方式
    'fg_color': '#F4B084',         #单元格背景颜色
})
```



2.1.2、通过format对象的方式设置单元格格式。

```python
 workfomat = workbook.add_format()
workfomat.set_bold(1)                #设置边框宽度
 workfomat.set_num_format('0.00')     #格式化数据格式为小数点后两位
 workfomat.set_align('center')        #设置对齐方式
 workfomat.set_fg_color('blue')       #设置单元格背景颜色
 workfomat.set_bg_color('red')        #设置单元格背景颜色 (经测试和上边的功能一样)
```

2.1.3、一些单元表的操作，像这样的操作还有好多，可以根据自己的需要去进行研究。

```python
worksheet.merge_range('D1:D7','合并单元格')        #合并单元格
 worksheet.set_tab_color('red')                      #设置sheet标签颜色
worksheet.set_column('A:D',25)                      #设置A到D列的列宽为25
worksheet.write_formula('E2','=B2/C2')             #设置表格中的计算，‘E2’是计算结果，'=B2/C2'是计算公式
```

2.2、常用图表类型：



```python
#area：面积图
#bar：直方图
#colume：柱状图
#line：折线图
#pie：饼图
#doughnut：环形图
#sactter：散点图
#stock：股票趋势图
#radar：雷达图
```

19

20

2