## manage.py 使用

使用manage.py需要在其所在的目录下面运行。

- 运行Django：`py manage.py runserver`

- 用指定端口运行：`py manage.py runserver 8080`

> 启动服务器后，修改代码会自动重启服务

- 创建应用：`py manage.py startapp {app_name}` 会自动创建文件夹和相关的文件

- 创建模型：`py manage.py makemigrations {app_name}` 需要在`INSTALLED_APPS`中注册应用模型

- 将数据模型自动迁移到数据库：`py manage.py migrate` 会为在`INSTALLED_APPS`中声明了的应用进行数据库迁移，所以不要忘记创建模型后在`INSTALLED_APPS`中声明。

### 更新模型5部曲

1. 创建应用

2. 将应用添加到`INSTALLED_APPS`

3. 修改模型

4. `py manage.py makemigrations {app_name}`

5. `py manage.py migrate`