目前只思考了整体的结构, 代码后续完善中.

加载过程:

入口文件 -> 注册自加载函数 -> 注册异常处理函数 -> 加载配置文件 -> 请求
-> 路由 -> 经控制器处理数据模型后 -> 响应 -> 返回json或其他格式 -> 渲染view

目录结构

  


```
simpleFrame                     [项目目录]
├── Public                      [公共文件]
│   ├── App.php                 [框架类]
│   ├── Container.php           [服务容器]
│   └── Route.php               [路由类]
├── Helper                      [工具类]
│   └── Load.php                [自加载类]
├── Model                       [实体类]
│   ├── Exception.php      	  [异常实体类]
│   ├── Log.php                 [日志实体类]
│   ├── Request.php             [请求实体类]
│   ├── Response.php            [响应实体类]
│   └── Database                [数据库实体类目录]
│       ├── DB.php          	  [数据库实体基类]
│       ├── Redis.php       	  [Redis实体类]
│       └── Mysql.php           [mysql实体类]
├── Handlers                    [框架运行时挂载处理机制类目录]
│   ├── ExceptionHadler.php     [异常处理类]
│   ├── LogHadler.php           [日志处理类]
│   ├── RequestHadler.php       [请求处理类]
│   ├── ResponseHadler.php      [响应处理类]
│   └── DBHadler.php        	  [数据库处理类]


```
