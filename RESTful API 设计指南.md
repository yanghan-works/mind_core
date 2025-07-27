---
tags: 
aliases: 
created: 2025-07-27 18:27
---

> 这是一份旨在提供清晰、一致且易于使用的 RESTful API 设计规范。良好的 API 设计如同清晰的路标，能让开发者轻松理解并正确使用。



## 1. 核心原则

API 的设计应遵循以下几个核心原则，它们是构建高质量 API 的基石：

- **无状态 (Stateless)**：服务器不应存储任何关于客户端请求的上下文信息。每一次请求都应包含所有必要信息。
    
- **客户端-服务器 (Client-Server)**：客户端和服务器的角色应明确分离，它们之间通过请求-响应模式进行交互。
    
- **统一接口 (Uniform Interface)**：使用统一的、预定义的接口来简化和解耦架构，这是 REST 设计的核心。
    

## 2. URI 设计：用名词而非动词

URI（统一资源标识符）是 API 的入口。设计 URI 时，应始终使用名词来表示资源集合。

### 2.1 资源命名

使用复数名词来表示资源集合，这是一种广泛接受的最佳实践。

|   |   |   |
|---|---|---|
|**✅ 推荐 (Good)**|**❌ 不推荐 (Bad)**|**说明**|
|`/users`|`/getAllUsers`|获取所有用户|
|`/users/123`|`/getUserById?id=123`|获取特定 ID 的用户|
|`/users/123/articles`|`/getUserArticles?uid=123`|获取某用户的文章列表|

### 2.2版本控制

将 API 版本号放入 URI 中，是一种明确且直接的做法。

```
https://api.example.com/v1/users
https://api.example.com/v2/users
```

## 3. HTTP 方法：操作资源的动词

使用标准的 HTTP 方法来对资源执行操作 (CRUD: Create, Read, Update, Delete)。

- **`GET`**：**读取**资源。
    
    - `GET /users`：获取用户列表。
        
    - `GET /users/123`：获取 ID 为 123 的用户。
        
- **`POST`**：**创建**新资源。
    
    - `POST /users`：创建一个新用户。
        
- **`PUT`**：**更新**或**替换**一个现有资源。
    
    - `PUT /users/123`：完整更新 ID 为 123 的用户信息。
        
- **`DELETE`**：**删除**一个资源。
    
    - `DELETE /users/123`：删除 ID 为 123 的用户。
        

## 4. 状态码：明确的响应反馈

使用标准的 HTTP 状态码来表示请求的结果。

> **重要提示**：永远不要自定义状态码。使用标准代码能让所有 HTTP 客户端都能理解你的 API 响应。

- **2xx 成功**
    
    - `200 OK`：请求成功。
        
    - `201 Created`：资源创建成功。
        
- **4xx 客户端错误**
    
    - `400 Bad Request`：请求无效（例如，参数错误）。
        
    - `404 Not Found`：请求的资源不存在。
        
- **5xx 服务器错误**
    
    - `500 Internal Server Error`：服务器内部发生错误。
        

## 5. 一个完整的例子

下面是一个获取特定用户信息的完整请求与响应示例。

### 请求 (Request)

```
GET /v1/users/123 HTTP/1.1
Host: api.example.com
Accept: application/json
```

### 响应 (Response)

```
HTTP/1.1 200 OK
Content-Type: application/json

{
  "id": 123,
  "username": "coder_xiaoming",
  "email": "xiaoming@example.com",
  "createdAt": "2023-10-27T10:00:00Z"
}
```

_文档最后更新于：2025-07-27_