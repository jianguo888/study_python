https://zhuanlan.zhihu.com/p/24180606

smtplib

email

17752170152

授权码

YEOHQCXIDWYXRUVV



demo

```python
#!/usr/bin/env python3.9.2
# -*- coding: utf-8 -*-
# @Time    :  2021-03-02 8:40
# @Author  : Luckly
# @FileName: email.py.py
# @Software: PyCharm
# @Blog    ：https://blog.csdn.net/qq_39132095
import smtplib
from email.mime.text import MIMEText
#设置服务器所需信息
#163邮箱服务器地址
mail_host = 'smtp.163.com'
#163用户名
mail_user = '17752170152'
#密码(部分邮箱为授权码)
mail_pass = 'YEOHQCXIDWYXRUVV'
#邮件发送方邮箱地址
sender = '17752170152@163.com'
#邮件接受方邮箱地址，注意需要[]包裹，这意味着你可以写多个邮件地址群发
receivers = ['852851198@qq.com']

#设置email信息
#邮件内容设置
message = MIMEText('content','plain','utf-8')
#邮件主题
message['Subject'] = 'title'
#发送方信息
message['From'] = sender
#接受方信息
message['To'] = receivers[0]

#登录并发送邮件
try:
    smtpObj = smtplib.SMTP()
    #连接到服务器
    smtpObj.connect(mail_host,25)
    #登录到服务器
    smtpObj.login(mail_user,mail_pass)
    #发送
    smtpObj.sendmail(
        sender,receivers,message.as_string())
    #退出
    smtpObj.quit()
    print('success')
except smtplib.SMTPException as e:
    print('error',e) #打印错误
```







参考https://www.runoob.com/python/python-email.html

![image-20210302215206642](https://luckly007.oss-cn-beijing.aliyuncs.com/image-20210302215206642.png)



![image-20210302215443738](https://luckly007.oss-cn-beijing.aliyuncs.com/image-20210302215443738.png)

发送带格式邮件

![image-20210302215752809](https://luckly007.oss-cn-beijing.aliyuncs.com/image-20210302215752809.png)

![image-20210302215845072](https://luckly007.oss-cn-beijing.aliyuncs.com/image-20210302215845072.png)

![image-20210302220811647](https://luckly007.oss-cn-beijing.aliyuncs.com/image-20210302220811647.png)



```python
#!/usr/bin/env python3.9.2
# -*- coding: utf-8 -*-
# @Time    :  2021-03-02 22:09
# @Author  : Luckly
# @FileName: weixinglocal.py.py
# @Software: PyCharm
# @Blog    ：https://blog.csdn.net/qq_39132095
from wxpy import *

bot =Bot()

my_frirnds=bot.friends(update=False)
print(my_frirnds.stats_text())

```



![image-20210302221334387](https://luckly007.oss-cn-beijing.aliyuncs.com/image-20210302221334387.png)

![image-20210302221424158](https://luckly007.oss-cn-beijing.aliyuncs.com/image-20210302221424158.png)

钉钉机器人

![image-20210302222328275](https://luckly007.oss-cn-beijing.aliyuncs.com/image-20210302222328275.png)

is_at_all=true

![image-20210302222439853](https://luckly007.oss-cn-beijing.aliyuncs.com/image-20210302222439853.png)

![image-20210302224451386](https://luckly007.oss-cn-beijing.aliyuncs.com/image-20210302224451386.png)

![image-20210302224641339](https://luckly007.oss-cn-beijing.aliyuncs.com/image-20210302224641339.png)

![image-20210302225003226](https://luckly007.oss-cn-beijing.aliyuncs.com/image-20210302225003226.png)

打开上班工具

![image-20210302225432364](https://luckly007.oss-cn-beijing.aliyuncs.com/image-20210302225432364.png)

![image-20210302225602425](https://luckly007.oss-cn-beijing.aliyuncs.com/image-20210302225602425.png)