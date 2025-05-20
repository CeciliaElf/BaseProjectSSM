# SSM 通用后台管理系统 🚀

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Java](https://img.shields.io/badge/Java-8+-orange.svg)
![Spring](https://img.shields.io/badge/Spring-4.x-green.svg)
![MyBatis](https://img.shields.io/badge/MyBatis-3.x-red.svg)

一个基于 SSM(Spring+SpringMVC+MyBatis) 框架开发的通用后台管理系统，提供完整的权限管理、角色分配和系统监控功能。

## ✨ 功能特点

- 📊 **动态菜单** - 基于用户角色自动加载对应菜单
- 🔒 **权限控制** - 细粒度的功能权限控制
- 👥 **用户管理** - 支持用户的添加、修改、删除和查询
- 👑 **角色管理** - 角色的创建与权限分配
- 📝 **操作日志** - 记录用户关键操作，便于审计和追踪
- 🔢 **验证码** - 登录验证码，提高安全性
- 🖼️ **文件上传** - 支持头像等图片的上传功能

## 🛠️ 技术栈

### 后端
- **核心框架**: Spring 4.x
- **MVC 框架**: Spring MVC
- **ORM 框架**: MyBatis
- **数据库**: MySQL
- **项目构建**: Maven
- **日志**: Log4j
- **其他**: Jackson, Apache Commons, 等

### 前端
- **JS 框架**: jQuery
- **UI 库**: EasyUI
- **视图引擎**: JSP
- **其他**: HTML, CSS, JavaScript

## 📦 项目结构

```
BaseProjectSSM/
├── src/                          # 源代码目录
│   ├── com/cecilia/programmer/   # 主包
│   │   ├── controller/           # 控制器
│   │   ├── dao/                  # 数据访问层
│   │   ├── entity/               # 实体类
│   │   ├── interceptor/          # 拦截器
│   │   ├── service/              # 服务层
│   │   └── util/                 # 工具类
│   └── config/                   # 配置文件
├── WebContent/                   # Web内容
│   ├── WEB-INF/
│   │   ├── views/                # JSP视图
│   │   └── web.xml               # Web配置
│   └── resources/                # 静态资源
│       ├── admin/                # 管理后台资源
│       └── upload/               # 上传文件目录
└── pom.xml                       # Maven配置
```

## 🚀 快速开始

### 环境要求
- JDK 1.8+
- Maven 3.0+
- MySQL 5.7+
- Tomcat 8.5+

### 数据库配置
1. 创建数据库`baseprojectssm`
2. 导入 SQL 脚本 (`doc/baseprojectssm.sql`)

### 修改配置
1. 编辑`src/config/db.properties`文件，设置数据库连接参数

```properties
jdbc.driver=com.mysql.cj.jdbc.Driver
jdbc.url=jdbc:mysql://localhost:3306/baseprojectssm?useUnicode=true&characterEncoding=utf8&serverTimezone=GMT%2B8
jdbc.username=root
jdbc.password=你的密码
```

### 部署运行
1. 使用 Maven 编译项目
```bash
mvn clean package
```

2. 将生成的 WAR 包部署到 Tomcat

3. 访问 `http://localhost:8080/BaseProjectSSM`

4. 默认管理员账号
```
用户名: admin
密码: admin
```

## 📸 系统截图

![登录页面](docs/images/login.png)
![系统首页](docs/images/dashboard.png)
![用户管理](docs/images/user-management.png)

## 📄 许可证

[MIT](LICENSE) © Cecilia

## 📊 系统功能模块

### 系统管理
- 用户管理
- 角色管理
- 菜单管理
- 日志管理

### 个人信息
- 修改密码
- 个人资料

## 🔗 相关链接
- [详细开发文档](开发教程文档.md)
- [Spring 官方文档](https://spring.io/projects/spring-framework)
- [MyBatis 官方文档](https://mybatis.org/mybatis-3/)

## ❓ 常见问题

**Q: 如何修改日志存储位置？**
A: 编辑`src/config/log4j.properties`，修改`log4j.appender.file.File`属性。

**Q: 如何扩展新的功能模块？**
A: 添加新的实体类、DAO、Service 和 Controller，然后在菜单管理中添加对应的菜单项。