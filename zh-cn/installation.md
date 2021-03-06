# 安装

> 介绍如何安装 PJ 博客

### 下载项目

你可以在命令行通过 `composer` 的命令 `create-project` 进行安装：

```shell
composer create-project jcc/blog
```


或者，你也可以通过 `git clone` 命令将代码从 `Github` 上拉取下来：

```shell
git clone git@github.com:jcc/blog.git
```

### 安装依赖包

#### 安装 `Laravel` 的依赖

You need to install the Laravel repositories:

```shell
composer install --no-dev
```

#### 安装前端依赖

###### 安装 `Gulp`

```shell
npm install --global gulp
```

或者你可以使用 `yarn` 代替 `npm` 节省下载安装时间：

```shell
yarn add global gulp
```

###### 安装 `Laravel Elixir` 和 `Vuejs` 的依赖:

```shell
npm install
```

或者

```shell
yarn
```

###### 编译

你可以单次编译：

```shell
gulp
```

或者你可以监控资源文件修改：

```shell
gulp watch
```

当然，你也可以运行所有任务并压缩所有 CSS 及 JavaScript：

```shell
gulp --production
```

### 修改配置

复制一份 `.env.example` 到 `.env`：

```shell
cp .env.example .env
```

配置好 `.env` 文件后，你可以运行 `blog:install` 命令进行数据库的*表迁移*以及*生成数据*：

```shell
php artisan blog:install
```
