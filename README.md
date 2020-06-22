# parametricmodel
参数化建模 pythonOcc cadquery CAD 

# 简介
项目提供录值页面,三维制图人员通过录入模型参数,提交到后端服务器进行预设模型赋值并生成新的模型,页面重新渲染出新生成的模型。

# 运用到的技术板块
1. docker
2. pythonOcc
3. [cadQuery](https://hub.docker.com/r/cadquery/cadquery)
4. [django](https://www.djangoproject.com)
5. [bootstrap](https://github.com/twbs/bootstrap)
6. [three.js](https://github.com/mrdoob/three.js)
7. [vue.js](https://github.com/vuejs/vue)

# 项目运行环境搭建
1. 拉取项目运行需要的环境镜像

`docker pull cadquery/cadquery`

2. 根据镜像创建并运行项目环境,-v中的djangoLocalPath为django项目实际计算机中的绝对路径

`docker run -it -v djangoLocalPath:/cadquery/djangoProject --name=cadquery -p:8888 bash`

3. 安装python软件包管理工具pip

`curl https://bootstrap.pypa.io/get-pip.py -o get-pip.py`
`python get-pip.py`

4. 切换到docker容器中的django项目目录下

`cd /cadquery/djangoProject`

5. 启动服务(会出现缺少模块的提示,请使用 `pip install xx` 安装相应模块)

`python manage.py runserver 0.0.0.0:8888`


