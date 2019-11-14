# 简单博客网页API设计

模拟设计网页地址：https://myBlogDesigned.com

### 1. 用户注册

#### 1.1 用户注册页面获取

```
URL：https://myBlogDesigned.com/signin
Method：GET
body：
{}
```

#### 1.2 用户注册操作

```
URL：https://myBlogDesigned.com/signin
Method：POST
body：
{
	"username": 用户名,
	"password": 用户密码,
	"time": 当前时间，
	"email":邮箱账户，
}
```

### 2. 用户认证

#### 2.1 用户认证页面获取

```
URL：https://myBlogDesigned.com/login
Method：GET
body：
{}
```

#### 2.2 用户认证界面操作

````
URL：https://myBlogDesigned.com/login
Method：POSt
body：
{
	"username":用户名,
	"password":用户密码,
}
````

#### 2.3 用户微信账号相关关联

```
URL：https://myBlogDesigned.com/login-wechat
Method：POST
body：
{
	"icon":头像,
	"wechatID":微信ID,
	"wechatPassword":微信密码，
}
```

### 3. 博客操作

#### 3.1 博客创建

```
URL：https://myBlogDesigned.com/blog/{username}/create
Method：POST
body：
{
	"BlogName":博客名,
	"Tag":博客标签，
	"BlogStat":共享权限，
}
```

#### 3.2 博客编写

```
URL：https://myBlogDesigned.com/blog/editor
Method：POST
body：
{
	"Content":博客内容，
}
```

#### 3.3 博客发布

```
URL：https://myBlogDesigned.com/blog/{username}/push
Method：POST
body：
{
	"blogID":博客ID，
	“shareStat":博客分享状态
}
```

### 4. 博客交互

#### 4.1 阅读他人博客

```
URL：https://myBlogDesigned.com/{username}/articles/{blogID}
Method：GET
body：
{}
```

#### 4.2 博客评论

```
URL：https://myBlogDesigned.com/{username}/articles/{blogID}/comment
Method：POST
body：
{
	"content":评论内容
}
```



