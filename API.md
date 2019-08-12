# API

可能不全

## Requests

### **GET** - /api/login

#### CURL

```sh
curl -X GET "https://admin.gene.xluyun.com/api/login"
```

### **GET** - /api/user

#### CURL

```sh
curl -X GET "https://admin.gene.xluyun.com/api/user"
```

### **GET** - /api/admin/user/list

#### CURL

```sh
curl -X GET "https://admin.gene.xluyun.com/api/admin/user/list\
?aid=3&token=333"
```

#### Query Parameters

- **aid** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "3"
  ],
  "default": "3"
}
```
- **token** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "333"
  ],
  "default": "333"
}
```

### **GET** - /api/admin/user

#### CURL

```sh
curl -X GET "https://admin.gene.xluyun.com/api/admin/user\
?aid=3&token=333&id=8"
```

#### Query Parameters

- **aid** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "3"
  ],
  "default": "3"
}
```
- **token** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "333"
  ],
  "default": "333"
}
```
- **id** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "8"
  ],
  "default": "8"
}
```

### **GET** - /api/admin/index

#### CURL

```sh
curl -X GET "https://admin.gene.xluyun.com/api/admin/index\
?aid=3&token=333&id=1"
```

#### Query Parameters

- **aid** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "3"
  ],
  "default": "3"
}
```
- **token** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "333"
  ],
  "default": "333"
}
```
- **id** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "1"
  ],
  "default": "1"
}
```

### **GET** - /api/user/csrf

#### CURL

```sh
curl -X GET "https://admin.gene.xluyun.com/api/user/csrf"
```

### **GET** - /api/weapp/index

#### CURL

```sh
curl -X GET "https://admin.gene.xluyun.com/api/weapp/index\
?uid=1&token=1"
```

#### Query Parameters

- **uid** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "1"
  ],
  "default": "1"
}
```
- **token** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "1"
  ],
  "default": "1"
}
```

### **POST** - /api/upload

#### CURL

```sh
curl -X POST "https://admin.gene.xluyun.com/api/upload" \
    -H "Content-Type: multipart/form-data; charset=utf-8; boundary=__X_PAW_BOUNDARY__" \
    --data-raw "file"="$file"
```

#### Header Parameters

- **Content-Type** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "multipart/form-data; charset=utf-8; boundary=__X_PAW_BOUNDARY__"
  ],
  "default": "multipart/form-data; charset=utf-8; boundary=__X_PAW_BOUNDARY__"
}
```

#### Body Parameters

- **file** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    ""
  ]
}
```

### **POST** - /api/admin/order/refund

#### CURL

```sh
curl -X POST "https://admin.gene.xluyun.com/api/admin/order/refund" \
    -H "Content-Type: application/json; charset=utf-8" \
    --data-raw "$body"
```

#### Header Parameters

- **Content-Type** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "application/json; charset=utf-8"
  ],
  "default": "application/json; charset=utf-8"
}
```

#### Body Parameters

- **body** should respect the following schema:

```
{
  "type": "string",
  "default": "{\"oid\":45,\"fee\":0.02,\"refund_desc\":\"\\u534f\\u5546\\u4e00\\u81f4\"}"
}
```

### **POST** - /api/admin/coupon

#### CURL

```sh
curl -X POST "https://admin.gene.xluyun.com/api/admin/coupon\
?aid=1&token=333" \
    -H "Content-Type: application/json; charset=utf-8" \
    --data-raw "$body"
```

#### Query Parameters

- **aid** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "1"
  ],
  "default": "1"
}
```
- **token** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "333"
  ],
  "default": "333"
}
```

#### Header Parameters

- **Content-Type** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "application/json; charset=utf-8"
  ],
  "default": "application/json; charset=utf-8"
}
```

#### Body Parameters

- **body** should respect the following schema:

```
{
  "type": "string",
  "default": "{\"name\":\"\\u7a0b\\u5e8f\\u5458\\u4e13\\u5c5e\\u4f18\\u60e0\\u5238\",\"price\":1,\"min_price\":1,\"expired_time\":\"2019-02-18\",\"duration\":2,\"type\":2,\"attribute\":\"666\"}"
}
```

### **POST** - /api/admin/coupon/code

#### CURL

```sh
curl -X POST "https://admin.gene.xluyun.com/api/admin/coupon/code\
?aid=1&token=333" \
    -H "Content-Type: application/json; charset=utf-8" \
    --data-raw "$body"
```

#### Query Parameters

- **aid** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "1"
  ],
  "default": "1"
}
```
- **token** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "333"
  ],
  "default": "333"
}
```

#### Header Parameters

- **Content-Type** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "application/json; charset=utf-8"
  ],
  "default": "application/json; charset=utf-8"
}
```

#### Body Parameters

- **body** should respect the following schema:

```
{
  "type": "string",
  "default": "{\"count\":100,\"binded_company\":2,\"coupon_id\":1}"
}
```

### **PUT** - /api/admin/coupon

#### CURL

```sh
curl -X PUT "https://admin.gene.xluyun.com/api/admin/coupon\
?aid=1&token=333" \
    -H "Content-Type: application/json; charset=utf-8" \
    --data-raw "$body"
```

#### Query Parameters

- **aid** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "1"
  ],
  "default": "1"
}
```
- **token** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "333"
  ],
  "default": "333"
}
```

#### Header Parameters

- **Content-Type** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "application/json; charset=utf-8"
  ],
  "default": "application/json; charset=utf-8"
}
```

#### Body Parameters

- **body** should respect the following schema:

```
{
  "type": "string",
  "default": "{\"name\":\"\\u7a0b\\u5e8f\\u5458\\u4e13\\u5c5e\\u4f18\\u60e0\\u5238\",\"price\":1,\"min_price\":1,\"expired_time\":\"2019-02-18\",\"duration\":2,\"type\":1,\"attribute\":\"1\",\"id\":2}"
}
```

### **GET** - /api/admin/coupon/list

#### CURL

```sh
curl -X GET "https://admin.gene.xluyun.com/api/admin/coupon/list\
?uid=8&token=333" \
    -H "Content-Type: application/json; charset=utf-8" \
    --data-raw "$body"
```

#### Query Parameters

- **uid** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "8"
  ],
  "default": "8"
}
```
- **token** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "333"
  ],
  "default": "333"
}
```

#### Header Parameters

- **Content-Type** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "application/json; charset=utf-8"
  ],
  "default": "application/json; charset=utf-8"
}
```

#### Body Parameters

- **body** should respect the following schema:

```
{
  "type": "string",
  "default": "{}"
}
```

### **GET** - /api/admin/coupon/code

#### CURL

```sh
curl -X GET "https://admin.gene.xluyun.com/api/admin/coupon/code\
?uid=8&token=333" \
    -H "Content-Type: application/json; charset=utf-8" \
    --data-raw "$body"
```

#### Query Parameters

- **uid** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "8"
  ],
  "default": "8"
}
```
- **token** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "333"
  ],
  "default": "333"
}
```

#### Header Parameters

- **Content-Type** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "application/json; charset=utf-8"
  ],
  "default": "application/json; charset=utf-8"
}
```

#### Body Parameters

- **body** should respect the following schema:

```
{
  "type": "string",
  "default": "{}"
}
```

### **GET** - /api/admin/coupon/record

#### CURL

```sh
curl -X GET "https://admin.gene.xluyun.com/api/admin/coupon/record\
?uid=8&token=333&coupon=2" \
    -H "Content-Type: application/json; charset=utf-8" \
    --data-raw "$body"
```

#### Query Parameters

- **uid** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "8"
  ],
  "default": "8"
}
```
- **token** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "333"
  ],
  "default": "333"
}
```
- **coupon** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "2"
  ],
  "default": "2"
}
```

#### Header Parameters

- **Content-Type** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "application/json; charset=utf-8"
  ],
  "default": "application/json; charset=utf-8"
}
```

#### Body Parameters

- **body** should respect the following schema:

```
{
  "type": "string",
  "default": "{}"
}
```

### **GET** - /api/admin/coupon

#### CURL

```sh
curl -X GET "https://admin.gene.xluyun.com/api/admin/coupon\
?uid=8&token=333&id=1"
```

#### Query Parameters

- **uid** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "8"
  ],
  "default": "8"
}
```
- **token** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "333"
  ],
  "default": "333"
}
```
- **id** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "1"
  ],
  "default": "1"
}
```

### **DELETE** - /api/admin/coupon

#### CURL

```sh
curl -X DELETE "https://admin.gene.xluyun.com/api/admin/coupon\
?uid=8&token=333&id=5" \
    -H "Content-Type: application/json; charset=utf-8" \
    --data-raw "$body"
```

#### Query Parameters

- **uid** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "8"
  ],
  "default": "8"
}
```
- **token** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "333"
  ],
  "default": "333"
}
```
- **id** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "5"
  ],
  "default": "5"
}
```

#### Header Parameters

- **Content-Type** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "application/json; charset=utf-8"
  ],
  "default": "application/json; charset=utf-8"
}
```

#### Body Parameters

- **body** should respect the following schema:

```
{
  "type": "string",
  "default": "{}"
}
```

### **DELETE** - /api/admin/coupon/code

#### CURL

```sh
curl -X DELETE "https://admin.gene.xluyun.com/api/admin/coupon/code\
?uid=8&token=333&code=0000000302136940" \
    -H "Content-Type: application/json; charset=utf-8" \
    --data-raw "$body"
```

#### Query Parameters

- **uid** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "8"
  ],
  "default": "8"
}
```
- **token** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "333"
  ],
  "default": "333"
}
```
- **code** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "0000000302136940"
  ],
  "default": "0000000302136940"
}
```

#### Header Parameters

- **Content-Type** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "application/json; charset=utf-8"
  ],
  "default": "application/json; charset=utf-8"
}
```

#### Body Parameters

- **body** should respect the following schema:

```
{
  "type": "string",
  "default": "{}"
}
```

### **POST** - /api/admin/banner

#### CURL

```sh
curl -X POST "https://admin.gene.xluyun.com/api/admin/banner\
?aid=1&token=333" \
    -H "Content-Type: application/json; charset=utf-8" \
    --data-raw "$body"
```

#### Query Parameters

- **aid** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "1"
  ],
  "default": "1"
}
```
- **token** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "333"
  ],
  "default": "333"
}
```

#### Header Parameters

- **Content-Type** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "application/json; charset=utf-8"
  ],
  "default": "application/json; charset=utf-8"
}
```

#### Body Parameters

- **body** should respect the following schema:

```
{
  "type": "string",
  "default": "{\"image\":\"https://www.baidu.com\",\"to_type\":1,\"to_attr\":\"1\"}"
}
```

### **GET** - /api/admin/banner

#### CURL

```sh
curl -X GET "https://admin.gene.xluyun.com/api/admin/banner\
?uid=8&token=333&id=1"
```

#### Query Parameters

- **uid** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "8"
  ],
  "default": "8"
}
```
- **token** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "333"
  ],
  "default": "333"
}
```
- **id** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "1"
  ],
  "default": "1"
}
```

### **DELETE** - /api/admin/banner

#### CURL

```sh
curl -X DELETE "https://admin.gene.xluyun.com/api/admin/banner\
?uid=8&token=333&id=2" \
    -H "Content-Type: application/json; charset=utf-8" \
    --data-raw "$body"
```

#### Query Parameters

- **uid** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "8"
  ],
  "default": "8"
}
```
- **token** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "333"
  ],
  "default": "333"
}
```
- **id** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "2"
  ],
  "default": "2"
}
```

#### Header Parameters

- **Content-Type** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "application/json; charset=utf-8"
  ],
  "default": "application/json; charset=utf-8"
}
```

#### Body Parameters

- **body** should respect the following schema:

```
{
  "type": "string",
  "default": "{}"
}
```

### **GET** - /api/admin/banner/list

#### CURL

```sh
curl -X GET "https://admin.gene.xluyun.com/api/admin/banner/list\
?uid=8&token=333" \
    -H "Content-Type: application/json; charset=utf-8" \
    --data-raw "$body"
```

#### Query Parameters

- **uid** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "8"
  ],
  "default": "8"
}
```
- **token** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "333"
  ],
  "default": "333"
}
```

#### Header Parameters

- **Content-Type** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "application/json; charset=utf-8"
  ],
  "default": "application/json; charset=utf-8"
}
```

#### Body Parameters

- **body** should respect the following schema:

```
{
  "type": "string",
  "default": "{}"
}
```

### **PUT** - /api/admin/banner

#### CURL

```sh
curl -X PUT "https://admin.gene.xluyun.com/api/admin/banner\
?uid=8&token=333" \
    -H "Content-Type: application/json; charset=utf-8" \
    --data-raw "$body"
```

#### Query Parameters

- **uid** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "8"
  ],
  "default": "8"
}
```
- **token** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "333"
  ],
  "default": "333"
}
```

#### Header Parameters

- **Content-Type** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "application/json; charset=utf-8"
  ],
  "default": "application/json; charset=utf-8"
}
```

#### Body Parameters

- **body** should respect the following schema:

```
{
  "type": "string",
  "default": "{\"address_name\":\"\\u738b\\u8fdb\\u559c4\",\"address_phone\":\"15300000000\",\"address_district\":\"\\u4e0a\\u6d77\\u5e02 \\u6768\\u6d66\\u533a\",\"address_location\":\"\\u56db\\u5e73\\u8def1239\\u53f7\\u540c\\u6d4e\\u5927\\u5b66\",\"id\":2,\"is_default\":1}"
}
```

### **POST** - /api/admin/recommend

#### CURL

```sh
curl -X POST "https://admin.gene.xluyun.com/api/admin/recommend\
?aid=1&token=333" \
    -H "Content-Type: application/json; charset=utf-8" \
    --data-raw "$body"
```

#### Query Parameters

- **aid** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "1"
  ],
  "default": "1"
}
```
- **token** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "333"
  ],
  "default": "333"
}
```

#### Header Parameters

- **Content-Type** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "application/json; charset=utf-8"
  ],
  "default": "application/json; charset=utf-8"
}
```

#### Body Parameters

- **body** should respect the following schema:

```
{
  "type": "string",
  "default": "{\"gid\":1}"
}
```

### **DELETE** - /api/admin/recommend

#### CURL

```sh
curl -X DELETE "https://admin.gene.xluyun.com/api/admin/recommend\
?uid=8&token=333&id=1" \
    -H "Content-Type: application/json; charset=utf-8" \
    --data-raw "$body"
```

#### Query Parameters

- **uid** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "8"
  ],
  "default": "8"
}
```
- **token** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "333"
  ],
  "default": "333"
}
```
- **id** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "1"
  ],
  "default": "1"
}
```

#### Header Parameters

- **Content-Type** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "application/json; charset=utf-8"
  ],
  "default": "application/json; charset=utf-8"
}
```

#### Body Parameters

- **body** should respect the following schema:

```
{
  "type": "string",
  "default": "{}"
}
```

### **GET** - /api/admin/recommend/list

#### CURL

```sh
curl -X GET "https://admin.gene.xluyun.com/api/admin/recommend/list\
?uid=8&token=333" \
    -H "Content-Type: application/json; charset=utf-8" \
    --data-raw "$body"
```

#### Query Parameters

- **uid** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "8"
  ],
  "default": "8"
}
```
- **token** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "333"
  ],
  "default": "333"
}
```

#### Header Parameters

- **Content-Type** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "application/json; charset=utf-8"
  ],
  "default": "application/json; charset=utf-8"
}
```

#### Body Parameters

- **body** should respect the following schema:

```
{
  "type": "string",
  "default": "{}"
}
```

### **PUT** - /api/admin/recommend

#### CURL

```sh
curl -X PUT "https://admin.gene.xluyun.com/api/admin/recommend\
?uid=8&token=333" \
    -H "Content-Type: application/json; charset=utf-8" \
    --data-raw "$body"
```

#### Query Parameters

- **uid** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "8"
  ],
  "default": "8"
}
```
- **token** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "333"
  ],
  "default": "333"
}
```

#### Header Parameters

- **Content-Type** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "application/json; charset=utf-8"
  ],
  "default": "application/json; charset=utf-8"
}
```

#### Body Parameters

- **body** should respect the following schema:

```
{
  "type": "string",
  "default": "{\"address_name\":\"\\u738b\\u8fdb\\u559c4\",\"address_phone\":\"15300000000\",\"address_district\":\"\\u4e0a\\u6d77\\u5e02 \\u6768\\u6d66\\u533a\",\"address_location\":\"\\u56db\\u5e73\\u8def1239\\u53f7\\u540c\\u6d4e\\u5927\\u5b66\",\"id\":2,\"is_default\":1}"
}
```

### **GET** - /api/admin/box

#### CURL

```sh
curl -X GET "https://admin.gene.xluyun.com/api/admin/box\
?aid=2&id=100003&token=6c7a3926d6ceb89e8ef3c3a7a9ed1009"
```

#### Query Parameters

- **aid** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "2"
  ],
  "default": "2"
}
```
- **id** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "100003"
  ],
  "default": "100003"
}
```
- **token** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "6c7a3926d6ceb89e8ef3c3a7a9ed1009"
  ],
  "default": "6c7a3926d6ceb89e8ef3c3a7a9ed1009"
}
```

### **GET** - /api/weapp/box

#### CURL

```sh
curl -X GET "https://admin.gene.xluyun.com/api/weapp/box\
?uid=2&id=100000&token=6c7a3926d6ceb89e8ef3c3a7a9ed1009"
```

#### Query Parameters

- **uid** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "2"
  ],
  "default": "2"
}
```
- **id** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "100000"
  ],
  "default": "100000"
}
```
- **token** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "6c7a3926d6ceb89e8ef3c3a7a9ed1009"
  ],
  "default": "6c7a3926d6ceb89e8ef3c3a7a9ed1009"
}
```

### **GET** - /api/admin/box/list

#### CURL

```sh
curl -X GET "https://admin.gene.xluyun.com/api/admin/box/list\
?aid=3&token=3&pageSize=10&page=1"
```

#### Query Parameters

- **aid** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "3"
  ],
  "default": "3"
}
```
- **token** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "3"
  ],
  "default": "3"
}
```
- **pageSize** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "10"
  ],
  "default": "10"
}
```
- **page** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "1"
  ],
  "default": "1"
}
```

### **GET** - /api/weapp/box/list

#### CURL

```sh
curl -X GET "https://admin.gene.xluyun.com/api/weapp/box/list\
?uid=8&token=3&pageSize=10&page=1&type=2"
```

#### Query Parameters

- **uid** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "8"
  ],
  "default": "8"
}
```
- **token** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "3"
  ],
  "default": "3"
}
```
- **pageSize** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "10"
  ],
  "default": "10"
}
```
- **page** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "1"
  ],
  "default": "1"
}
```
- **type** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "2"
  ],
  "default": "2"
}
```

### **POST** - /api/admin/box

#### CURL

```sh
curl -X POST "https://admin.gene.xluyun.com/api/admin/box\
?aid=1&token=333" \
    -H "Content-Type: application/json; charset=utf-8" \
    --data-raw "$body"
```

#### Query Parameters

- **aid** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "1"
  ],
  "default": "1"
}
```
- **token** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "333"
  ],
  "default": "333"
}
```

#### Header Parameters

- **Content-Type** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "application/json; charset=utf-8"
  ],
  "default": "application/json; charset=utf-8"
}
```

#### Body Parameters

- **body** should respect the following schema:

```
{
  "type": "string",
  "default": "{\"code\":\"1000022\"}"
}
```

### **POST** - /api/weapp/box/attach

#### CURL

```sh
curl -X POST "https://admin.gene.xluyun.com/api/weapp/box/attach\
?uid=8&token=333" \
    -H "Content-Type: application/json; charset=utf-8" \
    --data-raw "$body"
```

#### Query Parameters

- **uid** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "8"
  ],
  "default": "8"
}
```
- **token** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "333"
  ],
  "default": "333"
}
```

#### Header Parameters

- **Content-Type** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "application/json; charset=utf-8"
  ],
  "default": "application/json; charset=utf-8"
}
```

#### Body Parameters

- **body** should respect the following schema:

```
{
  "type": "string",
  "default": "{\"code\":\"201901\"}"
}
```

### **POST** - /api/admin/box/checkitem

#### CURL

```sh
curl -X POST "https://admin.gene.xluyun.com/api/admin/box/checkitem\
?aid=1&token=333" \
    -H "Content-Type: application/json; charset=utf-8" \
    --data-raw "$body"
```

#### Query Parameters

- **aid** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "1"
  ],
  "default": "1"
}
```
- **token** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "333"
  ],
  "default": "333"
}
```

#### Header Parameters

- **Content-Type** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "application/json; charset=utf-8"
  ],
  "default": "application/json; charset=utf-8"
}
```

#### Body Parameters

- **body** should respect the following schema:

```
{
  "type": "string",
  "default": "{\"box_code\":\"19099\",\"checkitem_id\":6}"
}
```

### **POST** - /api/admin/box/import

#### CURL

```sh
curl -X POST "https://admin.gene.xluyun.com/api/admin/box/import\
?aid=1&token=333" \
    -H "Content-Type: application/json; charset=utf-8" \
    --data-raw "$body"
```

#### Query Parameters

- **aid** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "1"
  ],
  "default": "1"
}
```
- **token** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "333"
  ],
  "default": "333"
}
```

#### Header Parameters

- **Content-Type** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "application/json; charset=utf-8"
  ],
  "default": "application/json; charset=utf-8"
}
```

#### Body Parameters

- **body** should respect the following schema:

```
{
  "type": "string",
  "default": "{\"boxs\":[{\"box_code\":\"1010\",\"phone_number\":\"13000000000\"}],\"checkitems\":[3,6]}"
}
```

### **GET** - /api/admin/box/list/settled

#### CURL

```sh
curl -X GET "https://admin.gene.xluyun.com/api/admin/box/list/settled\
?aid=1&token=333" \
    -H "Content-Type: application/json; charset=utf-8" \
    --data-raw "$body"
```

#### Query Parameters

- **aid** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "1"
  ],
  "default": "1"
}
```
- **token** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "333"
  ],
  "default": "333"
}
```

#### Header Parameters

- **Content-Type** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "application/json; charset=utf-8"
  ],
  "default": "application/json; charset=utf-8"
}
```

#### Body Parameters

- **body** should respect the following schema:

```
{
  "type": "string",
  "default": "{\"user_id\":7}"
}
```

### **GET** - /api/admin/box/list/unsettled

#### CURL

```sh
curl -X GET "https://admin.gene.xluyun.com/api/admin/box/list/unsettled\
?aid=1&token=333&phone_number=13000000000" \
    -H "Content-Type: application/json; charset=utf-8" \
    --data-raw "$body"
```

#### Query Parameters

- **aid** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "1"
  ],
  "default": "1"
}
```
- **token** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "333"
  ],
  "default": "333"
}
```
- **phone_number** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "13000000000"
  ],
  "default": "13000000000"
}
```

#### Header Parameters

- **Content-Type** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "application/json; charset=utf-8"
  ],
  "default": "application/json; charset=utf-8"
}
```

#### Body Parameters

- **body** should respect the following schema:

```
{
  "type": "string",
  "default": "{\"phone_number\":\"100000\"}"
}
```

### **PUT** - /api/admin/box

#### CURL

```sh
curl -X PUT "https://admin.gene.xluyun.com/api/admin/box\
?aid=1" \
    -H "Content-Type: application/json; charset=utf-8" \
    --data-raw "$body"
```

#### Query Parameters

- **aid** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "1"
  ],
  "default": "1"
}
```

#### Header Parameters

- **Content-Type** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "application/json; charset=utf-8"
  ],
  "default": "application/json; charset=utf-8"
}
```

#### Body Parameters

- **body** should respect the following schema:

```
{
  "type": "string",
  "default": "{\"id\":2,\"description\":\"\\u4f60\\u786e\\u5b9e\\u662f\\u6709\\u75c5\"}"
}
```

### **DELETE** - /api/admin/box

#### CURL

```sh
curl -X DELETE "https://admin.gene.xluyun.com/api/admin/box\
?aid=2&id=100000" \
    -H "Content-Type: application/json; charset=utf-8" \
    --data-raw "$body"
```

#### Query Parameters

- **aid** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "2"
  ],
  "default": "2"
}
```
- **id** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "100000"
  ],
  "default": "100000"
}
```

#### Header Parameters

- **Content-Type** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "application/json; charset=utf-8"
  ],
  "default": "application/json; charset=utf-8"
}
```

#### Body Parameters

- **body** should respect the following schema:

```
{
  "type": "string",
  "default": "{}"
}
```

### **DELETE** - /api/admin/box/checkitem

#### CURL

```sh
curl -X DELETE "https://admin.gene.xluyun.com/api/admin/box/checkitem\
?box_code=19099&checkitem_id=6" \
    -H "Content-Type: application/json; charset=utf-8" \
    --data-raw "$body"
```

#### Query Parameters

- **box_code** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "19099"
  ],
  "default": "19099"
}
```
- **checkitem_id** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "6"
  ],
  "default": "6"
}
```

#### Header Parameters

- **Content-Type** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "application/json; charset=utf-8"
  ],
  "default": "application/json; charset=utf-8"
}
```

#### Body Parameters

- **body** should respect the following schema:

```
{
  "type": "string",
  "default": "{}"
}
```

### **GET** - /api/admin/checkitem/report

#### CURL

```sh
curl -X GET "https://admin.gene.xluyun.com/api/admin/checkitem/report\
?id=5" \
    -H "Content-Type: application/json; charset=utf-8" \
    --data-raw "$body"
```

#### Query Parameters

- **id** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "5"
  ],
  "default": "5"
}
```

#### Header Parameters

- **Content-Type** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "application/json; charset=utf-8"
  ],
  "default": "application/json; charset=utf-8"
}
```

#### Body Parameters

- **body** should respect the following schema:

```
{
  "type": "string",
  "default": "{}"
}
```

### **POST** - /api/admin/checkitem/report

#### CURL

```sh
curl -X POST "https://admin.gene.xluyun.com/api/admin/checkitem/report" \
    -H "Content-Type: application/json; charset=utf-8" \
    --data-raw "$body"
```

#### Header Parameters

- **Content-Type** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "application/json; charset=utf-8"
  ],
  "default": "application/json; charset=utf-8"
}
```

#### Body Parameters

- **body** should respect the following schema:

```
{
  "type": "string",
  "default": "{\"checkitem_id\":6,\"info\":\"{\\\"a\\\":\\\"b\\\"}\"}"
}
```

### **GET** - /api/admin/query/user

#### CURL

```sh
curl -X GET "https://admin.gene.xluyun.com/api/admin/query/user\
?aid=1&token=2&query=$query" \
    -H "Content-Type: application/json; charset=utf-8" \
    --data-raw "$body"
```

#### Query Parameters

- **aid** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "1"
  ],
  "default": "1"
}
```
- **token** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "2"
  ],
  "default": "2"
}
```
- **query** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    ""
  ]
}
```

#### Header Parameters

- **Content-Type** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "application/json; charset=utf-8"
  ],
  "default": "application/json; charset=utf-8"
}
```

#### Body Parameters

- **body** should respect the following schema:

```
{
  "type": "string",
  "default": "{\"title\":\"\",\"author\":\"\",\"content\":\"\",\"cover\":\"\",\"goods\":\"\",\"tickets\":\"\",\"id\":\"\"}"
}
```

### **GET** - /api/admin/query/box

#### CURL

```sh
curl -X GET "https://admin.gene.xluyun.com/api/admin/query/box\
?aid=1&token=2&query=1" \
    -H "Content-Type: application/json; charset=utf-8" \
    --data-raw "$body"
```

#### Query Parameters

- **aid** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "1"
  ],
  "default": "1"
}
```
- **token** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "2"
  ],
  "default": "2"
}
```
- **query** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "1"
  ],
  "default": "1"
}
```

#### Header Parameters

- **Content-Type** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "application/json; charset=utf-8"
  ],
  "default": "application/json; charset=utf-8"
}
```

#### Body Parameters

- **body** should respect the following schema:

```
{
  "type": "string",
  "default": "{}"
}
```

### **GET** - /api/admin/query/checkitem

#### CURL

```sh
curl -X GET "https://admin.gene.xluyun.com/api/admin/query/checkitem\
?aid=1&token=2&query=$query" \
    -H "Content-Type: application/json; charset=utf-8" \
    --data-raw "$body"
```

#### Query Parameters

- **aid** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "1"
  ],
  "default": "1"
}
```
- **token** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "2"
  ],
  "default": "2"
}
```
- **query** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    ""
  ]
}
```

#### Header Parameters

- **Content-Type** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "application/json; charset=utf-8"
  ],
  "default": "application/json; charset=utf-8"
}
```

#### Body Parameters

- **body** should respect the following schema:

```
{
  "type": "string",
  "default": "{\"title\":\"\",\"author\":\"\",\"content\":\"\",\"cover\":\"\",\"goods\":\"\",\"tickets\":\"\",\"id\":\"\"}"
}
```

### **GET** - /api/admin/report

#### CURL

```sh
curl -X GET "https://admin.gene.xluyun.com/api/admin/report\
?aid=2&id=100000&token=6c7a3926d6ceb89e8ef3c3a7a9ed1009"
```

#### Query Parameters

- **aid** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "2"
  ],
  "default": "2"
}
```
- **id** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "100000"
  ],
  "default": "100000"
}
```
- **token** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "6c7a3926d6ceb89e8ef3c3a7a9ed1009"
  ],
  "default": "6c7a3926d6ceb89e8ef3c3a7a9ed1009"
}
```

### **GET** - /api/weapp/report/list

#### CURL

```sh
curl -X GET "https://admin.gene.xluyun.com/api/weapp/report/list\
?uid=8&id=1001&token=6c7a3926d6ceb89e8ef3c3a7a9ed1009"
```

#### Query Parameters

- **uid** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "8"
  ],
  "default": "8"
}
```
- **id** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "1001"
  ],
  "default": "1001"
}
```
- **token** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "6c7a3926d6ceb89e8ef3c3a7a9ed1009"
  ],
  "default": "6c7a3926d6ceb89e8ef3c3a7a9ed1009"
}
```

### **GET** - /api/report/checkitem

#### CURL

```sh
curl -X GET "https://admin.gene.xluyun.com/api/report/checkitem\
?uid=8&checkitem_id=8&token=6c7a3926d6ceb89e8ef3c3a7a9ed1009&box_code=100000"
```

#### Query Parameters

- **uid** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "8"
  ],
  "default": "8"
}
```
- **checkitem_id** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "8"
  ],
  "default": "8"
}
```
- **token** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "6c7a3926d6ceb89e8ef3c3a7a9ed1009"
  ],
  "default": "6c7a3926d6ceb89e8ef3c3a7a9ed1009"
}
```
- **box_code** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "100000"
  ],
  "default": "100000"
}
```

### **GET** - /api/report/subitem

#### CURL

```sh
curl -X GET "https://admin.gene.xluyun.com/api/report/subitem\
?uid=8&checkitem_id=8&token=6c7a3926d6ceb89e8ef3c3a7a9ed1009\
&sub_item_id=1543242282124"
```

#### Query Parameters

- **uid** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "8"
  ],
  "default": "8"
}
```
- **checkitem_id** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "8"
  ],
  "default": "8"
}
```
- **token** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "6c7a3926d6ceb89e8ef3c3a7a9ed1009"
  ],
  "default": "6c7a3926d6ceb89e8ef3c3a7a9ed1009"
}
```
- **sub_item_id** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "1543242282124"
  ],
  "default": "1543242282124"
}
```

### **GET** - /api/admin/report/sample

#### CURL

```sh
curl -X GET "https://admin.gene.xluyun.com/api/admin/report/sample\
?aid=2&ids=2%2C4%2C5&token=6c7a3926d6ceb89e8ef3c3a7a9ed1009"
```

#### Query Parameters

- **aid** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "2"
  ],
  "default": "2"
}
```
- **ids** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "2,4,5"
  ],
  "default": "2,4,5"
}
```
- **token** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "6c7a3926d6ceb89e8ef3c3a7a9ed1009"
  ],
  "default": "6c7a3926d6ceb89e8ef3c3a7a9ed1009"
}
```

### **GET** - /api/admin/report/list

#### CURL

```sh
curl -X GET "https://admin.gene.xluyun.com/api/admin/report/list\
?aid=3&token=3&pageSize=10&page=1"
```

#### Query Parameters

- **aid** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "3"
  ],
  "default": "3"
}
```
- **token** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "3"
  ],
  "default": "3"
}
```
- **pageSize** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "10"
  ],
  "default": "10"
}
```
- **page** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "1"
  ],
  "default": "1"
}
```

### **POST** - /api/admin/report

#### CURL

```sh
curl -X POST "https://admin.gene.xluyun.com/api/admin/report\
?aid=1&token=333" \
    -H "Content-Type: application/json; charset=utf-8" \
    --data-raw "$body"
```

#### Query Parameters

- **aid** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "1"
  ],
  "default": "1"
}
```
- **token** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "333"
  ],
  "default": "333"
}
```

#### Header Parameters

- **Content-Type** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "application/json; charset=utf-8"
  ],
  "default": "application/json; charset=utf-8"
}
```

#### Body Parameters

- **body** should respect the following schema:

```
{
  "type": "string",
  "default": "{\"box_code\":\"1001\",\"info\":\"{\\\"s1\\\":1, \\\"s2\\\": 3}\"}"
}
```

### **PUT** - /api/admin/report

#### CURL

```sh
curl -X PUT "https://admin.gene.xluyun.com/api/admin/report\
?aid=1" \
    -H "Content-Type: application/json; charset=utf-8" \
    --data-raw "$body"
```

#### Query Parameters

- **aid** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "1"
  ],
  "default": "1"
}
```

#### Header Parameters

- **Content-Type** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "application/json; charset=utf-8"
  ],
  "default": "application/json; charset=utf-8"
}
```

#### Body Parameters

- **body** should respect the following schema:

```
{
  "type": "string",
  "default": "{\"box_code\":\"1001\",\"info\":\"{\\\"a\\\": 1, \\\"b\\\": 2}\"}"
}
```

### **DELETE** - /api/admin/report

#### CURL

```sh
curl -X DELETE "https://admin.gene.xluyun.com/api/admin/report\
?aid=2&id=1001" \
    -H "Content-Type: application/json; charset=utf-8" \
    --data-raw "$body"
```

#### Query Parameters

- **aid** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "2"
  ],
  "default": "2"
}
```
- **id** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "1001"
  ],
  "default": "1001"
}
```

#### Header Parameters

- **Content-Type** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "application/json; charset=utf-8"
  ],
  "default": "application/json; charset=utf-8"
}
```

#### Body Parameters

- **body** should respect the following schema:

```
{
  "type": "string",
  "default": "{}"
}
```

### **GET** - /api/weapp/report

#### CURL

```sh
curl -X GET "https://admin.gene.xluyun.com/api/weapp/report\
?uid=8&token=0&id=100000" \
    -H "Content-Type: application/json; charset=utf-8" \
    --data-raw "$body"
```

#### Query Parameters

- **uid** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "8"
  ],
  "default": "8"
}
```
- **token** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "0"
  ],
  "default": "0"
}
```
- **id** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "100000"
  ],
  "default": "100000"
}
```

#### Header Parameters

- **Content-Type** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "application/json; charset=utf-8"
  ],
  "default": "application/json; charset=utf-8"
}
```

#### Body Parameters

- **body** should respect the following schema:

```
{
  "type": "string",
  "default": "{\"phone_number\":\"15301921831\"}"
}
```

### **POST** - /api/weapp/attachPhone/start

#### CURL

```sh
curl -X POST "https://admin.gene.xluyun.com/api/weapp/attachPhone/start\
?uid=9&token=0" \
    -H "Content-Type: application/json; charset=utf-8" \
    --data-raw "$body"
```

#### Query Parameters

- **uid** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "9"
  ],
  "default": "9"
}
```
- **token** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "0"
  ],
  "default": "0"
}
```

#### Header Parameters

- **Content-Type** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "application/json; charset=utf-8"
  ],
  "default": "application/json; charset=utf-8"
}
```

#### Body Parameters

- **body** should respect the following schema:

```
{
  "type": "string",
  "default": "{\"phone_number\":\"15301921831\"}"
}
```

### **POST** - /api/weapp/attachPhone

#### CURL

```sh
curl -X POST "https://admin.gene.xluyun.com/api/weapp/attachPhone\
?uid=8&token=0" \
    -H "Content-Type: application/json; charset=utf-8" \
    --data-raw "$body"
```

#### Query Parameters

- **uid** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "8"
  ],
  "default": "8"
}
```
- **token** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "0"
  ],
  "default": "0"
}
```

#### Header Parameters

- **Content-Type** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "application/json; charset=utf-8"
  ],
  "default": "application/json; charset=utf-8"
}
```

#### Body Parameters

- **body** should respect the following schema:

```
{
  "type": "string",
  "default": "{\"phone_number\":\"15301921831\",\"code\":\"000011\"}"
}
```

### **GET** - /api/admin/checkitem

#### CURL

```sh
curl -X GET "https://admin.gene.xluyun.com/api/admin/checkitem\
?aid=2&id=1&token=6c7a3926d6ceb89e8ef3c3a7a9ed1009"
```

#### Query Parameters

- **aid** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "2"
  ],
  "default": "2"
}
```
- **id** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "1"
  ],
  "default": "1"
}
```
- **token** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "6c7a3926d6ceb89e8ef3c3a7a9ed1009"
  ],
  "default": "6c7a3926d6ceb89e8ef3c3a7a9ed1009"
}
```

### **GET** - /api/admin/checkitem/list

#### CURL

```sh
curl -X GET "https://admin.gene.xluyun.com/api/admin/checkitem/list\
?aid=3&token=3&pageSize=10&page=1"
```

#### Query Parameters

- **aid** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "3"
  ],
  "default": "3"
}
```
- **token** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "3"
  ],
  "default": "3"
}
```
- **pageSize** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "10"
  ],
  "default": "10"
}
```
- **page** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "1"
  ],
  "default": "1"
}
```

### **POST** - /api/admin/checkitem

#### CURL

```sh
curl -X POST "https://admin.gene.xluyun.com/api/admin/checkitem\
?aid=1&token=333" \
    -H "Content-Type: application/json; charset=utf-8" \
    --data-raw "$body"
```

#### Query Parameters

- **aid** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "1"
  ],
  "default": "1"
}
```
- **token** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "333"
  ],
  "default": "333"
}
```

#### Header Parameters

- **Content-Type** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "application/json; charset=utf-8"
  ],
  "default": "application/json; charset=utf-8"
}
```

#### Body Parameters

- **body** should respect the following schema:

```
{
  "type": "string",
  "default": "{\"name\":\"\\u67d0\\u9879\\u76ee1\",\"header\":\"jjj\",\"description\":\"\\u68c0\\u6d4b\\u4f60\\u662f\\u4e0d\\u662f\\u6709\\u75c51\",\"order\":\"2\"}"
}
```

### **PUT** - /api/admin/checkitem

#### CURL

```sh
curl -X PUT "https://admin.gene.xluyun.com/api/admin/checkitem\
?aid=1" \
    -H "Content-Type: application/json; charset=utf-8" \
    --data-raw "$body"
```

#### Query Parameters

- **aid** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "1"
  ],
  "default": "1"
}
```

#### Header Parameters

- **Content-Type** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "application/json; charset=utf-8"
  ],
  "default": "application/json; charset=utf-8"
}
```

#### Body Parameters

- **body** should respect the following schema:

```
{
  "type": "string",
  "default": "{\"id\":2,\"description\":\"\\u4f60\\u786e\\u5b9e\\u662f\\u6709\\u75c5\"}"
}
```

### **DELETE** - /api/admin/checkitem

#### CURL

```sh
curl -X DELETE "https://admin.gene.xluyun.com/api/admin/checkitem\
?aid=2&id=1" \
    -H "Content-Type: application/json; charset=utf-8" \
    --data-raw "$body"
```

#### Query Parameters

- **aid** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "2"
  ],
  "default": "2"
}
```
- **id** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "1"
  ],
  "default": "1"
}
```

#### Header Parameters

- **Content-Type** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "application/json; charset=utf-8"
  ],
  "default": "application/json; charset=utf-8"
}
```

#### Body Parameters

- **body** should respect the following schema:

```
{
  "type": "string",
  "default": "{}"
}
```

### **GET** - /api/admin/admin

#### CURL

```sh
curl -X GET "https://admin.gene.xluyun.com/api/admin/admin\
?aid=2&id=2&token=6c7a3926d6ceb89e8ef3c3a7a9ed1009"
```

#### Query Parameters

- **aid** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "2"
  ],
  "default": "2"
}
```
- **id** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "2"
  ],
  "default": "2"
}
```
- **token** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "6c7a3926d6ceb89e8ef3c3a7a9ed1009"
  ],
  "default": "6c7a3926d6ceb89e8ef3c3a7a9ed1009"
}
```

### **POST** - /api/login/admin

#### CURL

```sh
curl -X POST "https://admin.gene.xluyun.com/api/login/admin" \
    -H "Content-Type: application/json; charset=utf-8" \
    --data-raw "$body"
```

#### Header Parameters

- **Content-Type** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "application/json; charset=utf-8"
  ],
  "default": "application/json; charset=utf-8"
}
```

#### Body Parameters

- **body** should respect the following schema:

```
{
  "type": "string",
  "default": "{\"username\":\"admin\",\"password\":\"passowrd\"}"
}
```

### **GET** - /api/admin/admin/list

#### CURL

```sh
curl -X GET "https://admin.gene.xluyun.com/api/admin/admin/list\
?aid=3&token=3&pageSize=10&page=1"
```

#### Query Parameters

- **aid** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "3"
  ],
  "default": "3"
}
```
- **token** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "3"
  ],
  "default": "3"
}
```
- **pageSize** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "10"
  ],
  "default": "10"
}
```
- **page** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "1"
  ],
  "default": "1"
}
```

### **POST** - /api/admin/admin

#### CURL

```sh
curl -X POST "https://admin.gene.xluyun.com/api/admin/admin\
?aid=1&token=333" \
    -H "Content-Type: application/json; charset=utf-8" \
    --data-raw "$body"
```

#### Query Parameters

- **aid** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "1"
  ],
  "default": "1"
}
```
- **token** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "333"
  ],
  "default": "333"
}
```

#### Header Parameters

- **Content-Type** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "application/json; charset=utf-8"
  ],
  "default": "application/json; charset=utf-8"
}
```

#### Body Parameters

- **body** should respect the following schema:

```
{
  "type": "string",
  "default": "{\"username\":\"admin1\",\"password\":\"admin\",\"identity\":0,\"realname\":\"0staerk\"}"
}
```

### **PUT** - /api/admin/admin

#### CURL

```sh
curl -X PUT "https://admin.gene.xluyun.com/api/admin/admin\
?aid=1" \
    -H "Content-Type: application/json; charset=utf-8" \
    --data-raw "$body"
```

#### Query Parameters

- **aid** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "1"
  ],
  "default": "1"
}
```

#### Header Parameters

- **Content-Type** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "application/json; charset=utf-8"
  ],
  "default": "application/json; charset=utf-8"
}
```

#### Body Parameters

- **body** should respect the following schema:

```
{
  "type": "string",
  "default": "{\"id\":2,\"identity\":3}"
}
```

### **DELETE** - /api/admin/admin

#### CURL

```sh
curl -X DELETE "https://admin.gene.xluyun.com/api/admin/admin\
?aid=2&id=1" \
    -H "Content-Type: application/json; charset=utf-8" \
    --data-raw "$body"
```

#### Query Parameters

- **aid** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "2"
  ],
  "default": "2"
}
```
- **id** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "1"
  ],
  "default": "1"
}
```

#### Header Parameters

- **Content-Type** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "application/json; charset=utf-8"
  ],
  "default": "application/json; charset=utf-8"
}
```

#### Body Parameters

- **body** should respect the following schema:

```
{
  "type": "string",
  "default": "{}"
}
```

### **POST** - /api/admin/password_reset

#### CURL

```sh
curl -X POST "https://admin.gene.xluyun.com/api/admin/password_reset\
?aid=2&token=1" \
    -H "Content-Type: application/json; charset=utf-8" \
    --data-raw "$body"
```

#### Query Parameters

- **aid** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "2"
  ],
  "default": "2"
}
```
- **token** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "1"
  ],
  "default": "1"
}
```

#### Header Parameters

- **Content-Type** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "application/json; charset=utf-8"
  ],
  "default": "application/json; charset=utf-8"
}
```

#### Body Parameters

- **body** should respect the following schema:

```
{
  "type": "string",
  "default": "{\"old\":\"admin\",\"password\":\"password\"}"
}
```

### **POST** - /api/admin/type

#### CURL

```sh
curl -X POST "https://admin.gene.xluyun.com/api/admin/type\
?aid=1&token=333" \
    -H "Content-Type: application/json; charset=utf-8" \
    --data-raw "$body"
```

#### Query Parameters

- **aid** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "1"
  ],
  "default": "1"
}
```
- **token** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "333"
  ],
  "default": "333"
}
```

#### Header Parameters

- **Content-Type** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "application/json; charset=utf-8"
  ],
  "default": "application/json; charset=utf-8"
}
```

#### Body Parameters

- **body** should respect the following schema:

```
{
  "type": "string",
  "default": "{\"name\":\"\\u5206\\u7c7b2\",\"order\":3}"
}
```

### **GET** - /api/admin/type

#### CURL

```sh
curl -X GET "https://admin.gene.xluyun.com/api/admin/type\
?uid=8&token=333&id=1"
```

#### Query Parameters

- **uid** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "8"
  ],
  "default": "8"
}
```
- **token** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "333"
  ],
  "default": "333"
}
```
- **id** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "1"
  ],
  "default": "1"
}
```

### **DELETE** - /api/admin/type

#### CURL

```sh
curl -X DELETE "https://admin.gene.xluyun.com/api/admin/type\
?uid=8&token=333&id=2" \
    -H "Content-Type: application/json; charset=utf-8" \
    --data-raw "$body"
```

#### Query Parameters

- **uid** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "8"
  ],
  "default": "8"
}
```
- **token** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "333"
  ],
  "default": "333"
}
```
- **id** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "2"
  ],
  "default": "2"
}
```

#### Header Parameters

- **Content-Type** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "application/json; charset=utf-8"
  ],
  "default": "application/json; charset=utf-8"
}
```

#### Body Parameters

- **body** should respect the following schema:

```
{
  "type": "string",
  "default": "{}"
}
```

### **GET** - /api/admin/type/list

#### CURL

```sh
curl -X GET "https://admin.gene.xluyun.com/api/admin/type/list\
?uid=8&token=333" \
    -H "Content-Type: application/json; charset=utf-8" \
    --data-raw "$body"
```

#### Query Parameters

- **uid** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "8"
  ],
  "default": "8"
}
```
- **token** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "333"
  ],
  "default": "333"
}
```

#### Header Parameters

- **Content-Type** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "application/json; charset=utf-8"
  ],
  "default": "application/json; charset=utf-8"
}
```

#### Body Parameters

- **body** should respect the following schema:

```
{
  "type": "string",
  "default": "{}"
}
```

### **GET** - /api/weapp/type/list

#### CURL

```sh
curl -X GET "https://admin.gene.xluyun.com/api/weapp/type/list\
?uid=8&token=333" \
    -H "Content-Type: application/json; charset=utf-8" \
    --data-raw "$body"
```

#### Query Parameters

- **uid** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "8"
  ],
  "default": "8"
}
```
- **token** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "333"
  ],
  "default": "333"
}
```

#### Header Parameters

- **Content-Type** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "application/json; charset=utf-8"
  ],
  "default": "application/json; charset=utf-8"
}
```

#### Body Parameters

- **body** should respect the following schema:

```
{
  "type": "string",
  "default": "{}"
}
```

### **PUT** - /api/admin/type

#### CURL

```sh
curl -X PUT "https://admin.gene.xluyun.com/api/admin/type\
?uid=8&token=333" \
    -H "Content-Type: application/json; charset=utf-8" \
    --data-raw "$body"
```

#### Query Parameters

- **uid** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "8"
  ],
  "default": "8"
}
```
- **token** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "333"
  ],
  "default": "333"
}
```

#### Header Parameters

- **Content-Type** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "application/json; charset=utf-8"
  ],
  "default": "application/json; charset=utf-8"
}
```

#### Body Parameters

- **body** should respect the following schema:

```
{
  "type": "string",
  "default": "{\"address_name\":\"\\u738b\\u8fdb\\u559c4\",\"address_phone\":\"15300000000\",\"address_district\":\"\\u4e0a\\u6d77\\u5e02 \\u6768\\u6d66\\u533a\",\"address_location\":\"\\u56db\\u5e73\\u8def1239\\u53f7\\u540c\\u6d4e\\u5927\\u5b66\",\"id\":2,\"is_default\":1}"
}
```

### **POST** - /api/admin/good/checkitem

#### CURL

```sh
curl -X POST "https://admin.gene.xluyun.com/api/admin/good/checkitem\
?aid=1&token=333" \
    -H "Content-Type: application/json; charset=utf-8" \
    --data-raw "$body"
```

#### Query Parameters

- **aid** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "1"
  ],
  "default": "1"
}
```
- **token** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "333"
  ],
  "default": "333"
}
```

#### Header Parameters

- **Content-Type** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "application/json; charset=utf-8"
  ],
  "default": "application/json; charset=utf-8"
}
```

#### Body Parameters

- **body** should respect the following schema:

```
{
  "type": "string",
  "default": "{\"gid\":1,\"cid\":6}"
}
```

### **DELETE** - /api/admin/good/checkitem

#### CURL

```sh
curl -X DELETE "https://admin.gene.xluyun.com/api/admin/good/checkitem\
?uid=8&token=333&gid=1&cid=6" \
    -H "Content-Type: application/json; charset=utf-8" \
    --data-raw "$body"
```

#### Query Parameters

- **uid** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "8"
  ],
  "default": "8"
}
```
- **token** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "333"
  ],
  "default": "333"
}
```
- **gid** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "1"
  ],
  "default": "1"
}
```
- **cid** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "6"
  ],
  "default": "6"
}
```

#### Header Parameters

- **Content-Type** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "application/json; charset=utf-8"
  ],
  "default": "application/json; charset=utf-8"
}
```

#### Body Parameters

- **body** should respect the following schema:

```
{
  "type": "string",
  "default": "{}"
}
```

### **POST** - /api/weapp/cart

#### CURL

```sh
curl -X POST "https://admin.gene.xluyun.com/api/weapp/cart\
?uid=8&token=333" \
    -H "Content-Type: application/json; charset=utf-8" \
    --data-raw "$body"
```

#### Query Parameters

- **uid** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "8"
  ],
  "default": "8"
}
```
- **token** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "333"
  ],
  "default": "333"
}
```

#### Header Parameters

- **Content-Type** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "application/json; charset=utf-8"
  ],
  "default": "application/json; charset=utf-8"
}
```

#### Body Parameters

- **body** should respect the following schema:

```
{
  "type": "string",
  "default": "{\"gid\":1,\"count\":1}"
}
```

### **GET** - /api/weapp/cart

#### CURL

```sh
curl -X GET "https://admin.gene.xluyun.com/api/weapp/cart\
?uid=8&token=333"
```

#### Query Parameters

- **uid** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "8"
  ],
  "default": "8"
}
```
- **token** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "333"
  ],
  "default": "333"
}
```

### **GET** - /api/weapp/good

#### CURL

```sh
curl -X GET "https://admin.gene.xluyun.com/api/weapp/good\
?uid=8&token=333&id=4&detail=true"
```

#### Query Parameters

- **uid** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "8"
  ],
  "default": "8"
}
```
- **token** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "333"
  ],
  "default": "333"
}
```
- **id** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "4"
  ],
  "default": "4"
}
```
- **detail** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "true"
  ],
  "default": "true"
}
```

### **DELETE** - /api/admin/good

#### CURL

```sh
curl -X DELETE "https://admin.gene.xluyun.com/api/admin/good\
?uid=8&token=333&id=2" \
    -H "Content-Type: application/json; charset=utf-8" \
    --data-raw "$body"
```

#### Query Parameters

- **uid** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "8"
  ],
  "default": "8"
}
```
- **token** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "333"
  ],
  "default": "333"
}
```
- **id** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "2"
  ],
  "default": "2"
}
```

#### Header Parameters

- **Content-Type** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "application/json; charset=utf-8"
  ],
  "default": "application/json; charset=utf-8"
}
```

#### Body Parameters

- **body** should respect the following schema:

```
{
  "type": "string",
  "default": "{}"
}
```

### **GET** - /api/admin/good/list

#### CURL

```sh
curl -X GET "https://admin.gene.xluyun.com/api/admin/good/list\
?uid=8&token=333" \
    -H "Content-Type: application/json; charset=utf-8" \
    --data-raw "$body"
```

#### Query Parameters

- **uid** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "8"
  ],
  "default": "8"
}
```
- **token** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "333"
  ],
  "default": "333"
}
```

#### Header Parameters

- **Content-Type** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "application/json; charset=utf-8"
  ],
  "default": "application/json; charset=utf-8"
}
```

#### Body Parameters

- **body** should respect the following schema:

```
{
  "type": "string",
  "default": "{}"
}
```

### **PUT** - /api/admin/good

#### CURL

```sh
curl -X PUT "https://admin.gene.xluyun.com/api/admin/good\
?uid=8&token=333" \
    -H "Content-Type: application/json; charset=utf-8" \
    --data-raw "$body"
```

#### Query Parameters

- **uid** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "8"
  ],
  "default": "8"
}
```
- **token** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "333"
  ],
  "default": "333"
}
```

#### Header Parameters

- **Content-Type** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "application/json; charset=utf-8"
  ],
  "default": "application/json; charset=utf-8"
}
```

#### Body Parameters

- **body** should respect the following schema:

```
{
  "type": "string",
  "default": "{\"name\":\"\\u4e00\\u4e2a\\u6539\\u8fc7\\u540d\\u7684\\u5546\\u54c1\",\"id\":2}"
}
```

### **POST** - /api/admin/good

#### CURL

```sh
curl -X POST "https://admin.gene.xluyun.com/api/admin/good\
?aid=1&token=333" \
    -H "Content-Type: application/json; charset=utf-8" \
    --data-raw "$body"
```

#### Query Parameters

- **aid** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "1"
  ],
  "default": "1"
}
```
- **token** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "333"
  ],
  "default": "333"
}
```

#### Header Parameters

- **Content-Type** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "application/json; charset=utf-8"
  ],
  "default": "application/json; charset=utf-8"
}
```

#### Body Parameters

- **body** should respect the following schema:

```
{
  "type": "string",
  "default": "{\"tid\":1,\"name\":\"\\u975e\\u5e38\\u9ad8\\u7ea7\\u7684\\u5546\\u54c1\",\"price\":12.33,\"icon\":\"http://www.baidu.com\",\"images\":\"http://www.baidu.com,http://www.baidu.com\",\"tip\":\"default tip\",\"attribute\":\"default attribute\",\"content\":\"default content\",\"checkitems\":[6,8]}"
}
```

### **GET** - /api/admin/good

#### CURL

```sh
curl -X GET "https://admin.gene.xluyun.com/api/admin/good\
?aid=8&token=333&id=4&detail=true"
```

#### Query Parameters

- **aid** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "8"
  ],
  "default": "8"
}
```
- **token** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "333"
  ],
  "default": "333"
}
```
- **id** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "4"
  ],
  "default": "4"
}
```
- **detail** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "true"
  ],
  "default": "true"
}
```

### **GET** - /api/weapp/good

#### CURL

```sh
curl -X GET "https://admin.gene.xluyun.com/api/weapp/good\
?uid=8&token=333&id=4&detail=true"
```

#### Query Parameters

- **uid** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "8"
  ],
  "default": "8"
}
```
- **token** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "333"
  ],
  "default": "333"
}
```
- **id** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "4"
  ],
  "default": "4"
}
```
- **detail** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "true"
  ],
  "default": "true"
}
```

### **DELETE** - /api/admin/good

#### CURL

```sh
curl -X DELETE "https://admin.gene.xluyun.com/api/admin/good\
?uid=8&token=333&id=2" \
    -H "Content-Type: application/json; charset=utf-8" \
    --data-raw "$body"
```

#### Query Parameters

- **uid** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "8"
  ],
  "default": "8"
}
```
- **token** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "333"
  ],
  "default": "333"
}
```
- **id** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "2"
  ],
  "default": "2"
}
```

#### Header Parameters

- **Content-Type** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "application/json; charset=utf-8"
  ],
  "default": "application/json; charset=utf-8"
}
```

#### Body Parameters

- **body** should respect the following schema:

```
{
  "type": "string",
  "default": "{}"
}
```

### **GET** - /api/admin/good/list

#### CURL

```sh
curl -X GET "https://admin.gene.xluyun.com/api/admin/good/list\
?uid=8&token=333" \
    -H "Content-Type: application/json; charset=utf-8" \
    --data-raw "$body"
```

#### Query Parameters

- **uid** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "8"
  ],
  "default": "8"
}
```
- **token** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "333"
  ],
  "default": "333"
}
```

#### Header Parameters

- **Content-Type** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "application/json; charset=utf-8"
  ],
  "default": "application/json; charset=utf-8"
}
```

#### Body Parameters

- **body** should respect the following schema:

```
{
  "type": "string",
  "default": "{}"
}
```

### **PUT** - /api/admin/good

#### CURL

```sh
curl -X PUT "https://admin.gene.xluyun.com/api/admin/good\
?uid=8&token=333" \
    -H "Content-Type: application/json; charset=utf-8" \
    --data-raw "$body"
```

#### Query Parameters

- **uid** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "8"
  ],
  "default": "8"
}
```
- **token** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "333"
  ],
  "default": "333"
}
```

#### Header Parameters

- **Content-Type** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "application/json; charset=utf-8"
  ],
  "default": "application/json; charset=utf-8"
}
```

#### Body Parameters

- **body** should respect the following schema:

```
{
  "type": "string",
  "default": "{\"name\":\"\\u4e00\\u4e2a\\u6539\\u8fc7\\u540d\\u7684\\u5546\\u54c1\",\"id\":2}"
}
```

### **POST** - /api/admin/company

#### CURL

```sh
curl -X POST "https://admin.gene.xluyun.com/api/admin/company\
?aid=1&token=333" \
    -H "Content-Type: application/json; charset=utf-8" \
    --data-raw "$body"
```

#### Query Parameters

- **aid** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "1"
  ],
  "default": "1"
}
```
- **token** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "333"
  ],
  "default": "333"
}
```

#### Header Parameters

- **Content-Type** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "application/json; charset=utf-8"
  ],
  "default": "application/json; charset=utf-8"
}
```

#### Body Parameters

- **body** should respect the following schema:

```
{
  "type": "string",
  "default": "{\"name\":\"\\u817e\\u8baf\\u79d1\\u6280\"}"
}
```

### **GET** - /api/admin/company

#### CURL

```sh
curl -X GET "https://admin.gene.xluyun.com/api/admin/company\
?aid=8&token=333&id=2&detail=true"
```

#### Query Parameters

- **aid** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "8"
  ],
  "default": "8"
}
```
- **token** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "333"
  ],
  "default": "333"
}
```
- **id** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "2"
  ],
  "default": "2"
}
```
- **detail** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "true"
  ],
  "default": "true"
}
```

### **DELETE** - /api/admin/company

#### CURL

```sh
curl -X DELETE "https://admin.gene.xluyun.com/api/admin/company\
?uid=8&token=333&id=2" \
    -H "Content-Type: application/json; charset=utf-8" \
    --data-raw "$body"
```

#### Query Parameters

- **uid** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "8"
  ],
  "default": "8"
}
```
- **token** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "333"
  ],
  "default": "333"
}
```
- **id** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "2"
  ],
  "default": "2"
}
```

#### Header Parameters

- **Content-Type** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "application/json; charset=utf-8"
  ],
  "default": "application/json; charset=utf-8"
}
```

#### Body Parameters

- **body** should respect the following schema:

```
{
  "type": "string",
  "default": "{}"
}
```

### **GET** - /api/admin/company/list

#### CURL

```sh
curl -X GET "https://admin.gene.xluyun.com/api/admin/company/list\
?uid=8&token=333" \
    -H "Content-Type: application/json; charset=utf-8" \
    --data-raw "$body"
```

#### Query Parameters

- **uid** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "8"
  ],
  "default": "8"
}
```
- **token** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "333"
  ],
  "default": "333"
}
```

#### Header Parameters

- **Content-Type** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "application/json; charset=utf-8"
  ],
  "default": "application/json; charset=utf-8"
}
```

#### Body Parameters

- **body** should respect the following schema:

```
{
  "type": "string",
  "default": "{}"
}
```

### **PUT** - /api/admin/company

#### CURL

```sh
curl -X PUT "https://admin.gene.xluyun.com/api/admin/company\
?uid=8&token=333" \
    -H "Content-Type: application/json; charset=utf-8" \
    --data-raw "$body"
```

#### Query Parameters

- **uid** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "8"
  ],
  "default": "8"
}
```
- **token** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "333"
  ],
  "default": "333"
}
```

#### Header Parameters

- **Content-Type** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "application/json; charset=utf-8"
  ],
  "default": "application/json; charset=utf-8"
}
```

#### Body Parameters

- **body** should respect the following schema:

```
{
  "type": "string",
  "default": "{\"name\":\"\\u4eac\\u4e1c\\u652f\\u4ed8\",\"id\":2}"
}
```

### **POST** - /api/admin/company/admin

#### CURL

```sh
curl -X POST "https://admin.gene.xluyun.com/api/admin/company/admin\
?aid=1&token=333" \
    -H "Content-Type: application/json; charset=utf-8" \
    --data-raw "$body"
```

#### Query Parameters

- **aid** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "1"
  ],
  "default": "1"
}
```
- **token** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "333"
  ],
  "default": "333"
}
```

#### Header Parameters

- **Content-Type** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "application/json; charset=utf-8"
  ],
  "default": "application/json; charset=utf-8"
}
```

#### Body Parameters

- **body** should respect the following schema:

```
{
  "type": "string",
  "default": "{\"company\":2,\"username\":\"tencent\",\"password\":\"tencent\"}"
}
```

### **GET** - /api/admin/company/admin

#### CURL

```sh
curl -X GET "https://admin.gene.xluyun.com/api/admin/company/admin\
?aid=8&token=333&id=1&detail=true"
```

#### Query Parameters

- **aid** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "8"
  ],
  "default": "8"
}
```
- **token** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "333"
  ],
  "default": "333"
}
```
- **id** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "1"
  ],
  "default": "1"
}
```
- **detail** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "true"
  ],
  "default": "true"
}
```

### **DELETE** - /api/admin/company/admin

#### CURL

```sh
curl -X DELETE "https://admin.gene.xluyun.com/api/admin/company/admin\
?uid=8&token=333&id=2" \
    -H "Content-Type: application/json; charset=utf-8" \
    --data-raw "$body"
```

#### Query Parameters

- **uid** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "8"
  ],
  "default": "8"
}
```
- **token** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "333"
  ],
  "default": "333"
}
```
- **id** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "2"
  ],
  "default": "2"
}
```

#### Header Parameters

- **Content-Type** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "application/json; charset=utf-8"
  ],
  "default": "application/json; charset=utf-8"
}
```

#### Body Parameters

- **body** should respect the following schema:

```
{
  "type": "string",
  "default": "{}"
}
```

### **GET** - /api/admin/company/admin/list

#### CURL

```sh
curl -X GET "https://admin.gene.xluyun.com/api/admin/company/admin/list\
?uid=8&token=333&company=2" \
    -H "Content-Type: application/json; charset=utf-8" \
    --data-raw "$body"
```

#### Query Parameters

- **uid** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "8"
  ],
  "default": "8"
}
```
- **token** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "333"
  ],
  "default": "333"
}
```
- **company** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "2"
  ],
  "default": "2"
}
```

#### Header Parameters

- **Content-Type** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "application/json; charset=utf-8"
  ],
  "default": "application/json; charset=utf-8"
}
```

#### Body Parameters

- **body** should respect the following schema:

```
{
  "type": "string",
  "default": "{}"
}
```

### **PUT** - /api/admin/company/admin

#### CURL

```sh
curl -X PUT "https://admin.gene.xluyun.com/api/admin/company/admin\
?uid=8&token=333" \
    -H "Content-Type: application/json; charset=utf-8" \
    --data-raw "$body"
```

#### Query Parameters

- **uid** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "8"
  ],
  "default": "8"
}
```
- **token** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "333"
  ],
  "default": "333"
}
```

#### Header Parameters

- **Content-Type** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "application/json; charset=utf-8"
  ],
  "default": "application/json; charset=utf-8"
}
```

#### Body Parameters

- **body** should respect the following schema:

```
{
  "type": "string",
  "default": "{\"password\":\"tencent1\",\"id\":1}"
}
```

### **POST** - /api/weapp/address

#### CURL

```sh
curl -X POST "https://admin.gene.xluyun.com/api/weapp/address\
?uid=8&token=333" \
    -H "Content-Type: application/json; charset=utf-8" \
    --data-raw "$body"
```

#### Query Parameters

- **uid** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "8"
  ],
  "default": "8"
}
```
- **token** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "333"
  ],
  "default": "333"
}
```

#### Header Parameters

- **Content-Type** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "application/json; charset=utf-8"
  ],
  "default": "application/json; charset=utf-8"
}
```

#### Body Parameters

- **body** should respect the following schema:

```
{
  "type": "string",
  "default": "{\"address_name\":\"\\u738b\\u8fdb\\u559c\",\"address_phone\":\"15300000000\",\"address_district\":\"\\u4e0a\\u6d77\\u5e02 \\u6768\\u6d66\\u533a\",\"address_location\":\"\\u56db\\u5e73\\u8def1239\\u53f7\\u540c\\u6d4e\\u5927\\u5b66\"}"
}
```

### **GET** - /api/weapp/address

#### CURL

```sh
curl -X GET "https://admin.gene.xluyun.com/api/weapp/address\
?uid=8&token=333&id=1"
```

#### Query Parameters

- **uid** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "8"
  ],
  "default": "8"
}
```
- **token** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "333"
  ],
  "default": "333"
}
```
- **id** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "1"
  ],
  "default": "1"
}
```

### **DELETE** - /api/weapp/address

#### CURL

```sh
curl -X DELETE "https://admin.gene.xluyun.com/api/weapp/address\
?uid=8&token=333&id=2" \
    -H "Content-Type: application/json; charset=utf-8" \
    --data-raw "$body"
```

#### Query Parameters

- **uid** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "8"
  ],
  "default": "8"
}
```
- **token** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "333"
  ],
  "default": "333"
}
```
- **id** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "2"
  ],
  "default": "2"
}
```

#### Header Parameters

- **Content-Type** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "application/json; charset=utf-8"
  ],
  "default": "application/json; charset=utf-8"
}
```

#### Body Parameters

- **body** should respect the following schema:

```
{
  "type": "string",
  "default": "{}"
}
```

### **GET** - /api/weapp/address/list

#### CURL

```sh
curl -X GET "https://admin.gene.xluyun.com/api/weapp/address/list\
?uid=8&token=333" \
    -H "Content-Type: application/json; charset=utf-8" \
    --data-raw "$body"
```

#### Query Parameters

- **uid** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "8"
  ],
  "default": "8"
}
```
- **token** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "333"
  ],
  "default": "333"
}
```

#### Header Parameters

- **Content-Type** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "application/json; charset=utf-8"
  ],
  "default": "application/json; charset=utf-8"
}
```

#### Body Parameters

- **body** should respect the following schema:

```
{
  "type": "string",
  "default": "{}"
}
```

### **PUT** - /api/weapp/address

#### CURL

```sh
curl -X PUT "https://admin.gene.xluyun.com/api/weapp/address\
?uid=8&token=333" \
    -H "Content-Type: application/json; charset=utf-8" \
    --data-raw "$body"
```

#### Query Parameters

- **uid** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "8"
  ],
  "default": "8"
}
```
- **token** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "333"
  ],
  "default": "333"
}
```

#### Header Parameters

- **Content-Type** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "application/json; charset=utf-8"
  ],
  "default": "application/json; charset=utf-8"
}
```

#### Body Parameters

- **body** should respect the following schema:

```
{
  "type": "string",
  "default": "{\"address_name\":\"\\u738b\\u8fdb\\u559c4\",\"address_phone\":\"15300000000\",\"address_district\":\"\\u4e0a\\u6d77\\u5e02 \\u6768\\u6d66\\u533a\",\"address_location\":\"\\u56db\\u5e73\\u8def1239\\u53f7\\u540c\\u6d4e\\u5927\\u5b66\",\"id\":2,\"is_default\":1}"
}
```

### **POST** - /api/weapp/userinfo

#### CURL

```sh
curl -X POST "https://admin.gene.xluyun.com/api/weapp/userinfo\
?uid=1&token=333" \
    -H "Content-Type: application/json; charset=utf-8" \
    --data-raw "$body"
```

#### Query Parameters

- **uid** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "1"
  ],
  "default": "1"
}
```
- **token** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "333"
  ],
  "default": "333"
}
```

#### Header Parameters

- **Content-Type** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "application/json; charset=utf-8"
  ],
  "default": "application/json; charset=utf-8"
}
```

#### Body Parameters

- **body** should respect the following schema:

```
{
  "type": "string",
  "default": "{\"checker_name\":\"\\u738b\\u8fdb\\u559c\",\"checker_gender\":1,\"checker_birthday\":\"2016-03-03\",\"checker_location\":\"\\u4e0a\\u6d77\\u5e02\",\"checker_has_smoking_history\":1,\"checker_has_medical_history\":1,\"checker_medical_history\":\"\\u5fc3\\u810f\\u75c5\"}"
}
```

### **GET** - /api/weapp/userinfo

#### CURL

```sh
curl -X GET "https://admin.gene.xluyun.com/api/weapp/userinfo\
?uid=1&token=333&id=1" \
    -H "Content-Type: application/json; charset=utf-8" \
    --data-raw "$body"
```

#### Query Parameters

- **uid** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "1"
  ],
  "default": "1"
}
```
- **token** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "333"
  ],
  "default": "333"
}
```
- **id** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "1"
  ],
  "default": "1"
}
```

#### Header Parameters

- **Content-Type** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "application/json; charset=utf-8"
  ],
  "default": "application/json; charset=utf-8"
}
```

#### Body Parameters

- **body** should respect the following schema:

```
{
  "type": "string",
  "default": "{}"
}
```

### **DELETE** - /api/weapp/userinfo

#### CURL

```sh
curl -X DELETE "https://admin.gene.xluyun.com/api/weapp/userinfo\
?uid=1&token=333&id=2" \
    -H "Content-Type: application/json; charset=utf-8" \
    --data-raw "$body"
```

#### Query Parameters

- **uid** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "1"
  ],
  "default": "1"
}
```
- **token** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "333"
  ],
  "default": "333"
}
```
- **id** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "2"
  ],
  "default": "2"
}
```

#### Header Parameters

- **Content-Type** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "application/json; charset=utf-8"
  ],
  "default": "application/json; charset=utf-8"
}
```

#### Body Parameters

- **body** should respect the following schema:

```
{
  "type": "string",
  "default": "{}"
}
```

### **GET** - /api/weapp/userinfo/list

#### CURL

```sh
curl -X GET "https://admin.gene.xluyun.com/api/weapp/userinfo/list\
?uid=1&token=333" \
    -H "Content-Type: application/json; charset=utf-8" \
    --data-raw "$body"
```

#### Query Parameters

- **uid** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "1"
  ],
  "default": "1"
}
```
- **token** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "333"
  ],
  "default": "333"
}
```

#### Header Parameters

- **Content-Type** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "application/json; charset=utf-8"
  ],
  "default": "application/json; charset=utf-8"
}
```

#### Body Parameters

- **body** should respect the following schema:

```
{
  "type": "string",
  "default": "{}"
}
```

### **GET** - /api/admin/userinfo/list

#### CURL

```sh
curl -X GET "https://admin.gene.xluyun.com/api/admin/userinfo/list\
?uid=1&token=333&aid=1" \
    -H "Content-Type: application/json; charset=utf-8" \
    --data-raw "$body"
```

#### Query Parameters

- **uid** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "1"
  ],
  "default": "1"
}
```
- **token** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "333"
  ],
  "default": "333"
}
```
- **aid** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "1"
  ],
  "default": "1"
}
```

#### Header Parameters

- **Content-Type** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "application/json; charset=utf-8"
  ],
  "default": "application/json; charset=utf-8"
}
```

#### Body Parameters

- **body** should respect the following schema:

```
{
  "type": "string",
  "default": "{}"
}
```

### **PUT** - /api/weapp/userinfo

#### CURL

```sh
curl -X PUT "https://admin.gene.xluyun.com/api/weapp/userinfo\
?uid=1&token=333" \
    -H "Content-Type: application/json; charset=utf-8" \
    --data-raw "$body"
```

#### Query Parameters

- **uid** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "1"
  ],
  "default": "1"
}
```
- **token** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "333"
  ],
  "default": "333"
}
```

#### Header Parameters

- **Content-Type** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "application/json; charset=utf-8"
  ],
  "default": "application/json; charset=utf-8"
}
```

#### Body Parameters

- **body** should respect the following schema:

```
{
  "type": "string",
  "default": "{\"checker_name\":\"\\u738b\\u8fdb\\u559c\",\"checker_gender\":1,\"checker_birthday\":\"2016-03-03\",\"checker_location\":\"\\u4e0a\\u6d77\\u5e02\",\"checker_has_smoking_history\":1,\"checker_has_medical_history\":1,\"checker_medical_history\":\"\\u5fc3\\u810f\\u75c51\",\"id\":\"1\"}"
}
```

## References

