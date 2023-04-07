# API

`POST` /app/sendCode 发送验证码

### 请求参数

| 参数名   | 必填 | 类型     | 描述  |
|-------|----|--------|-----|
| phone | 是  | String | 手机号 |

### 示例

``` json
{
    "phone": "13666666666",
}
```

### 成功响应

``` json
{
    "code": 0,
    "data": "014906"
}
```

---

`POST` /app/user/loginAndRegister 登录注册

### 请求参数

| 参数名         | 必填 | 类型     | 描述    |
|-------------|----|--------|-------|
| phone       | 是  | String | 手机号   |
| tag         | 是  | String | 验证码标识 |
| code        | 是  | String | 验证码   |
| recommendId | 否  | String | 推荐码   |

### 示例

``` json
{
    "phone": "13666666666",
    "tag":"014906",
    "code":"938239",
    "recommend_id":" ",
}
```

### 成功响应

``` json
{
    "code": 0,
    "data": "m06HUq4xH9DXDxn4XKYkoeKa0apphU7p1URpmey231Ao7l05lnm2kblp9eaVRqtd"
}
```

---

`POST` /app/user/fetchInfo 获取用户信息

### 请求参数

| 参数名   | 必填 | 类型     | 描述  |
|-------|----|--------|-----|
| phone | 是  | String | 手机号 |

### 示例

``` json
{
    "phone": "13666666666",
}
```

### 成功响应

``` css
{
    "code": 0,
    "data": {
        "phone": "13629402950",
        "email": "",
        "pwd_flag": "0", // 0 未设置 1 已设置
        "recommend_code": "7Cp6CW"
    }
}
```

``` javascript
{
    "code": 0,
    "data": {
        "phone": "13629402950",
        "email": "",
        "pwd_flag": "0", // 0 未设置 1 已设置
        "recommend_code": "7Cp6CW"
    }
}
```

``` json5
{
    "code": 0,
    "data": {
        "phone": "13629402950",
        "email": "",
        "pwd_flag": "0", // 0 未设置 1 已设置
        "recommend_code": "7Cp6CW"
    }
}
```

``` 
{
    "code": 0,
    "data": {
        "phone": "13629402950",
        "email": "",
        "pwd_flag": "0", // 0 未设置 1 已设置
        "recommend_code": "7Cp6CW"
    }
}
```
---

`POST` /app/user/updatePayPwd 修改支付密码

### 请求参数

| 参数名    | 必填 | 类型     | 描述  |
|--------|----|--------|-----|
| phone  | 是  | String | 手机号 |
| oldPwd | 是  | String | 旧密码 |
| newPwd | 是  | String | 新密码 |

### 示例

``` json
{
    "phone":"13629402950",
    "new_pwd":"654321",
    "old_pwd":"123456"
}
```

### 成功响应

``` json
{
    "code": 0,
    "data": "修改成功"
}
```

---