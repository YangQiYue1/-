# Mybatis-Plus

## 一、简介及特性

- 简介

  > Mybatis-Plus是一个Mybatis的增强工具，在Mybatis的基础上只做增强不做改变，为简化开发、提高效率而生。Mybatis-Plus提供了通用的mapper和service，可以在不编写任何SQL语句的情况下，快速实现对单表的CRUD、批量、逻辑删除、分页等操作。

- 特性
  - **无侵入**：只做增强不做改变，引入它不会对现有工程产生影响，如丝般顺滑
  - **损耗小**：启动即会自动注入基本 CURD，性能基本无损耗，直接面向对象操作
  - **强大的 CRUD 操作**：内置通用 Mapper、通用 Service，仅仅通过少量配置即可实现单表大部分 CRUD 操作，更有强大的条件构造器，满足各类使用需求
  - **支持 Lambda 形式调用**：通过 Lambda 表达式，方便的编写各类查询条件，无需再担心字段写错
  - **支持主键自动生成**：支持多达 4 种主键策略（内含分布式唯一 ID 生成器 - Sequence），可自由配置，完美解决主键问题
  - **支持 ActiveRecord 模式**：支持 ActiveRecord 形式调用，实体类只需继承 Model 类即可进行强大的 CRUD 操作
  - **支持自定义全局通用操作**：支持全局通用方法注入（ Write once, use anywhere ）
  - **内置代码生成器**：采用代码或者 Maven 插件可快速生成 Mapper 、 Model 、 Service 、 Controller 层代码，支持模板引擎，更有超多自定义配置等您来使用
  - **内置分页插件**：基于 MyBatis 物理分页，开发者无需关心具体操作，配置好插件之后，写分页等同于普通 List 查询
  - **分页插件支持多种数据库**：支持 MySQL、MariaDB、Oracle、DB2、H2、HSQL、SQLite、Postgre、SQLServer 等多种数据库
  - **内置性能分析插件**：可输出 SQL 语句以及其执行时间，建议开发测试时启用该功能，能快速揪出慢查询
  - **内置全局拦截插件**：提供全表 delete 、 update 操作智能分析阻断，也可自定义拦截规则，预防误操作

## 二、入门案例

- **创建表**

  ```sql
  CREATE TABLE `user` (
    `id` bigint(20) NOT NULL COMMENT '主键ID',
    `name` varchar(30) COLLATE utf8mb4_bin DEFAULT NULL COMMENT '姓名',
    `age` int(11) DEFAULT NULL COMMENT '年龄',
    `email` varchar(50) COLLATE utf8mb4_bin DEFAULT NULL COMMENT '邮箱',
    PRIMARY KEY (`id`)
  ) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_bin;
  ```

- **新增数据**

  ```sql
  	insert into user(id,name,age,email) values
  		(1,'Jone',18,'test1@baomidou.com'),
  		(2,'Jack',20,'test2@baomidou.com'),
  		(3,'Tom',28,'test3@baomidou.com'),
  		(4,'Sandy',21,'test4@baomidou.com'),
  		(5,'Billie',24,'test5@baomidou.com');
  ```

- **创建SpringBoot工程**

  - 初始化工程

    > 使用SpringBoot初始化器创建工程

  - 引入相关依赖

    ```xml
    <!--mybatis-plus启动器-->
    <dependency>
        <groupId>com.baomidou</groupId>
        <artifactId>mybatis-plus-boot-starter</artifactId>
        <version>3.5.1</version>
    </dependency>
    <!--简化实体类开发-->
    <dependency>
        <groupId>org.projectlombok</groupId>
        <artifactId>lombok</artifactId>
        <optional>true</optional>
    </dependency>
    <!--mysql驱动-->
    <dependency>
        <groupId>mysql</groupId>
        <artifactId>mysql-connector-java</artifactId>
        <scope>runtime</scope>
    </dependency>
    ```

  -  配置数据源

    ```yaml
    spring:
      datasource:
        type: com.zaxxer.hikari.HikariDataSource
        driver-class-name: com.mysql.cj.jdbc.Driver
        url: jdbc:mysql://bj-cdb-k9ar05pc.sql.tencentcdb.com:60083/mybatis_plus?useUnicode=true&characterEncoding=UTF8
        username: root
        password: Y5897257!
    ```

    

  - 





























## 二、基本功能

### 2.1 通用mapper

### 2.2 通用service

### 2.3 常用注解

### 2.4 条件构造器

### 2.5 通用枚举

## 三、插件

### 3.1 分页插件

### 3.2 乐观锁

## 四、代码生成器

## 五、多数据源

## 六、MybatisX插件

