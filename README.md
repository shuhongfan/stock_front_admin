## 1.目录结构
目录  
```  
   │──dist            
   │──src             
   │  │──api             接口请求目录  
   │  │──assets          静态资源目录
   │  │──common          公共目录(如：公共函数,可直接修改，不影响打包后的文件)    
   │  │──components      组件目录  
   │  │──config          配置目录  
   │  │──lib             核心库目录  
   │  │──router          路由目录  
   │  │──store           vuex目录  
   │  │──views           视图目录  
   │  │──App.vue         根组件  
   │  │──index.html      模板文件    
   │  │──main.js         入口文件                  
   │  └──settings.js     配置文件
   │    ...
```
   
## 2.Build
```
# install dependency
npm install

# test development dev
npm run dev

# build
npm run build

# build test
npm run build:test

# watch
npm run watch
```
## 3.用户登录响应数据
权限结构数据：
~~~
{
    "code": 1,
    "data": {
        "id": "1237361915165020161",
        "username": "admin",
        "phone": "13888888888",
        "nickName": "itheima",
        "realName": "heima",
        "sex": 1,
        "deptId": "1237322421447561216",
        "deptName": "测试添加部门",
        "status": 1,
        "email": "875267425@qq.com",
        "menus": [
            {
                "id": "1236916745927790564",
                "title": "组织管理",
                "icon": "el-icon-star-off",
                "path": "/org",
                "name": "org",
                "children": [
                    {
                        "id": "1236916745927790578",
                        "title": "角色管理",
                        "icon": "el-icon-s-promotion",
                        "path": "/roles",
                        "name": "roles",
                        "children": []
                    },
                    {
                        "id": "1236916745927790560",
                        "title": "菜单权限管理",
                        "icon": "el-icon-s-tools",
                        "path": "/menus",
                        "name": "menus",
                        "children": []
                    },
                    {
                        "id": "1236916745927790575",
                        "title": "用户管理",
                        "icon": "el-icon-s-custom",
                        "path": "/users",
                        "name": "user",
                        "children": []
                    },
                    {
                        "id": "1236916745927790573",
                        "title": "部门管理",
                        "icon": "el-icon-s-tools",
                        "path": "/depts",
                        "name": "depts",
                        "children": []
                    }
                ],
                "spread": true,
                "checked": false
            },
            {
                "id": "1236916745927790569",
                "title": "系统管理",
                "icon": "el-icon-s-tools",
                "path": "/sys",
                "name": "auth",
                "children": [
                    {
                        "id": "1236916745927790589",
                        "title": "日志管理",
                        "icon": "el-icon-s-flag",
                        "path": "/logs",
                        "name": "logs",
                        "children": []
                    },
                    {
                        "id": "1236916745927790558",
                        "title": "接口管理",
                        "icon": "el-icon-s-tools",
                        "path": "/swagger",
                        "name": "swagger",
                        "children": []
                    },
                    {
                        "id": "1236916745927790571",
                        "title": "SQL监控",
                        "icon": "el-icon-s-tools",
                        "path": "/sql",
                        "name": "sql",
                        "children": []
                    }
                ]
            },
            {
                "id": "1236916745927790569",
                "title": "账号管理",
                "icon": "el-icon-s-data",
                "path": "/user",
                "name": "user",
                "children": []
            }
        ],
        "permissions": [
            "sys:log:delete",
            "sys:user:add",
            "sys:role:update",
            "sys:dept:list"
        ]
    }
}
~~~

常见打包错误：
运行 npm run build,报错：
Module build failed (from ./node_modules/image-webpack-loader/index.js)
解决方案：
~~~js
先卸载
npm uninstall image-webpack-loader
然后使用
cnpm install image-webpack-loader --save-dev
~~~
