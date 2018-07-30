# python
#### python学习

[urllib.request发送请求一](https://blog.csdn.net/bo_mask/article/details/76067790)

[python requets模块详细用法一](https://www.jianshu.com/p/201b94e6e2a1)

[python爬虫之requests库的详解二](https://blog.csdn.net/sunshunli/article/details/79965891)

[requests快速上手](http://docs.python-requests.org/zh_CN/latest/user/quickstart.html#id10)

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
