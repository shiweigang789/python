# python
#### python学习

[urllib.request发送请求一](https://blog.csdn.net/bo_mask/article/details/76067790)

[python requets模块详细用法一](https://www.jianshu.com/p/201b94e6e2a1)

[python爬虫之requests库的详解二](https://blog.csdn.net/sunshunli/article/details/79965891)

[requests快速上手](http://docs.python-requests.org/zh_CN/latest/user/quickstart.html#id10)

[Python 3基础语法知识点](https://mp.weixin.qq.com/s?__biz=MzIxODM4MjA5MA==&mid=2247487975&idx=1&sn=a4e4fb98178d94d8fed77f41890b6061&chksm=97ea3b82a09db294b2107bf1be3a914e461de694cc2c5f142524c15458534e8074439cb26568&mpshare=1&scene=23&srcid=1219eqzRgdeBNtOKc8Vm1gAi#rd)

##### python django链接mysql数据库 配置
    
    DATABASES = {
        'default': {
            'ENGINE': 'django.db.backends.mysql',
            'NAME': 'django_db1',
            'USER': 'root',
            'PASSWORD':'123456',
            'HOST': '127.0.0.1',
            'PORT': '3306',
        }
    }
    
    
    from django.db import connection
    
    cursor = connection.cursor()
    cursor.execute("insert into book(id, name, author) value (null, '三国演义', '罗贯中')")
    cursor.execute("select * from book")
    rows = cursor.fetchall()

##### manage操作
    创建App
    python manage.py startapp name
    创建数据映射
    python manage.py makemigrations
    Python manage.py migrate
