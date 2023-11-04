## Описание HTTP-сообщений
# Acivities
**ОР** = "Ожидаемый результат"

### GET Тест 10 - Проверка корректности кода 

URL: "https://fakerestapi.azurewebsites.net/api/v1/Activities"    
**ОР**: выполнен запрос, код ответа 200  

**Заголовки запроса**:  
User-Agent: PostmanRuntime/7.33.0  
Accept: \*/\*  
Postman-Token: c113d5ec-961b-4c78-9468-8f93a70c0a8b  
Host: fakerestapi.azurewebsites.net   
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  

**Заголовки ответа**:  
Content-Length: 0  
Connection: close  
Date: Mon, 25 Sep 2023 07:16:27 GMT

****

### GET Тест 11 - Проверка нагрузки ответа  
URL: "https://fakerestapi.azurewebsites.net/api/v1/Activities"    
**ОР**: выполнен запрос, код ответа 200  

**Заголовки запроса**:  
User-Agent: PostmanRuntime/7.33.0  
Accept: \*/\*  
Postman-Token: 23001923-d2cb-4292-9409-cc9ecbdaa8c3 
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive    

**Заголовки ответа**  
Content-Type: application/json; charset=utf-8; v=1.0    
Date: Mon, 25 Sep 2023 07:29:19 GMT   
Server: Kestrel   
Transfer-Encoding: chunked   
api-supported-versions: 1.0   
****

### GET Тест 12 - Проверка заголовков ответа

URL: "https://fakerestapi.azurewebsites.net/api/v1/Activities" 

**ОР**: Ответ своевременный, получены заголовки согласно спецификации, не содержится заголовок "X-Powered-By"  

**Заголовки запроса**  
User-Agent: PostmanRuntime/7.33.0    
Accept: \*/\*    
Postman-Token: 6fde750a-de85-42e5-8e41-4575a297adcf  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  

**Заголовки ответа**  
Content-Type: application/json; charset=utf-8; v=1.0  
Date: Mon, 25 Sep 2023 07:38:18 GMT  
Server: Kestrel  
Transfer-Encoding: chunked  
api-supported-versions: 1.0  
****
### GET Тест 14 - Получение списка активностей 

URL: "https://fakerestapi.azurewebsites.net/api/v1/Activities"   
**ОР**: получен список сущностей, код ответа 200  

**Заголовки зароса**:  
User-Agent: PostmanRuntime/7.33.0  
Accept: \*/\*  
Postman-Token: e8c03ddc-22e2-4e75-a972-7b6c7af6e3ed  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive 

**Заголовки ответа**:  
Content-Type: application/json; charset=utf-8; v=1.0  
Date: Mon, 25 Sep 2023 07:23:05 GMT  
Server: Kestrel  
Transfer-Encoding: chunked
api-supported-versions: 1.0  

Тело ответа:  
```
{
        "id": 3,
        "title": "Activity 3",
        "dueDate": "2023-09-24T05:56:13.4654534+00:00",
        "completed": false
    },
    {
        "id": 4,
        "title": "Activity 4",
        "dueDate": "2023-09-24T06:56:13.4654536+00:00",
        "completed": true
    },
    {
        "id": 5,
        "title": "Activity 5",
        "dueDate": "2023-09-24T07:56:13.4654539+00:00",
        "completed": false
    }
```
****

### GET Тест 18 - Получение списка активностей неверным методом  

URL: "https://fakerestapi.azurewebsites.net/api/v1/Activities"  
**ОР**: список методом OPTIONS не получен, код 405 "Method Not Allowed"  

**Заголовки зароса**:
User-Agent: PostmanRuntime/7.33.0 
Accept: \*/\*    
Postman-Token: 6e7f4640-7113-4ffd-bf9c-07889fb9cf0b    
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive    

 **Заголовки ответа**  
Content-Length: 0  
Date: Mon, 25 Sep 2023 08:10:28 GMT  
Server: Kestrel  
Allow: GET, POST  
*****

### POST Тест 19 - Отправление новых активностей

URL: "https://fakerestapi.azurewebsites.net/api/v1/Activities"  
**ОР**: новая сущность создана, код 201   

**Заголовки запроса**:  
Content-Type: application/json
User-Agent: PostmanRuntime/7.33.0
Accept: \*/\*
Postman-Token: 8edf4d41-49b1-4ff3-8418-afae46b0bcb4
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
Content-Length: 102

**Тело запроса**:  
```
{
  "id": {{activity_id}},
  "title": "string",
  "dueDate": "2023-09-22T05:54:10.236Z",
  "completed": true
}
```

**Заголовки ответа**:  
Content-Type: application/json; charset=utf-8; v=1.0
Date: Mon, 25 Sep 2023 08:17:15 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0 

**Тело ответа**:  
```
{
    "id": 33,
    "title": "string",
    "dueDate": "2023-09-22T05:54:10.236Z",
    "completed": true
}
```
****
### POST Тест 22 - Проверка нагрузки ответа  
URL: "https://fakerestapi.azurewebsites.net/api/v1/Activities"  

**ОР**: ответ своевременный, содержит данные в формате JSON, без ошибок, заголовки согласно спецификации

**Заголовки запроса**:  
Content-Type: application/json  
User-Agent: PostmanRuntime/7.33.0  
Accept: \*/\*  
Postman-Token: 48237dd9-be66-45e9-9201-a21a7b00517b 
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  
Content-Length: 102  

**Тело запроса**:
```
{
  "id": {{activity_id}},
  "title": "string",
  "dueDate": "2023-09-22T05:54:10.236Z",
  "completed": true
}
```
**Заголовки ответа**:
Content-Type: application/json; charset=utf-8; v=1.0  
Date: Mon, 25 Sep 2023 18:59:06 GMT  
Server: Kestrel  
Transfer-Encoding: chunked  
api-supported-versions: 1.0  

**Тело ответа:**
```
{
    "id": 33,
    "title": "string",
    "dueDate": "2023-09-22T05:54:10.236Z",
    "completed": true
}
```
*****
### POST Тест 23 - Проверка заголовков ответа  
URL: "https://fakerestapi.azurewebsites.net/api/v1/Activities"  

**ОР**: получены заголовки согласно спецификации, не содержится заголовок "X-Powered-By"  

 **Заголовки запроса**:  
 Content-Type: application/json  
User-Agent: PostmanRuntime/7.33.0  
Accept: \*/\*  
Postman-Token: 76b1b832-1e44-45ea-9b57-df196dae8fbd  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  
Content-Length: 110    

**Тело запроса:**  
```
{
    "id": {{activity_id}},
    "title": "string",
    "dueDate": "2023-09-22T05:54:10.236Z",
    "completed": true
}
```  

**Заголовки ответа:**  
Content-Type: application/json; charset=utf-8; v=1.0  
Date: Mon, 25 Sep 2023 08:35:12 GMT  
Server: Kestrel   
Transfer-Encoding: chunked  
api-supported-versions: 1.0  

**Тело ответа:**  
```
{
    "id": 33,
    "title": "string",
    "dueDate": "2023-09-22T05:54:10.236Z",
    "completed": true
}
```
*****
### POST Тест 25 - Создание новой активности с неверными данными 
URL: "https://fakerestapi.azurewebsites.net/api/v1/Activities" 

**ОР**:  Новая сущность не создана, код 400

**Заголовки запроса**:  
Content-Type: application/json  
User-Agent: PostmanRuntime/7.33.0  
Accept: \*/\*    
Postman-Token: aca8390c-00bb-4665-8b2b-f7059ac38d06  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  
Content-Length: 100   

**Тело запроса**:
```
{
  "id": ,
  "title": "string",
  "dueDate": "2023-09-22T05:54:10.236Z",
  "completed": true
}
``` 
**Заголовки ответа**:  
Content-Length: 0  
Date: Mon, 25 Sep 2023 09:11:01 GMT  
Server: Kestrel  
******
### POST Тест 26 - Создание новой активности неверным методом

URL: "https://fakerestapi.azurewebsites.net/api/v1/Activities"  
**ОР**: Новая сущность методом PATCH не создана, ответ 405  

**Заголовки запроса**:  
Content-Type: application/json  
User-Agent: PostmanRuntime/7.33.0  
Accept: \*/\*  
Postman-Token: 866ba14d-4f2a-467f-afe6-18c4de8633a2  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br   
Connection: keep-alive  
Content-Length: 102  

**Тело запроса**:  
```
{
  "id": {{activity_id}},
  "title": "string",
  "dueDate": "2023-09-22T05:54:10.236Z",
  "completed": true
}
```

**Заголовки ответа**:  

Content-Length: 0  
Date: Mon, 25 Sep 2023 08:31:03 GMT  
Server: Kestrel  
Allow: GET, POST  
****

### GET Тест 27 - Получение списка созданных сущностей по id. 

URL: "https://fakerestapi.azurewebsites.net/api/v1/Activities/33"   
**ОР**: в ответе получена созданная сущность c новым id, код ответа 200 

**Заголовки запроса**:  
User-Agent: PostmanRuntime/7.33.0
Accept: \*/\*
Postman-Token: 72ea9144-35f3-4bf0-9bcf-f6ea001982e9
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Заголовки ответа**:  
Content-Type: application/json; charset=utf-8; v=1.0
Date: Mon, 25 Sep 2023 09:17:37 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0 

Тело ответа:  
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.4",
    "title": "Not Found",
    "status": 404,
    "traceId": "00-b5b6816be1168a408317103be10c35de-550db4f8e793e94d-00"
}
```
 *****

### GET Тест 28 - Получение списка активностей по неверному id
URL: "https://fakerestapi.azurewebsites.net/api/v1/Activities/5999999"   
**ОР**: ответ своевременный, сущность не получена, код 404  

**Заголовки запроса**:  
User-Agent: PostmanRuntime/7.33.0  
Accept: \*/\*  
Postman-Token: 34907e08-0873-46fa-9b95-6052b53205cf  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  

**Заголовки ответа**:  
Content-Type: application/problem+json; charset=utf-8; v=1.0  
Date: Mon, 25 Sep 2023 09:23:36 GMT  
Server: Kestrel  
Transfer-Encoding: chunked  
api-supported-versions: 1.0  
******
### GET Тест 29 - Получение списка активностей по id неверным методом
URL: "https://fakerestapi.azurewebsites.net/api/v1/Activities/8"    
**ОР**: методом PATCH ответ не получен, ошибка 405 

**Заголовки запроса:**  
User-Agent: PostmanRuntime/7.33.0  
Accept: \*/\*  
Postman-Token: 9313b681-6607-4954-bede-7308eef7fc11  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  
Content-Length: 0  

**Заголовки ответа:**
Content-Length: 0   
Date: Mon, 25 Sep 2023 09:30:29 GMT  
Server: Kestrel  
Allow: DELETE, GET, PUT    
******

### POST Тест 30 - Создание новых активностей - дублирование 
URL: "https://fakerestapi.azurewebsites.net/api/v1/Activities"   
**ОР**: дублированная сущность не создастся, код 409  

**Заголовки запроса**:
Content-Type: application/json  
User-Agent: PostmanRuntime/7.33.0  
Accept: \*/\*  
Postman-Token: 4b333b38-2b0d-45fe-a778-f7ab5fda2fad  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  
Content-Length: 101  

**Тело запроса:** 
```
{
  "id": {{activity8_id}},
  "title": "string",
  "dueDate": "2023-09-22T05:54:10.236Z",
  "completed": true
}
```

**Заголовки ответа:**
Content-Type: application/json; charset=utf-8; v=1.0  
Date: Mon, 25 Sep 2023 09:32:44 GMT  
Server: Kestrel  
Transfer-Encoding: chunked  
api-supported-versions: 1.0  
**Тело ответа:**  
```
{
    "id": 8,
    "title": "string",
    "dueDate": "2023-09-22T05:54:10.236Z",
    "completed": true
}
```
***** 
### POST Тест 31 - создание новой активности: неполная модель 
URL: "https://fakerestapi.azurewebsites.net/api/v1/Activities"  
**ОР**: новая сущность не создана, код 400

**Заголовки запроса**:  
Content-Type: application/json  
User-Agent: PostmanRuntime/7.33.0  
Accept: \*/\*  
Postman-Token: 7b41f94f-79e2-41f6-889d-89ef26fa1f73    
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  
Content-Length: 40  

**Тело запроса**:
```
{
  "dueDate": 
  "completed": true
}
```
**Заголовки ответа**:
Content-Type: application/problem+json; charset=utf-8  
Date: Mon, 25 Sep 2023 11:44:01 GMT  
Server: Kestrel  
Transfer-Encoding: chunked  

**Тело ответа:**
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-176e204cfe5b9f498f9e6214409aa73f-be4a5746f29ef74a-00",
    "errors": {
        "$.dueDate": [
            "The JSON value could not be converted to System.DateTime. Path: $.dueDate | LineNumber: 2 | BytePositionInLine: 13."
        ]
    }
}
```
*****
### GET Тест 33 - Проверка нагрузки ответа по id
URL: "https://fakerestapi.azurewebsites.net/api/v1/Activities/5"  
**ОР**: выполнен запрос, ответ содержит данные в формате JSON, без ошибок, заголовки согласно спецификации, код 200   код ответа 200  

**Заголовки запроса**:
User-Agent: PostmanRuntime/7.33.0  
Accept: \*/\*  
Postman-Token: 06955eec-1bfa-44f0-bb20-7b0c40652682 
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  

**Заголовки ответа**: 
Content-Type: application/json; charset=utf-8; v=1.0  
Date: Mon, 25 Sep 2023 18:13:28 GMT  
Server: Kestrel  
Transfer-Encoding: chunked  
api-supported-versions: 1.0  

**Тело ответа:**
```
{
    "id": 5,
    "title": "Activity 5",
    "dueDate": "2023-09-25T23:13:28.5032805+00:00",
    "completed": false
}
```
******
### GET Тест 34 - Проверка заголовков по id

URL: "https://fakerestapi.azurewebsites.net/api/v1/Activities/4"  

**ОР**: ответ своевременный, получены заголовки согласно спецификации, не содержится заголовок "X-Powered-By"  

 **Заголовки запроса**:
 User-Agent: PostmanRuntime/7.33.0  
Accept: \*/\*  
Postman-Token: ce7aa20a-6990-4f70-bc1f-86fb60f787d0  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br   
Connection: keep-alive  

**Заголовки ответа**:  
Content-Type: application/json; charset=utf-8; v=1.0  
Date: Mon, 25 Sep 2023 12:25:00 GMT  
Server: Kestrel    
Transfer-Encoding: chunked  
api-supported-versions: 1.0  

**Тело ответа**:
```
{
    "id":4,
    "title":"Activity 4",
    "dueDate":"2023-09-25T16:25:00.9000624+00:00",
    "completed":true
}
```
***** 
### PUT Тест 37 - Обновление списка активностей по id  
URL: "https://fakerestapi.azurewebsites.net/api/v1/Activities/15"  
**ОР**: ответ содержит обновленные данные сущности, код 200 

**Заголовки запроса**:
Content-Type: application/json  
User-Agent: PostmanRuntime/7.33.0  
Accept: \*/\*  
Postman-Token: b768ea5f-13e3-405c-a43c-a18177206b92  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  
Content-Length: 100  

**Тело запроса**:  
```
{
  "id": 15,
  "title": "read",
  "dueDate": "2023-09-22T05:54:10.236Z",
  "completed": true
}
```

**Заголовки ответа**:
Content-Type: application/json; charset=utf-8; v=1.0  
Date: Mon, 25 Sep 2023 18:47:22 GMT  
Server: Kestrel  
Transfer-Encoding: chunked  
api-supported-versions: 1.0  

**Тело ответа**:
```
{
    "id": 15,
    "title": "read",
    "dueDate": "2023-09-22T05:54:10.236Z",
    "completed": true
}
```
******
### PUT Тест 53 - Проверка корректности кода по id  

URL: "https://fakerestapi.azurewebsites.net/api/v1/Activities/3"  
**ОР**: запрос выполнен, код 200  

**Заголовки запроса**:  
Content-Type: application/json
User-Agent: PostmanRuntime/7.33.0
Accept: \*/\*
Postman-Token: a09f282a-a1f7-4b1c-a1d4-cb7a2b0e753f
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
Content-Length: 101  

**Тело запроса:**
```
{
  "id": 3,
  "title": "string",
  "dueDate": "2023-09-22T05:54:10.236Z",
  "completed": true
}
```
**Заголовки ответа:** 
Content-Type: application/json; charset=utf-8; v=1.0 
Date: Mon, 25 Sep 2023 16:39:51 GMT   
Server: Kestrel  
Transfer-Encoding: chunked  
api-supported-versions: 1.0  

**Тело ответа:**
```
{
    "id": 3,
    "title": "string",
    "dueDate": "2023-09-22T05:54:10.236Z",
    "completed": true
}
```
***** 
### PUT Тест 54- Проверка нагрузки ответа по id 
URL: "https://fakerestapi.azurewebsites.net/api/v1/Activities/5"  

**ОР**: ответ своевременный, содержит данные в формате JSON, без ошибок, заголовки согласно спецификации, код 200  

**Заголовки запроса**:
Content-Type: application/json  
User-Agent: PostmanRuntime/7.33.0  
Accept: \*/\*  
Postman-Token: 1736a2fa-740d-4fb1-bdc7-c98821b07874  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br   
Connection: keep-alive  
Content-Length: 57  

**Тело запроса**:  
```
{
  "id": {{activity_real_id}},
  "title": "read",
  "completed": true
}
``` 
**Заголовки ответа**:
Content-Type: application/json; charset=utf-8; v=1.0   
Date: Mon, 25 Sep 2023 18:33:30 GMT  
Server: Kestrel  
Transfer-Encoding: chunked  
api-supported-versions: 1.0  

**Тело ответа**:
```
{
    "id": 5,
    "title": "read",
    "dueDate": "0001-01-01T00:00:00",
    "completed": true
}
```
*****
### PUT Тест 55- Проверка заголовков ответа по id
URL: "https://fakerestapi.azurewebsites.net/api/v1/Activities/8"   
**ОР**: получены заголовки согласно спецификации, не содержится заголовок "X-Powered-By"  

 **Заголовки запроса**:
 Content-Type: application/json  
User-Agent: PostmanRuntime/7.33.0  
Accept: \*/\*  
Postman-Token: 04c59776-47ea-4987-87cd-adaa44841086  
Host: fakerestapi.azurewebsites.net   
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  
Content-Length: 101  

**Тело запроса**:
```
{
  "id": {{activity8_id}},
  "title": "string",
  "dueDate": "2023-09-22T05:54:10.236Z",
  "completed": true
}
```
**Заголовки ответа**:
Content-Type: application/json; charset=utf-8; v=1.0  
Date: Mon, 25 Sep 2023 19:23:13 GMT  
Server: Kestrel  
Transfer-Encoding: chunked  
api-supported-versions: 1.0  

**Тело ответа**:
```
{
    "id": 8,
    "title": "string",
    "dueDate": "2023-09-22T05:54:10.236Z",
    "completed": true
}
```
******
### PUT Тест 57- Обновление списка активностей с неверными данными  
URL: "https://fakerestapi.azurewebsites.net/api/v1/Activities/8"   
**ОР**: данные не обновлены, код 400  

**Заголовки запроса**:
Content-Type: application/json  
User-Agent: PostmanRuntime/7.33.0  
Accept: \*/\*  
Postman-Token: a356507c-77fe-41ec-9f76-23aa02e4b397  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  
Content-Length: 100  

**Тело запроса**:
```
{
  "id": ,
  "title": "string",
  "dueDate": "2023-09-22T05:54:10.236Z",
  "completed": true
}
```

**Заголовки ответа**:
Content-Type: application/problem+json; charset=utf-8  
Date: Mon, 25 Sep 2023 19:32:50 GMT  
Server: Kestrel  
Transfer-Encoding: chunked  

**Тело ответа:**
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-11a6b0c1173824479ae49961c79fb59a-7d3c42bd72572745-00",
    "errors": {
        "$.id": [
            "',' is an invalid start of a value. Path: $.id | LineNumber: 1 | BytePositionInLine: 8."
        ]
    }
}
```
*****
### DELETE Тест 60 - Удаление активностей по id  
URL: "https://fakerestapi.azurewebsites.net/api/v1/Activities/30"  

**ОР**: сущность удалена, код 200  

**Заголовки запроса:**
User-Agent: PostmanRuntime/7.33.0  
Accept: \*/\*  
Postman-Token: 7541a801-ffa5-4889-a98c-f1270b488622  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  
 
 **Заголовик ответа:**
Content-Length: 0  
Date: Mon, 25 Sep 2023 19:55:03 GMT  
Server: Kestrel  
api-supported-versions: 1.0  
*****
### DELETE Тест 61 - Проверка корректности кода по id  
URL: "https://fakerestapi.azurewebsites.net/api/v1/Activities/3"  

**ОР**: запрос выполнен, код 200  

**Заголовки запроса:**  
User-Agent: PostmanRuntime/7.33.0  
Accept: \*/\*  
Postman-Token: 5763f500-c8bf-4b3e-98d1-a7d3400f9d20  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  

**Заголовки ответа**:
Content-Length: 0  
Date: Mon, 25 Sep 2023 19:59:44 GMT  
Server: Kestrel  
api-supported-versions: 1.0  
*****

### DELETE Тест 63- Проверка заголовков ответа по id  
URL: "https://fakerestapi.azurewebsites.net/api/v1/Activities/18"  

**ОР**: ответ своевременный, получены заголовки согласно спецификации, не содержится заголовок "X-Powered-By"  

**Заголовки запроса**:
User-Agent: PostmanRuntime/7.33.0
Accept: \*/\*
Postman-Token: 3e92cbb3-b2cb-4cde-806e-a0d9295ad5fa
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Заголовки ответа**:
Content-Length: 0  
Date: Mon, 25 Sep 2023 20:05:23 GMT  
Server: Kestrel  
api-supported-versions: 1.0  
****

### DELETE Тест 65 - Удаление активностей с неверными данными  
URL: "https://fakerestapi.azurewebsites.net/api/v1/Activities/123"  

**ОР**: удаление не успешно, код 404  

**Заголовки запроса**:
User-Agent: PostmanRuntime/7.33.0  
Accept: \*/\*  
Postman-Token: 06f90909-020e-402f-9824-fd8628e70e88  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  

 **Заголовки ответа**:  
 Content-Length: 0  
Date: Mon, 25 Sep 2023 20:14:16 GMT  
Server: Kestrel  
api-supported-versions: 1.0  
*****
### DELETE Тест 66 - Удаление активностей неверным методом    
URL: "https://fakerestapi.azurewebsites.net/api/v1/Activities/5"  

**ОР**: удаление сущности методом HEAD не успешно, код 405  

**Заголовки запроса**:  
User-Agent: PostmanRuntime/7.33.0  
Accept: \*/\*    
Postman-Token: e595f0eb-df29-45f4-806d-703eb8e0659b  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  

**Заголовки ответа**:
Date: Mon, 25 Sep 2023 20:20:08 GMT  
Server: Kestrel  
Allow: DELETE, GET, PUT  
****
# CoverPhotos 
### GET Тест 88 - Получение списка фото для обложки  
URL: "https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos"  

**ОР**: получен список сущностей, код 200  

**Заголовки запроса**: 
User-Agent: PostmanRuntime/7.33.0  
Accept: \*/\*  
Postman-Token: 0a0cae25-6370-49f2-913b-e120b901315e  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  

**Заголовки ответа**:  
Content-Type: application/json; charset=utf-8; v=1.0  
Date: Tue, 26 Sep 2023 12:53:53 GMT  
Server: Kestrel  
Transfer-Encoding: chunked  
api-supported-versions: 1.0  

**Тело ответа**:
```
{
        "id": 1,
        "idBook": 1,
        "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 1&w=250&h=350"
    },
    {
        "id": 2,
        "idBook": 2,
        "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 2&w=250&h=350"
    }
```
*****

### GET Тест 90 - Проверка нагрузки ответа  
URL: "https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos"  

**ОР**: ответ своевременный, содержит данные в формате JSON, без ошибок, заголовки согласно спецификации, код 200   

**Заголовки запроса**: 
User-Agent: PostmanRuntime/7.33.0  
Accept: \*/\*  
Postman-Token: 3d223750-62d7-4faf-8d09-e2046f5a5d2d  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  

**Заголовки ответа**:
Content-Type: application/json; charset=utf-8; v=1.0  
Date: Tue, 26 Sep 2023 12:59:06 GMT  
Server: Kestrel  
Transfer-Encoding: chunked  
api-supported-versions: 1.0  

**Тело ответа**:
```
{
        "id": 1,
        "idBook": 1,
        "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 1&w=250&h=350"
    },
    {
        "id": 2,
        "idBook": 2,
        "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 2&w=250&h=350"
    }
```
*****
### GET Тест 94 - Проверка заголовков ответа 
URL: "https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos"  

**ОР**: получены заголовки согласно спецификации, не содержится заголовок "X-Powered-By"  

**Заголовки запроса**:
User-Agent: PostmanRuntime/7.33.0  
Accept: \*/\*    
Postman-Token: 90b00bb9-c912-4b64-b5ff-f9ed36365a18  
Host: fakerestapi.azurewebsites.net    
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  

**Заголовки ответа**:
Content-Type: application/json; charset=utf-8; v=1.0  
Date: Tue, 26 Sep 2023 13:09:59 GMT  
Server: Kestrel  
Transfer-Encoding: chunked  
api-supported-versions: 1.0  

**Тело ответа**:
```
{
        "id": 3,
        "idBook": 3,
        "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 3&w=250&h=350"
}
```

### GET Тест 96 - Получение списка фото для обложки неверным методом  

URL: "https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos"  

**ОР**: список не получен, код 405  

**Заголовки запроса**:  
User-Agent: PostmanRuntime/7.33.0  
Accept: \*/\*  
Postman-Token: 8f0e0380-2f8a-4d9c-b9bf-a487ca3083e3   
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  

**Заголовки ответа**:  
Content-Length: 0  
Date: Tue, 26 Sep 2023 13:15:47 GMT  
Server: Kestrel  
Allow: GET, POST  
****

### POST Тест 97- отправление новых сущностей фото для обложки  
URL: "https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos"  

**ОР**: Новая сущность создана, код 201  

**Заголовки запроса**:
Content-Type: application/json  
User-Agent: PostmanRuntime/7.33.0  
Accept: \*/\*  
Postman-Token: e975ca26-bfeb-4c5b-90ef-b5bcfa451c1e  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  
Content-Length: 53  

**Тело запроса**:  
```
{
  "id": {{cover_id}},
  "idBook": 0,
  "url": "string"
}
```

**Заголовки ответа**:  
Content-Type: application/json; charset=utf-8; v=1.0  
Date: Tue, 26 Sep 2023 13:22:49 GMT  
Server: Kestrel  
Transfer-Encoding: chunked  
api-supported-versions: 1.0  

**Тело ответа**:  
```
{
    "id": 205,
    "idBook": 0,
    "url": "string"
}
```
******

### POST Тест 101 - Проверка нагрузки ответа 
URL: ""https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos"  
**ОР**: ответ своевременный, содержит данные в формате JSON, без ошибок, заголовки согласно спецификации

**Заголовки запроса**:  
Content-Type: application/json  
User-Agent: PostmanRuntime/7.33.0  
Accept: \*/\*  
Postman-Token: 249f5c18-ac84-439b-b419-3906415df63e  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  
Content-Length: 53  

**Тело запроса**:  
```
{
  "id": {{cover_id}},
  "idBook": 0,
  "url": "string"
}
```
**Заголоки ответа**:  
Content-Type: application/json; charset=utf-8; v=1.0  
Date: Tue, 26 Sep 2023 14:11:15 GMT  
Server: Kestrel  
Transfer-Encoding: chunked  
api-supported-versions: 1.0   

**Тело ответа**:  
```
{
    "id": 205,
    "idBook": 0,
    "url": "string"
}
```
*******
### POST Тест 102 - Проверка заголовков ответа  
URL: "https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos"  
**ОР**: получены заголовки согласно спецификации, не содержится заголовок "X-Powered-By"  

**Заголовки запроса**:  
Content-Type: application/json  
User-Agent: PostmanRuntime/7.33.0  
Accept: \*/\*  
Postman-Token: a87dc7a5-0160-4194-9ed7-1511e34fdbf8  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  
Content-Length: 53    

**Тело запроса**:  
```
{
  "id": {{cover_id}},
  "idBook": 0,
  "url": "string"
}
```

**Заголовки ответа**:  
Content-Type: application/json; charset=utf-8; v=1.0
Date: Tue, 26 Sep 2023 16:30:31 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0  

**Тело ответа**:
```
{
    "id": 205,
    "idBook": 0,
    "url": "string"
}
```
### POST Тест 106 - Создание нового объекта фото для обложки с неверными данными  
URL: "https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos"  
**ОР**: объект не создан, код 400

**Заголовки запроса**:  
Content-Type: application/json  
User-Agent: PostmanRuntime/7.33.0  
Accept: \*/\* 
Postman-Token: f702f0c8-3e69-4b2d-ba3b-9a51c6dc1634  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  
Content-Length: 44  

**Тело запроса**:  
```
{
  "id": {{cover_id}},
  "idBook": 0,
  "url":
}
```
**Заголовки ответа**:  
Content-Type: application/problem+json; charset=utf-8  
Date: Tue, 26 Sep 2023 16:36:13 GMT  
Server: Kestrel  
Transfer-Encoding: chunked  

**Тело ответа**:
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-267694998d790e41b45d268e8015d29f-be78f398eba69f41-00",
    "errors": {
        "$.url": [
            "'}' is an invalid start of a value. Path: $.url | LineNumber: 4 | BytePositionInLine: 0."
        ]
    }
}
```
*****
### POST Тест 107 - Создание нового объекта фото для обложки неверным методом  
URL: "https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos"  
**ОР**: Создание объекта методом PATCH не успешно, код 405

**Заголовки запроса**:  
Content-Type: application/json  
User-Agent: PostmanRuntime/7.33.0  
Accept: \*/\*  
Postman-Token: 4a1c0ec0-b66a-4884-8e14-f75b85a08ef8  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br 
Connection: keep-alive  
Content-Length: 51  

**Тело запроса**:
```
{
  "id": 0,
  "idBook": 0,
  "url": "string"
}
```
**Заголовки ответа**:  
Content-Length: 0  
Date: Tue, 26 Sep 2023 16:40:02 GMT  
Server: Kestrel  
Allow: GET, POST  
*****
### POST Тест 109- создание нового объекта фото для обложки: неполная модель  
URL: "https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos"  
**ОР**: объект не создан, код 400  
 
 **Заголовки запроса**:  
Content-Type: application/json  
User-Agent: PostmanRuntime/7.33.0  
Accept: \*/\*  
Postman-Token: f9e21d0f-2324-4041-8dd3-d58a9a1a8897  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  
Content-Length: 14  

 **Тело запроса**:  
```
{
  "id": 
}
```
 **Заголовки ответа**:  
Content-Type: application/problem+json; charset=utf-8  
Date: Tue, 26 Sep 2023 16:44:46 GMT  
Server: Kestrel  
Transfer-Encoding: chunked  

**Тело ответа**:
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-a35de5e57094ca49b429c1bd7b3a0620-0cc6606bcd6db641-00",
    "errors": {
        "$.id": [
            "'}' is an invalid start of a value. Path: $.id | LineNumber: 2 | BytePositionInLine: 0."
        ]
    }
}
```
*****

### GET Тест 110 - Получение списка новых созданных сущностей по id  
URL: "https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/205"  
**ОР**: Ответ содержит данные новой созданной сущности, код 200   

**Заголовки запроса**:  
User-Agent: PostmanRuntime/7.33.0  
Accept: \*/\*  
Postman-Token: 843acc4b-1b05-4f6c-a76e-b098354de0a1  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  

**Заголовки ответа**:  
Content-Type: application/problem+json; charset=utf-8; v=1.0  
Date: Tue, 26 Sep 2023 16:59:45 GMT  
Server: Kestrel  
Transfer-Encoding: chunked  
api-supported-versions: 1.0  

**Тело ответа**:  
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.4",
    "title": "Not Found",
    "status": 404,
    "traceId": "00-e16b98a8ace50b44a94cd98e51fd3c64-cacb594c000fb543-00"
}
```
*****

### GET Тест 112 - Проверка нагрузки ответа по id  
URL: "https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/10"  
**ОР**: ответ своевременный, содержит данные в формате JSON, без ошибок, заголовки согласно спецификации, код 200     

**Заголовки запроса**:   
User-Agent: PostmanRuntime/7.33.0  
Accept: \*/\*  
Postman-Token: 332e2b90-5232-4383-aa7c-41d4b41384c1  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  

**Заголовки ответа**:  
Content-Type: application/json; charset=utf-8; v=1.0  
Date: Tue, 26 Sep 2023 17:05:26 GMT  
Server: Kestrel  
Transfer-Encoding: chunked  
api-supported-versions: 1.0  

**Тело ответа:**
```
{
    "id": 10,
    "idBook": 10,
    "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 10&w=250&h=350"
}
```
****
### GET Тест 115 - Проверка заголовков ответа по id  
URL: "https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/10"  
**ОР**: получены заголовки согласно спецификации, не содержится заголовок "X-Powered-By"  

**Заголовки запроса**:  
User-Agent: PostmanRuntime/7.33.0  
Accept: \*/\*  
Postman-Token: 9a7f12f7-02da-4877-b251-b06b9a3c0ab9  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  

**Заголовки ответа**:  
Content-Type: application/json; charset=utf-8; v=1.0  
Date: Tue, 26 Sep 2023 17:10:11 GMT  
Server: Kestrel  
Transfer-Encoding: chunked  
api-supported-versions: 1.0  

**Тело ответа**:
```
{
    "id": 10,
    "idBook": 10,
    "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 10&w=250&h=350"
}
```
****
### GET Тест 118 - Получение объекта фото для обложки по неверному id   
URL: "https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/5999999"    
**ОР**:  объект не получен ,код 404  

**Заголовки запроса**:  
User-Agent: PostmanRuntime/7.33.0  
Accept: \*/\*  
Postman-Token: cd37a6e0-aacb-46d6-a821-2e58b61247b9  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  

**Заголовки ответа**:   
Content-Type: application/problem+json; charset=utf-8; v=1.0  
Date: Tue, 26 Sep 2023 17:21:52 GMT  
Server: Kestrel  
Transfer-Encoding: chunked  
api-supported-versions: 1.0  

 **Тело ответа:**
 ```
 {
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.4",
    "title": "Not Found",
    "status": 404,
    "traceId": "00-cf42fe6c333d6d4d848ea4d4d6ca44d6-fef43a3f2519304f-00"
}
```
*****

### GET Тест 119 - Получение объекта фото для обложки по id неверным методом  
URL: "https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/10"     
**ОР**:  получение сущности методом OPTIONS не успешно, код 405  

**Заголовки запроса**:  
User-Agent: PostmanRuntime/7.33.0  
Accept: \*/\*  
Postman-Token: b7e5fb8f-10c0-4d47-a931-2db27ef4856a  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  

**Заголовки ответа**:
Content-Length: 0  
Date: Tue, 26 Sep 2023 17:34:20 GMT  
Server: Kestrel  
Allow: DELETE, GET, PUT  

****
### GET Тест 121- Получение данных объекта обложки книг по id  
URL: "https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/31"      
**ОР**:  получение сущности, код 200 

**Заголовки запроса**:  
User-Agent: PostmanRuntime/7.33.0  
Accept: \*/\*  
Postman-Token: 1066c26b-765b-47e3-bdcc-d792f2d6c46c  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  

**Заголовки ответа**:  
Content-Type: application/json; charset=utf-8; v=1.0  
Date: Tue, 26 Sep 2023 17:39:10 GMT  
Server: Kestrel  
Transfer-Encoding: chunked  
api-supported-versions: 1.0  

**Тело ответа**:  
```
{
    "id": 31,
    "idBook": 31,
    "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 31&w=250&h=350"
}
```
*****
### PUT Тест 129 - Обновление списка фото для обложек по id  
URL: "https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/10"        
**ОР**: данные обновлены успешно, код 200  

**Заголовки запроса**:  
Content-Type: application/json  
User-Agent: PostmanRuntime/7.33.0  
Accept: \*/\*  
Postman-Token: 573969ce-0b5b-4c9c-9cf6-6dc9fd9dd0d4  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  
Content-Length: 55  

**Тело запроса**:  
```
{
  "id": {{cover_real_id}},
  "idBook": "10",
  "url": "string"
}
```
**Заголовки ответа**:  
Content-Type: application/json; charset=utf-8; v=1.0  
Date: Tue, 26 Sep 2023 17:49:18 GMT  
Server: Kestrel  
Transfer-Encoding: chunked  
api-supported-versions: 1.0  

**Тело ответа**:
```
{
    "id": 10,
    "idBook": 10,
    "url": "string"
}
```
*****
### PUT Тест 132- Проверка нагрузки ответа по id  
URL: "https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/10"        
**ОР**: ответ своевременный, содержит данные в формате JSON, без ошибок, заголовки согласно спецификации, код 200     

**Заголовки запроса**:
Content-Type: application/json  
User-Agent: PostmanRuntime/7.33.0  
Accept: \*/\*  
Postman-Token: d77c4dd3-edbd-4ac7-aae5-4e44da0ac6d1  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  
Content-Length: 53  

**Тело запроса**:  
```
{
  "id": {{cover_real_id}},
  "idBook": 10,
  "url": "string"
}
```
**Заголовки ответа**:  
Content-Type: application/json; charset=utf-8; v=1.0  
Date: Tue, 26 Sep 2023 17:55:29 GMT  
Server: Kestrel  
Transfer-Encoding: chunked  
api-supported-versions: 1.0  

**Тело ответа**:  
```
{
    "id": 10,
    "idBook": 10,
    "url": "string"
}
```
*****

### PUT  Тест 133 - Проверка заголовков ответа по id  
URL: "https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/10"        
**ОР**: получены заголовки согласно спецификации, не содержится заголовок "X-Powered-By"  

**Заголовки запроса**:
Content-Type: application/json  
User-Agent: PostmanRuntime/7.33.0  
Accept: \*/\*  
Postman-Token: 0571e871-f222-411a-a588-ebe2f7cb645d  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  
Content-Length: 53  

**Тело запроса**:
```
{
  "id": {{cover_real_id}},
  "idBook": 10,
  "url": "string"
}
```
**Заголовки ответа**:
Content-Type: application/json; charset=utf-8; v=1.0  
Date: Tue, 26 Sep 2023 18:01:21 GMT  
Server: Kestrel  
Transfer-Encoding: chunked  
api-supported-versions: 1.0  

**Тело ответа:**
```
{
    "id": 10,
    "idBook": 10,
    "url": "string"
}
```
*****

### PUT Тест 135 - Обновление списка активностей с неверными данными  
URL: "https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/10"        
**ОР**: обновление данных не успешно, код 400  

**Заголовки запроса**:
Content-Type: application/json  
User-Agent: PostmanRuntime/7.33.0  
Accept: \*/\*  
Postman-Token: bb220cbd-64af-4213-8e33-d7e41ebe91b9  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  
Content-Length: 52  

**Тело запроса**:  
```
{
  "id": {{cover_real_id}}
  "idBook": {{cover_real_id}},
  "url": "string"
}
```
**Заголовки ответа**:  
Content-Type: application/problem+json; charset=utf-8  
Date: Tue, 26 Sep 2023 18:06:14 GMT  
Server: Kestrel  
Transfer-Encoding: chunked  

**Тело ответа**:
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-62613f0189e94f41bca432dfda34269b-11371ac1cb4f2e41-00",
    "errors": {
        "$": [
            "'\"' is invalid after a value. Expected either ',', '}', or ']'. Path: $ | LineNumber: 2 | BytePositionInLine: 2."
        ]
    }
}
```
******
### PUT Тест 136 - Обновление списка активностей неверным методом  
URL: "https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos"       
**ОР**: обновление данных методом HEAD не успешно, код 405  

**Заголовки запроса**:  
Content-Type: application/json  
User-Agent: PostmanRuntime/7.33.0  
Accept: \*/\*  
Postman-Token: 092f2dc4-c9b1-46cf-bab9-73cb037edd33 
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  
Content-Length: 53  

**Тело запроса**:  
```
{
  "id": 10,
  "idBook": 10,
  "url": "string"
}
```
**Заголовки ответа**:  
Date: Tue, 26 Sep 2023 18:15:01 GMT  
Server: Kestrel  
Allow: GET, POST  
*****

### DELETE Тест 138 - Удаление объектов фото для обложки по id  
URL: "https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/205"  

**ОР**: удаление успешно, код 200  

**Заголовки запроса**:  
User-Agent: PostmanRuntime/7.33.0   
Accept: \*/\*  
Postman-Token: db3e865e-a537-4bf5-bfd1-1617245e7bd8  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  

**Заголовки ответа**:
Content-Length: 0  
Date: Tue, 26 Sep 2023 18:22:59 GMT  
Server: Kestrel  
api-supported-versions: 1.0  
*******
### DELETE Тест 141 - Проверка заголовков ответа по id  
URL: "https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/10"  

**ОР**: Ответ своевременный, получены заголовки согласно спецификации, не содержится заголовок "X-Powered-By"  

**Заголовки запроса**:  
User-Agent: PostmanRuntime/7.33.0  
Accept: \*/\*  
Postman-Token: 20775fa9-ad8c-40d2-8e92-1c8992a33fb4  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  

**Заголовки ответа:**
Content-Length: 0  
Date: Tue, 26 Sep 2023 18:25:56 GMT  
Server: Kestrel  
api-supported-versions: 1.0  
*****
### DELETE Тест 143 - Удаление объекта фото для обложки с неверными данными  
URL: "https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/203"  

**ОР**: удаление не успешно, код 404  

**Заголовки запроса**:  
User-Agent: PostmanRuntime/7.33.0  
Accept: \*/\*  
Postman-Token: cd13cf8b-279c-44a2-a54c-2a5250ea58de  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  

**Заголовки ответа**:
Content-Length: 0  
Date: Tue, 26 Sep 2023 18:30:15 GMT   
Server: Kestrel  
api-supported-versions: 1.0  
****
### DELETE Тест 144 - Удаление объекта фото для обложки неверным методом  
URL: "https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/10"  

**ОР**: удаление методом HEAD не успешно, код 405  

**Заголовки запроса**:  
User-Agent: PostmanRuntime/7.33.0  
Accept: \*/\*  
Postman-Token: 5ed847dc-0520-4c36-8c1a-1a2687dddd59  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  

**Заголовки ответа**:  
Date: Tue, 26 Sep 2023 18:33:33 GMT  
Server: Kestrel  
Allow: DELETE, GET, PUT  
*****
# Users
### GET Тест 152 - Получение списка пользователей  
URL: "https://fakerestapi.azurewebsites.net/api/v1/Users"

**ОР**: ответ своевременный, получен список пользователей, код 200

**Заголовки запроса**:  
User-Agent: PostmanRuntime/7.33.0  
Accept: \*/\*  
Postman-Token: fb40c390-7446-4b60-bc63-5500adb7be37  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  

**Заголовки ответа**:  
Content-Type: application/json; charset=utf-8; v=1.0  
Date: Tue, 26 Sep 2023 18:36:01 GMT  
Server: Kestrel  
Transfer-Encoding: chunked  
api-supported-versions: 1.0  
 
 **Тело ответа:**  
 ```
    {
        "id": 2,
        "userName": "User 2",
        "password": "Password2"
    },
    {
        "id": 3,
        "userName": "User 3",
        "password": "Password3"
    }
```
****
### GET Тест 154 - Проверка нагрузки ответа  
URL: "https://fakerestapi.azurewebsites.net/api/v1/Users"

**ОР**: ответ содержит данные в формате JSON, без ошибок, заголовки согласно спецификации, код 200   

**Заголовки запроса**  
User-Agent: PostmanRuntime/7.33.0  
Accept: \*/\*  
Postman-Token: bd8913ee-1f99-4e74-9703-eac8368ac6de  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  

**Заголовки ответа**:
Content-Type: application/json; charset=utf-8; v=1.0  
Date: Tue, 26 Sep 2023 18:41:51 GMT  
Server: Kestrel  
Transfer-Encoding: chunked  
api-supported-versions: 1.0  

**Тело ответа**:  
```
    {
        "id": 1,
        "userName": "User 1",
        "password": "Password1"
    },
    {
        "id": 2,
        "userName": "User 2",
        "password": "Password2"
    }
```
### GET Тест 155 - Проверка заголовков ответа  
URL: "https://fakerestapi.azurewebsites.net/api/v1/Users"  

**ОР**: получены заголовки согласно спецификации, не содержится заголовок "X-Powered-By"  

**Заголовки запроса**:  
User-Agent: PostmanRuntime/7.33.0  
Accept: \*/\*  
Postman-Token: ff0287de-2b6f-401c-b28c-1e9d9c90500e  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  

**Заголовки ответа**:  
Content-Type: application/json; charset=utf-8; v=1.0  
Date: Tue, 26 Sep 2023 18:46:53 GMT  
Server: Kestrel  
Transfer-Encoding: chunked  
api-supported-versions: 1.0  

**Тело ответа:** 
```
{
        "id": 2,
        "userName": "User 2",
        "password": "Password2"
}
``` 
****
### GET Тест 157 - Получение списка пользователей неверным методом  
URL: "https://fakerestapi.azurewebsites.net/api/v1/Users"  

**ОР**: ответ своевременный, список пользователей методом OPTIONS не получен, код 405  

**Заголовки запроса**:  
User-Agent: PostmanRuntime/7.33.0  
Accept: \*/\*  
Postman-Token: f79a104e-0d52-4de5-8ec1-767d3aaf0456  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  

**Заголовки ответа**:  
Content-Length: 0  
Date: Tue, 26 Sep 2023 18:50:32 GMT  
Server: Kestrel  
Allow: GET, POST 
*****
### POST Тест 158 - Создание новых пользователей  
 URL: "https://fakerestapi.azurewebsites.net/api/v1/Users"  

**ОР**: новая сущность (пользователь) создана ,код 201  

**Заголовки запроса**:  
Content-Type: application/json  
User-Agent: PostmanRuntime/7.33.0  
Accept: \*/\*  
Postman-Token: b9623019-7c6e-4e85-beae-8091768cd7c3   
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  
Content-Length: 79  

**Тело запроса**:
```
{
    "id": {{user_id}},
    "userName": "User {{user_id}}",
    "password": "Password{{user_id}}"
}
 ```
**Заголовки ответа**:  
Content-Type: application/json; charset=utf-8; v=1.0
Date: Tue, 26 Sep 2023 18:52:49 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0  

**Тело ответа:**
```
{
    "id": 11,
    "userName": "User 11",
    "password": "Password11"
}
```
****
### POST Тест 161 - Проверка нагрузки ответа  
URL: "https://fakerestapi.azurewebsites.net/api/v1/Users"  
**ОР**:  ответ своевременный, содержит данные в формате JSON, без ошибок, заголовки согласно спецификации  

**Заголовки запроса**:  
Content-Type: application/json  
User-Agent: PostmanRuntime/7.33.0  
Accept: \*/\*  
Postman-Token: d2c3b165-13d7-4e43-a0dd-22e0b7858513  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  
Content-Length: 74  

**Тело запроса**:  
```
{
    "id": {{user_real_id}},
    "userName": "User {{user_real_id}}",
    "password": "Password{{user_real_id}}"
}
```
**Заголовки ответа**:  
Content-Type: application/json; charset=utf-8; v=1.0  
Date: Wed, 27 Sep 2023 07:19:10 GMT  
Server: Kestrel  
Transfer-Encoding: chunked  
api-supported-versions: 1.0  

**Тело ответа**:  
```
{
    "id": 7,
    "userName": "User 7",
    "password": "Password7"
}
```
### POST Тест 162 - Проверка заголовков ответа  
URL: "https://fakerestapi.azurewebsites.net/api/v1/Users"  

**ОР**: получены заголовки согласно спецификации, не содержится заголовок "X-Powered-By"  

**Заголовки запроса**:  
Content-Type: application/json  
User-Agent: PostmanRuntime/7.33.0  
Accept: \*/\*  
Postman-Token: 82a7bc4a-692d-4ed9-bff0-fa1627542633  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  
Content-Length: 74  

**Тело запроса**:  
```
{
    "id": {{user_real_id}},
    "userName": "User {{user_real_id}}",
    "password": "Password{{user_real_id}}"
}
```
**Заголовки ответа**:  
Content-Type: application/json; charset=utf-8; v=1.0   
Date: Tue, 26 Sep 2023 19:05:23 GMT  
Server: Kestrel  
Transfer-Encoding: chunked  
api-supported-versions: 1.0  
**Тело ответа**:  
```
{
    "id": 7,
    "userName": "User 7",
    "password": "Password7"
}
```
*****
### POST Тест 164 - Создание новых пользователей с неверными данными  
URL: "https://fakerestapi.azurewebsites.net/api/v1/Users"  

**ОР**: создание сущности не успешно, код 400  

**Заголовки запроса**:   
Content-Type: application/json  
User-Agent: PostmanRuntime/7.33.0  
Accept: \*/\*  
Postman-Token: 033c5a69-bde2-4a0c-bde1-2b28cc587cc9  
Host: fakerestapi.azurewebsites.net   
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  
Content-Length: 65  

**Тело запроса**:  
```
{
    "id": 3,
    "userName": "User 3",
    "password": 
}
```
**Заголовки ответа**:  
Content-Type: application/problem+json; charset=utf-8  
Date: Tue, 26 Sep 2023 19:09:18 GMT  
Server: Kestrel  
Transfer-Encoding: chunked  

**Тело ответа**:  
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-682ad0c4bc43464b94fc1b81a1c95cad-b058a2821e001941-00",
    "errors": {
        "$.password": [
            "'}' is an invalid start of a value. Path: $.password | LineNumber: 4 | BytePositionInLine: 2."
        ]
    }
}
```
****
### POST Тест 168 - Проверка создания нового пользователя  
URL: "https://fakerestapi.azurewebsites.net/api/v1/Users"  

**ОР**: создание сущности успешно, подтверждено запросом GET, код 200  

**Заголовки запроса**:  
Content-Type: application/json  
User-Agent: PostmanRuntime/7.33.0  
Accept: \*/\*  
Postman-Token: cc0d034b-7d6e-4084-8931-b2d39afb6660  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  
Content-Length: 85  

**Тело запроса**:  
```
{
    "id": {{user_id}},
    "userName": "User {{user_id}}",
    "password": "Password{{user_id}}"
}
```
**Заголовки ответа**:  
Content-Type: application/problem+json; charset=utf-8  
Date: Tue, 26 Sep 2023 19:33:39 GMT  
Server: Kestrel  
Transfer-Encoding: chunked  

**Тело ответа**:  
```
{
    "id": 11,
    "userName": "User 11",
    "password": "Password11"
}
```
****
### GET Тест 169 - Получение списка пользователей по id   
URL: "https://fakerestapi.azurewebsites.net/api/v1/Users/7"  

**ОР**: ответ успешный, сущность получена, код 200  

**Заголовки запроса**:  
User-Agent: PostmanRuntime/7.33.0  
Accept: \*/\*  
Postman-Token: 56e11e96-2fe3-4c5c-8c0b-4cda127b7665  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  

**Заголовки ответа**:  
Content-Type: application/json; charset=utf-8; v=1.0  
Date: Tue, 26 Sep 2023 19:38:18 GMT  
Server: Kestrel  
Transfer-Encoding: chunked  
api-supported-versions: 1.0  

**Тело ответа**:  
```
{
    "id": 7,
    "userName": "User 7",
    "password": "Password7"
}
```
*****
### GET Тест 174 - Получение сущности пользователя по неверному id  
URL: "https://fakerestapi.azurewebsites.net/api/v1/Users/12"  

**ОР**: сущность не получена, код 404  

**Заголовки запроса**:  
User-Agent: PostmanRuntime/7.33.0  
Accept: \*/\*  
Postman-Token: 237e23ac-01ce-411e-aaab-6a13f318d2e4  
Host: fakerestapi.azurewebsites.net   
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  

**Заголовки ответа**:  
Content-Type: application/problem+json; charset=utf-8; v=1.0  
Date: Tue, 26 Sep 2023 19:44:23 GMT  
Server: Kestrel  
Transfer-Encoding: chunked  
api-supported-versions: 1.0  

**Тело ответа**:
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.4",
    "title": "Not Found",
    "status": 404,
    "traceId": "00-bd91839fd62e6548a013486519af0407-f01a4d45bcb7a74b-00"
}
```
****
### GET Тест 175 - Получение сущности пользователя по id неверным методом  
URL: "https://fakerestapi.azurewebsites.net/api/v1/Users/7"  

**ОР**: ответ своевременный, получение сущности методом OPTIONS не успешно, код 405  

**Заголовки запроса**:  
User-Agent: PostmanRuntime/7.33.0  
Accept: \*/\*  
Postman-Token: 02e13e04-4739-4dac-972e-2b60c9bf97b6  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  

**Заголовки ответа**:  
Content-Length: 0  
Date: Tue, 26 Sep 2023 19:53:22 GMT  
Server: Kestrel  
Allow: DELETE, GET, PUT  
****

### PUT Тест 177 - Обновление списка пользователей по id  
URL: "https://fakerestapi.azurewebsites.net/api/v1/Users/7"  

**ОР**: обновление успешное, код 200  

**Заголовки запроса**:  
Content-Type: application/json   
User-Agent: PostmanRuntime/7.33.0  
Accept: \*/\*
Postman-Token: d3d2ca63-8bce-4e53-bef7-830103c6bc3e  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  
Content-Length: 76  

**Тело запроса**:  
```
{
    "id": {{user_real_id}},
    "userName": "SuperUser {{user_real_id}}",
    "password": "Password{{user_real_id}}"
  }
```
**Заголовки ответа**:  
Content-Type: application/json; charset=utf-8; v=1.0  
Date: Wed, 27 Sep 2023 07:23:38 GMT  
Server: Kestrel  
Transfer-Encoding: chunked  
api-supported-versions: 1.0  

**Тело ответа**:
```
{
    "id": 7,
    "userName": "SuperUser 7",
    "password": "Password7"
}
```
### PUT Тест 183 - Обновление списка пользователей с неверными данными
URL: "https://fakerestapi.azurewebsites.net/api/v1/Users/7"  

**ОР**: обновление не успешно, код 400  

**Заголовки запроса**:  
Content-Type: application/json  
User-Agent: PostmanRuntime/7.33.0  
Accept: \*/\*  
Postman-Token: a6d2814c-a1c4-4735-b3a5-2bc90a53076c  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  
Content-Length: 76  

**Тело запроса**:  
```
{
    "id": {{user_real_id}}
    "userName": "User {{user_real_id}}",
    "password": "Password{{user_real_id}}"
}
```
**Заголовки ответа**:  
Content-Type: application/json; charset=utf-8; v=1.0  
Date: Tue, 26 Sep 2023 20:00:43 GMT  
Server: Kestrel  
Transfer-Encoding: chunked  
api-supported-versions: 1.0  

**Тело ответа**:  
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-886e33403f99c44397ee9574ba80462c-6c8cb3e5fdb35442-00",
    "errors": {
        "$": [
            "'\"' is invalid after a value. Expected either ',', '}', or ']'. Path: $ | LineNumber: 2 | BytePositionInLine: 4."
        ]
    }
}
```
***** 
### DELETE Тест 187- Удаление объектов пользователей по id  

URL: "https://fakerestapi.azurewebsites.net/api/v1/Users/2"  

**ОР**: объект удален успешно, код 200  

**Заголовки запроса**:  
User-Agent: PostmanRuntime/7.33.0  
Accept: \*/\*  
Postman-Token: b0328a2f-ca62-4b89-91a2-7e49a18d9cf3  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  

**Заголовки ответа**:  
Content-Length: 0  
Date: Wed, 27 Sep 2023 04:39:21 GMT  
Server: Kestrel  
api-supported-versions: 1.0  
****
### DELETE Тест 190- Проверка заголовков ответа по id
URL: "https://fakerestapi.azurewebsites.net/api/v1/Users/2"  

**ОР**: ответ своевременный, получены заголовки согласно спецификации, не содержится заголовок "X-Powered-By"

**Заголовки запроса**:  
User-Agent: PostmanRuntime/7.33.0  
Accept: \*/\*  
Postman-Token: 7f56def1-4750-4608-81a4-5a6c9254082e   
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  

**Заголовки ответа**:  
Content-Length: 0  
Date: Wed, 27 Sep 2023 04:42:22 GMT  
Server: Kestrel  
api-supported-versions: 1.0  
****
### DELETE Тест 192 - Удаление пользователя с неверными данными  
URL: "https://fakerestapi.azurewebsites.net/api/v1/Users/203"  

**ОР**: удаление не успешно, пользователь не найден, код 404  

**Заголовки запроса**:  
User-Agent: PostmanRuntime/7.33.0  
Accept: \*/\*  
Postman-Token: 206b3b9b-9be3-4842-af14-35571e8238cd  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive   

**Заголовки ответа**:  
Content-Length: 0  
Date: Wed, 27 Sep 2023 04:45:13 GMT  
Server: Kestrel  
api-supported-versions: 1.0  
*****
### DELETE Тест 193 - Удаление объекта пользователя неверным методом  
URL: "https://fakerestapi.azurewebsites.net/api/v1/Users/2"  

**ОР**: удаление методом HEAD не успешно, код 405  

**Заголовки запроса**:  
User-Agent: PostmanRuntime/7.33.0  
Accept: \*/\*  
Postman-Token: 7266a645-521a-42f9-a62b-0b025b996e3c  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  

**Заголовки ответа**:  
Date: Wed, 27 Sep 2023 04:53:32 GMT  
Server: Kestrel  
Allow: DELETE, GET, PUT  
****
# Books  

### GET Тест 68 - Получение списка книг  

URL: "https://fakerestapi.azurewebsites.net/api/v1/Books"  

**ОР**: получен список книг, код ответа 200  

**Заголовки зароса:**  

User-Agent: PostmanRuntime/7.33.0  

Accept: */*  

Postman-Token: e8c03ddc-22e2-4e75-a972-7b6c7af6e3ed  

Host: fakerestapi.azurewebsites.net  

Accept-Encoding: gzip, deflate, br  

Connection: keep-alive  

**Заголовки ответа:**  

Content-Type: application/json; charset=utf-8; v=1.0  

Date: Mon, 27 Sep 2023 14:13:05 GMT  

Server: Kestrel  

Transfer-Encoding: chunked  

api-supported-versions: 1.0  

**Тело ответа:**  

{  

        "id": 3,  

        "title": "Books 3",  

        "dueDate": "2023-09-24T05:56:13.4654534+00:00",  

        "completed": false  

    },  

    {  

        "id": 4,  

        "title": "Books 4",  

        "dueDate": "2023-09-24T06:56:13.4654536+00:00",  

        "completed": true  

    },  

    {  

        "id": 5,  

        "title": "Books 5",  

        "dueDate": "2023-09-24T07:56:13.4654539+00:00",  

        "completed": false  

    }  
    
****

### GET Тест 69 - Проверка корректности кода  

URL: "https://fakerestapi.azurewebsites.net/api/v1/Books"  

**ОР:** выполнен запрос, код ответа 200  

**Заголовки запроса:**  

User-Agent: PostmanRuntime/7.33.0  

Accept: */*  

Postman-Token: c113d5ec-961b-4c78-9468-8f93a70c0a8b  

Host: fakerestapi.azurewebsites.net  

Accept-Encoding: gzip, deflate, br  

Connection: keep-alive  

**Заголовки ответа:**  

Content-Length: 0  

Connection: close  

Date: Mon, 27 Sep 2023 14:16:27 GMT  
****


### GET Тест 75 - Проверка нагрузки ответа  

URL: "https://fakerestapi.azurewebsites.net/api/v1/Books"  

**ОР:** выполнен запрос, код ответа 200  

**Заголовки запроса:**  

User-Agent: PostmanRuntime/7.33.0  

Accept: */*  

Postman-Token: 23001923-d2cb-4292-9409-cc9ecbdaa8c3  

Host: fakerestapi.azurewebsites.net  

Accept-Encoding: gzip, deflate, br  

Connection: keep-alive  

**Заголовки ответа**  

Content-Type: application/json; charset=utf-8; v=1.0  

Date: Mon, 27 Sep 2023 14:26:19 GMT  

Server: Kestrel  

Transfer-Encoding: chunked  

api-supported-versions: 1.0  
****


### GET Тест 76 - Проверка заголовков ответа  

URL: "https://fakerestapi.azurewebsites.net/api/v1/Books"  

**ОР:** Ответ своевременный, получены заголовки согласно спецификации, не содержится заголовок "X-Powered-By"  

**Заголовки запроса**  

User-Agent: PostmanRuntime/7.33.0  

Accept: */*  

Postman-Token: 6fde750a-de85-42e5-8e41-4575a297adcf  

Host: fakerestapi.azurewebsites.net  

Accept-Encoding: gzip, deflate, br  

Connection: keep-alive  

**Заголовки ответа**  

Content-Type: application/json; charset=utf-8; v=1.0  

Date: Mon, 27 Sep 2023 14:36:18 GMT  

Server: Kestrel  

Transfer-Encoding: chunked  

api-supported-versions: 1.0  
****


### GET Тест 78 - Получение списка книг неверным методом  

URL: "https://fakerestapi.azurewebsites.net/api/v1/Books"  

**ОР:** список методом OPTIONS не получен, код 405 "Method Not Allowed"  

**Заголовки зароса:**  

User-Agent: PostmanRuntime/7.33.0  

Accept: */*  

Postman-Token: 6e7f4640-7113-4ffd-bf9c-07889fb9cf0b  

Host: fakerestapi.azurewebsites.net  

Accept-Encoding: gzip, deflate, br  

Connection: keep-alive  

**Заголовки ответа**  

Content-Length: 0  

Date: Mon, 27 Sep 2023 14:41:28 GMT  

Server: Kestrel  

Allow: GET, POST  
****


### POST Тест 80 - Отправление нового списка книг  

URL: "https://fakerestapi.azurewebsites.net/api/v1/Books"  

**ОР:** новая сущность создана, код 201  

**Заголовки запроса:**  

Content-Type: application/json  

User-Agent: PostmanRuntime/7.33.0  

Accept: */*  

Postman-Token: 8edf4d41-49b1-4ff3-8418-afae46b0bcb4  

Host: fakerestapi.azurewebsites.net  

Accept-Encoding: gzip, deflate, br  

Connection: keep-alive  

Content-Length: 102  

**Тело запроса:**  

{  

  "id": {{books_id}},  

  "title": "string",  

  "dueDate": "2023-09-22T05:54:10.236Z",  

  "completed": true  

}  

**Заголовки ответа:**  

Content-Type: application/json; charset=utf-8; v=1.0  

Date: Mon, 27 Sep 2023 14:47:15 GMT  

Server: Kestrel  

Transfer-Encoding: chunked  

api-supported-versions: 1.0  

**Тело ответа:**  

{  

    "id": 33,  

    "title": "string",  

    "dueDate": "2023-09-22T05:54:10.236Z",  

    "completed": true  

}  
****


### POST Тест 83 - Проверка нагрузки ответа  

URL: "https://fakerestapi.azurewebsites.net/api/v1/Books"  

**ОР:** ответ своевременный, содержит данные в формате JSON, без ошибок, заголовки согласно спецификации  

**Заголовки запроса:**  

Content-Type: application/json  

User-Agent: PostmanRuntime/7.33.0  

Accept: */*  

Postman-Token: 48237dd9-be66-45e9-9201-a21a7b00517b  

Host: fakerestapi.azurewebsites.net  

Accept-Encoding: gzip, deflate, br  

Connection: keep-alive  

Content-Length: 102  

**Тело запроса:**  

{  

  "id": {{books_id}},  

  "title": "string",  

  "dueDate": "2023-09-22T05:54:10.236Z",  

  "completed": true  

}  

**Заголовки ответа:**  

Content-Type: application/json; charset=utf-8; v=1.0  

Date: Mon, 27 Sep 2023 14:59:06 GMT  

Server: Kestrel  

Transfer-Encoding: chunked  

api-supported-versions: 1.0  

**Тело ответа:**  

{  

    "id": 33,  

    "title": "string",  

    "dueDate": "2023-09-22T05:54:10.236Z",  

    "completed": true  

}  
****


### POST Тест 84 - Проверка заголовков ответа  

URL: "https://fakerestapi.azurewebsites.net/api/v1/Books"  

**ОР:** получены заголовки согласно спецификации, не содержится заголовок "X-Powered-By"  

**Заголовки запроса:**  

Content-Type: application/json  

User-Agent: PostmanRuntime/7.33.0  

Accept: */*  

Postman-Token: 76b1b832-1e44-45ea-9b57-df196dae8fbd  

Host: fakerestapi.azurewebsites.net  

Accept-Encoding: gzip, deflate, br  

Connection: keep-alive  

Content-Length: 110  

**Тело запроса:**  

{  

    "id": {{books_id}},  

    "title": "string",  

    "dueDate": "2023-09-22T05:54:10.236Z",  

    "completed": true  

}  

**Заголовки ответа:**  

Content-Type: application/json; charset=utf-8; v=1.0  

Date: Mon, 27 Sep 2023 05:15:12 GMT  

Server: Kestrel  

Transfer-Encoding: chunked  

api-supported-versions: 1.0  

**Тело ответа:**  

{  

    "id": 33,  

    "title": "string",  

    "dueDate": "2023-09-22T05:54:10.236Z",  

    "completed": true  

}  
****


### POST Тест 85 - Создание нового списка книг с неверными данными  

URL: "https://fakerestapi.azurewebsites.net/api/v1/Books"  

**ОР:**  Новая сущность не создана, код 400  

**Заголовки запроса:**  

Content-Type: application/json  

User-Agent: PostmanRuntime/7.33.0  

Accept: */*  

Postman-Token: aca8390c-00bb-4665-8b2b-f7059ac38d06  

Host: fakerestapi.azurewebsites.net  

Accept-Encoding: gzip, deflate, br  

Connection: keep-alive  

Content-Length: 100  

**Тело запроса:**  

{  

  "id": ,  

  "title": "string",  

  "dueDate": "2023-09-22T05:54:10.236Z",  

  "completed": true  

}  

**Заголовки ответа:**  

Content-Length: 0  

Date: Mon, 27 Sep 2023 15:21:01 GMT  

Server: Kestrel  
****


### PATH Тест 86 - Создание новой книги неверным методом  

URL: "https://fakerestapi.azurewebsites.net/api/v1/Books"  

**ОР:** Новая сущность методом PATCH не создана, ответ 405  

**Заголовки запроса:**  

Content-Type: application/json  

User-Agent: PostmanRuntime/7.33.0  

Accept: */*  

Postman-Token: 866ba14d-4f2a-467f-afe6-18c4de8633a2  

Host: fakerestapi.azurewebsites.net  

Accept-Encoding: gzip, deflate, br  

Connection: keep-alive  

Content-Length: 102  

**Тело запроса:**  

{  

  "id": {{books_id}},  

  "title": "string",  

  "dueDate": "2023-09-22T05:54:10.236Z",  

  "completed": true  

}  

**Заголовки ответа:**  

Content-Length: 0  

Date: Mon, 27 Sep 2023 15:38:03 GMT  

Server: Kestrel  

Allow: GET, POST  
****


### GET Тест 87 - Получение списка созданных книг по id.  

URL: "https://fakerestapi.azurewebsites.net/api/v1/Books/33"  

**ОР:** в ответе получена созданная сущность c новым id, код ответа 200  

**Заголовки запроса:**  

User-Agent: PostmanRuntime/7.33.0  

Accept: */*  

Postman-Token: 72ea9144-35f3-4bf0-9bcf-f6ea001982e9  

Host: fakerestapi.azurewebsites.net  

Accept-Encoding: gzip, deflate, br  

Connection: keep-alive  

**Заголовки ответа:**  

Content-Type: application/json; charset=utf-8; v=1.0  

Date: Mon, 27 Sep 2023 15:47:37 GMT  

Server: Kestrel  

Transfer-Encoding: chunked  

api-supported-versions: 1.0  

**Тело ответа:**  

{  

    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.4",  

    "title": "Not Found",  

    "status": 404,  

    "traceId": "00-b5b6816be1168a408317103be10c35de-550db4f8e793e94d-00"  

}  
****


### GET Тест 91 - Получение списка активностей по неверному id  

URL: "https://fakerestapi.azurewebsites.net/api/v1/Books/5999999"  

**ОР:** ответ своевременный, сущность не получена, код 404  

**Заголовки запроса:**  

User-Agent: PostmanRuntime/7.33.0  

Accept: */*  

Postman-Token: 34907e08-0873-46fa-9b95-6052b53205cf  

Host: fakerestapi.azurewebsites.net  

Accept-Encoding: gzip, deflate, br  

Connection: keep-alive  

**Заголовки ответа:**  

Content-Type: application/problem+json; charset=utf-8; v=1.0  

Date: Mon, 25 Sep 2023 15:53:36 GMT  

Server: Kestrel  

Transfer-Encoding: chunked  

api-supported-versions: 1.0  
****


### PATCH Тест 93 - Получение списка книг по id неверным методом  

URL: "https://fakerestapi.azurewebsites.net/api/v1/Books/8"  

**ОР:** методом PATCH ответ не получен, ошибка 405  

**Заголовки запроса:**  

User-Agent: PostmanRuntime/7.33.0  

Accept: */*  

Postman-Token: 9313b681-6607-4954-bede-7308eef7fc11  

Host: fakerestapi.azurewebsites.net  

Accept-Encoding: gzip, deflate, br  

Connection: keep-alive  

Content-Length: 0   

**Заголовки ответа:**  

Content-Length: 0  

Date: Mon, 25 Sep 2023 16:05:29 GMT  

Server: Kestrel  

Allow: DELETE, GET, PUT  
****


### POST Тест 99 - Создание нового списка книг - дублирование  

URL: "https://fakerestapi.azurewebsites.net/api/v1/Books"  

**ОР:** дублированная сущность не создастся, код 409  

**Заголовки запроса:**  

Content-Type: application/json  

User-Agent: PostmanRuntime/7.33.0  

Accept: */*  

Postman-Token: 4b333b38-2b0d-45fe-a778-f7ab5fda2fad  

Host: fakerestapi.azurewebsites.net  

Accept-Encoding: gzip, deflate, br  

Connection: keep-alive  

Content-Length: 101  

**Тело запроса:**  

{  

  "id": {{book8_id}},  

  "title": "string",  

  "dueDate": "2023-09-22T05:54:10.236Z",  

  "completed": true  

}  

**Заголовки ответа:**  

Content-Type: application/json; charset=utf-8; v=1.0  

Date: Mon, 27 Sep 2023 18:04:44 GMT  

Server: Kestrel  

Transfer-Encoding: chunked  

api-supported-versions: 1.0  

**Тело ответа:**  

{  

    "id": 8,  

    "title": "string",  

    "dueDate": "2023-09-22T 05:54:10.236Z",  

    "completed": true  

}  
****


### GET Тест 105 - Проверка нагрузки ответа по id  

URL: "https://fakerestapi.azurewebsites.net/api/v1/Books/5"  

**ОР:** выполнен запрос, ответ содержит данные в формате JSON, без ошибок, заголовки согласно спецификации, код 200   код ответа 200  

**Заголовки запроса:**  

User-Agent: PostmanRuntime/7.33.0  

Accept: */*  

Postman-Token: 06955eec-1bfa-44f0-bb20-7b0c40652682  

Host: fakerestapi.azurewebsites.net  

Accept-Encoding: gzip, deflate, br  

Connection: keep-alive  

**Заголовки ответа:**  

Content-Type: application/json; charset=utf-8; v=1.0  

Date: Mon, 27 Sep 2023 18:09:28 GMT  

Server: Kestrel  

Transfer-Encoding: chunked  

api-supported-versions: 1.0  

**Тело ответа:**  

{  

    "id": 5,  

    "title": "Books 5",  

    "dueDate": "2023-09-25T23:13:28.5032805+00:00",  

    "completed": false  

}  
****


### GET Тест 113 - Проверка заголовков по id  

URL: "https://fakerestapi.azurewebsites.net/api/v1/Books/4"  

**ОР:** ответ своевременный, получены заголовки согласно спецификации, не содержится заголовок "X-Powered-By"  

**Заголовки запроса:**  

User-Agent: PostmanRuntime/7.33.0  

Accept: */*  

Postman-Token: ce7aa20a-6990-4f70-bc1f-86fb60f787d0  

Host: fakerestapi.azurewebsites.net  

Accept-Encoding: gzip, deflate, br  

Connection: keep-alive  

**Заголовки ответа:**  

Content-Type: application/json; charset=utf-8; v=1.0  

Date: Mon, 27 Sep 2023 18:15:00 GMT  

Server: Kestrel  

Transfer-Encoding: chunked  

api-supported-versions: 1.0  

**Тело ответа:**  

{  

    "id":4,  

    "title":"Books 4",  

    "dueDate":"2023-09-25T16:25:00.9000624+00:00",  

    "completed":true  

}  
****


### PUT Тест 234 - Обновление списка книг по id  

URL: "https://fakerestapi.azurewebsites.net/api/v1/Books/15"  

**ОР:** ответ содержит обновленные данные сущности, код 200  

**Заголовки запроса:**  

Content-Type: application/json  

User-Agent: PostmanRuntime/7.33.0  

Accept: */*  

Postman-Token: b768ea5f-13e3-405c-a43c-a18177206b92  

Host: fakerestapi.azurewebsites.net  

Accept-Encoding: gzip, deflate, br  

Connection: keep-alive  

Content-Length: 100  

**Тело запроса:**  

{  

  "id": 15,  

  "title": "read",  

  "dueDate": "2023-09-22T05:54:10.236Z",  

  "completed": true  

}  

**Заголовки ответа:**  

Content-Type: application/json; charset=utf-8; v=1.0  

Date: Mon, 27 Sep 2023 18:19:22 GMT  

Server: Kestrel  

Transfer-Encoding: chunked  

api-supported-versions: 1.0  

**Тело ответа:**   

{  

    "id": 15,  

    "title": "read",  

    "dueDate": "2023-09-22T05:54:10.236Z",  

    "completed": true  

}  
****


### PUT Тест 235 - Проверка корректности кода по id  

URL: "https://fakerestapi.azurewebsites.net/api/v1/Books/3"  

**ОР:** запрос выполнен, код 200  

**Заголовки запроса:**  

Content-Type: application/json  

User-Agent: PostmanRuntime/7.33.0  

Accept: */*  

Postman-Token: a09f282a-a1f7-4b1c-a1d4-cb7a2b0e753f  

Host: fakerestapi.azurewebsites.net  

Accept-Encoding: gzip, deflate, br  

Connection: keep-alive  

Content-Length: 101  

**Тело запроса:**  

{  

  "id": 3,  

  "title": "string",  

  "dueDate": "2023-09-22T05:54:10.236Z",  

  "completed": true  

}  

**Заголовки ответа:**  

Content-Type: application/json; charset=utf-8; v=1.0  

Date: Mon, 27 Sep 2023 18:29:51 GMT  

Server: Kestrel  

Transfer-Encoding: chunked  

api-supported-versions: 1.0  

**Тело ответа:**  

{  

    "id": 3,  

    "title": "string",  

    "dueDate": "2023-09-22T05:54:10.236Z",  

    "completed": true  

}  
****


### PUT Тест 105- Проверка нагрузки ответа по id  

URL: "https://fakerestapi.azurewebsites.net/api/v1/Books/5"  

**ОР:** ответ своевременный, содержит данные в формате JSON, без ошибок, заголовки согласно спецификации, код 200  

**Заголовки запроса:**  

Content-Type: application/json  

User-Agent: PostmanRuntime/7.33.0  

Accept: */*  

Postman-Token: 1736a2fa-740d-4fb1-bdc7-c98821b07874  

Host: fakerestapi.azurewebsites.net  

Accept-Encoding: gzip, deflate, br  

Connection: keep-alive  

Content-Length: 57  

**Тело запроса:**  

{  

  "id": {{books_real_id}},  

  "title": "read",  

  "completed": true  

}  

**Заголовки ответа:**  

Content-Type: application/json; charset=utf-8; v=1.0  

Date: Mon, 27 Sep 2023 18:34:30 GMT  

Server: Kestrel  

Transfer-Encoding: chunked  

api-supported-versions: 1.0  

**Тело ответа:**  

{  

    "id": 5,  

    "title": "read",  

    "dueDate": "0001-01-01T00:00:00",  

    "completed": true  

}  
****


### PUT Тест 238- Проверка заголовков ответа по id  

URL: "https://fakerestapi.azurewebsites.net/api/v1/Books/8"  

**ОР:** получены заголовки согласно спецификации, не содержится заголовок "X-Powered-By"  

**Заголовки запроса:**  

Content-Type: application/json  

User-Agent: PostmanRuntime/7.33.0  

Accept: */*  

Postman-Token: 04c59776-47ea-4987-87cd-adaa44841086  

Host: fakerestapi.azurewebsites.net  

Accept-Encoding: gzip, deflate, br  

Connection: keep-alive  

Content-Length: 101  

**Тело запроса:**  

{  

  "id": {{books8_id}},  

  "title": "string",  

  "dueDate": "2023-09-22T05:54:10.236Z",  

  "completed": true  

}   

**Заголовки ответа:**  

Content-Type: application/json; charset=utf-8; v=1.0  

Date: Mon, 27 Sep 2023 18:37:13 GMT  

Server: Kestrel  

Transfer-Encoding: chunked  

api-supported-versions: 1.0  

**Тело ответа:**  

{  

    "id": 8,  

    "title": "string",  

    "dueDate": "2023-09-22T05:54:10.236Z",  

    "completed": true  

}  
****


### PUT Тест 239- Обновление списка книг с неверными данными  

URL: "https://fakerestapi.azurewebsites.net/api/v1/Books/8"  

**ОР:** данные не обновлены, код 400  

**Заголовки запроса:**  

Content-Type: application/json  

User-Agent: PostmanRuntime/7.33.0  

Accept: */*  

Postman-Token: a356507c-77fe-41ec-9f76-23aa02e4b397  

Host: fakerestapi.azurewebsites.net  

Accept-Encoding: gzip, deflate, br  

Connection: keep-alive  

Content-Length: 100  

**Тело запроса:**  

{  

  "id": ,  

  "title": "string",  

  "dueDate": "2023-09-22T05:54:10.236Z",  

  "completed": true  

}  

**Заголовки ответа:**  

Content-Type: application/problem+json; charset=utf-8  

Date: Mon, 27 Sep 2023 19:32:50 GMT  

Server: Kestrel  

Transfer-Encoding: chunked  

**Тело ответа:**  

{  

    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",  

    "title": "One or more validation errors occurred.",  

    "status": 400,  

    "traceId": "00-11a6b0c1173824479ae49961c79fb59a-7d3c42bd72572745-00",  

    "errors": {  

        "$.id": [  

            "',' is an invalid start of a value. Path: $.id | LineNumber: 1 | BytePositionInLine: 8."  

        ]  

    }  

}  
****


### DELETE Тест 247- Удаление списка книг по id  

URL: "https://fakerestapi.azurewebsites.net/api/v1/Books/30"  

**ОР:** сущность удалена, код 200  

**Заголовки запроса:**  

User-Agent: PostmanRuntime/7.33.0  

Accept: */*  

Postman-Token: 7541a801-ffa5-4889-a98c-f1270b488622  

Host: fakerestapi.azurewebsites.net  

Accept-Encoding: gzip, deflate, br  

Connection: keep-alive  

**Заголовик ответа:**  

Content-Length: 0  

Date: Mon, 27 Sep 2023 18:45:03 GMT  

Server: Kestrel  

api-supported-versions: 1.  
****


### DELETE Тест 244 - Проверка корректности кода по id  

URL: "https://fakerestapi.azurewebsites.net/api/v1/Books/3"  

**ОР:** запрос выполнен, код 200  

**Заголовки запроса:** 

User-Agent: PostmanRuntime/7.33.0  

Accept: */*  

Postman-Token: 5763f500-c8bf-4b3e-98d1-a7d3400f9d20  

Host: fakerestapi.azurewebsites.net  

Accept-Encoding: gzip, deflate, br  

Connection: keep-alive  

**Заголовки ответа:**  

Content-Length: 0  

Date: Mon, 27 Sep 2023 18:49:44 GMT  

Server: Kestrel  

api-supported-versions: 1.0  
****


### DELETE Тест 246- Проверка заголовков ответа по id  

URL: "https://fakerestapi.azurewebsites.net/api/v1/Books/18"  

**ОР:** ответ своевременный, получены заголовки согласно спецификации, не содержится заголовок "X-Powered-By"  

**Заголовки запроса:**  

User-Agent: PostmanRuntime/7.33.0  

Accept: */*  

Postman-Token: 3e92cbb3-b2cb-4cde-806e-a0d9295ad5fa  

Host: fakerestapi.azurewebsites.net  

Accept-Encoding: gzip, deflate, br  

Connection: keep-alive  

**Заголовки ответа:**  

Content-Length: 0  

Date: Mon, 27 Sep 2023 18:54:23 GMT  

Server: Kestrel  

api-supported-versions: 1.0  
****


### DELETE Тест 247 - Удаление списка с неверными данными  

URL: "https://fakerestapi.azurewebsites.net/api/v1/Books/123"  

**ОР:** удаление не успешно, код 404  

**Заголовки запроса:**  

User-Agent: PostmanRuntime/7.33.0  

Accept: */*  

Postman-Token: 06f90909-020e-402f-9824-fd8628e70e88  

Host: fakerestapi.azurewebsites.net  

Accept-Encoding: gzip, deflate, br  

Connection: keep-alive  

**Заголовки ответа:**  

Content-Length: 0  

Date: Mon, 27 Sep 2023 18:58:16 GMT  

Server: Kestrel  

api-supported-versions: 1.0  
****


### DELETE Тест 249 - Удаление списка книг неверным методом  

URL: "https://fakerestapi.azurewebsites.net/api/v1/Books/5"  

**ОР:** удаление сущности методом HEAD не успешно, код 405  

**Заголовки запроса:**  

User-Agent: PostmanRuntime/7.33.0  

Accept: */*  

Postman-Token: e595f0eb-df29-45f4-806d-703eb8e0659b  

Host: fakerestapi.azurewebsites.net  

Accept-Encoding: gzip, deflate, br  

Connection: keep-alive  

**Заголовки ответа:**  

Date: Mon, 27 Sep 2023 19:05:08 GMT  

Server: Kestrel  

Allow: DELETE, GET, PUT  
****

## Authors

### GET Тест 39 - Получение списка авторов

- URL https://fakerestapi.azurewebsites.net/api/v1/Authors
- Ожидаемый результат:  
HTTP Status: 200 OK, Список авторов получен
- Заголовки запроса:  
User-Agent: PostmanRuntime/7.33.0  
Accept: */*  
Cache-Control: no-cache  
Postman-Token: f620b248-7bf6-461d-8bb2-eae6c90df1a2  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  
- Заголовки ответа:  
Content-Type: application/json; charset=utf-8; v=1.0  
Date: Tue, 26 Sep 2023 21:00:12 GMT  
Server: Kestrel  
Transfer-Encoding: chunked  
api-supported-versions: 1.0  
- Тело ответа:  
```
[ 
{ "id":  1,
"idBook":  1,
"firstName":  "First Name 1",
"lastName":  "Last Name 1" },
{"id":  2,
"idBook":  1,
"firstName":  "First Name 2",
"lastName":  "Last Name 2"}
]
```

### GET Тест 40 - Проверка корректности кода

- URL https://fakerestapi.azurewebsites.net/api/v1/Authors
- Ожидаемый результат:  
HTTP Status: 200 OK, Получен корректный код 
-  Заголовки запроса:  
User-Agent: PostmanRuntime/7.33.0  
Accept: */*  
Cache-Control: no-cache  
Postman-Token: f620b248-7bf6-461d-8bb2-eae6c90df1a2  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  
- Заголовки ответа:
Content-Type: application/json; charset=utf-8; v=1.0  
Date: Tue, 26 Sep 2023 21:00:12 GMT  
Server: Kestrel  
Transfer-Encoding: chunked  
api-supported-versions: 1.0  
- Тело ответа: 
```
[
{ "id":  1,
"idBook":  1,
"firstName":  "First Name 1",
"lastName":  "Last Name 1"},
{"id":  2,
"idBook":  1,
"firstName":  "First Name 2",
"lastName":  "Last Name 2"}
]
```

### GET Тест 41 - Проверка нагрузки ответа

- URL https://{{baseurl}}/Authors
- Ожидаемый результат:  
HTTP Status: 200 OK, Тело ответа содержит данные, согласно запросу
- Заголовки запроса:  
User-Agent: PostmanRuntime/7.33.0  
Accept: */*  
Cache-Control: no-cache  
Postman-Token: eadb64ac-cc8f-45b8-b910-3c829dd42f19  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive
- Заголовки ответа:
Content-Type: application/json; charset=utf-8; v=1.0  
Date: Tue, 26 Sep 2023 21:16:46 GMT  
Server: Kestrel  
Transfer-Encoding: chunked  
api-supported-versions: 1.0  
- Тело ответа:
```
[
{ "id":  1,
"idBook":  1,
"firstName":  "First Name 1",
"lastName":  "Last Name 1"},
{"id":  2,
"idBook":  1,
"firstName":  "First Name 2",
"lastName":  "Last Name 2"}
]
```

### GET Тест 42 - Проверка заголовков ответа

- URL https://{{baseurl}}/Authors
- Ожидаемый результат:  
HTTP Status: 200 OK, Выведены заголовки ответа согласно спецификации
- Заголовки запроса:  
User-Agent: PostmanRuntime/7.33.0  
Accept: */*  
Cache-Control: no-cache  
Postman-Token: ed76da1f-b302-4b5d-a0f1-814df17a1751    
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive
- Заголовки ответа:  
Content-Type: application/json; charset=utf-8; v=1.0   
Date: Tue, 26 Sep 2023 21:18:34 GMT  
Server: Kestrel  
Transfer-Encoding: chunked  
api-supported-versions: 1.0  
- Тело ответа:
```
[
{
"id":  1,
"idBook":  1,
"firstName":  "First Name 1",
"lastName":  "Last Name 1"},
{"id":  2,
"idBook":  1,
"firstName":  "First Name 2",
"lastName":  "Last Name 2"}
]
```

### GET Тест 43 - Проверка базовой работоспособности

- URL https://{{baseurl}}/Authors
- Ожидаемый результат:  
HTTP Status: 200 OK, Получен ответ в разумные сроки, согласно плану тестирования
- Заголовки запроса:  
User-Agent: PostmanRuntime/7.33.0  
Accept: */*  
Cache-Control: no-cache  
Postman-Token: ed76da1f-b302-4b5d-a0f1-814df17a1751  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  
- Заголовки ответа:
Content-Type: application/json; charset=utf-8; v=1.0  
Date: Tue, 26 Sep 2023 21:18:34 GMT  
Server: Kestrel  
Transfer-Encoding: chunked  
api-supported-versions: 1.0  
- Тело ответа:
```
[
{"id":  1,
"idBook":  1,
"firstName":  "First Name 1",
"lastName":  "Last Name 1"},
{
"id":  2,
"idBook":  1,
"firstName":  "First Name 2",
"lastName":  "Last Name 2"}
]
```

### OPTIONS Тест 44 - Получение списка авторов неверным методом

- URL  https://{{baseurl}}/Authors
- Ожидаемый результат:  
HTTP Status: 405 Method Not Allowed, Выбран неверный метод, список авторов не получен
- Заголовки запроса:  
User-Agent: PostmanRuntime/7.33.0  
Accept: */*  
Cache-Control: no-cache  
Postman-Token: eac27610-47e5-4617-b2db-39a2847c9390  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  
- Заголовки ответа:  
Content-Length: 0  
Date: Tue, 26 Sep 2023 21:24:12 GMT  
Server: Kestrel  
Allow: GET, POST

### POST Тест 45 - Отправление новых авторов

- URL https://{{baseurl}}/Authors
- Ожидаемый результат:  
HTTP Status: 200 OK
- Заголовки запроса:  
Content-Type: application/json  
User-Agent: PostmanRuntime/7.33.0  
Accept: */*  
Cache-Control: no-cache  
Postman-Token: 132103b3-cace-4b4f-b52c-e0cc57cc9f90  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive
- Тело запроса:
```
[
{
"id":  0,
"idBook":  0,
"firstName":  "string",
"lastName":  "string"
}
]
```
- Заголовки ответа:  
Content-Type: application/json; charset=utf-8; v=1.0  
Date: Tue, 26 Sep 2023 21:28:19 GMT  
Server: Kestrel  
Transfer-Encoding: chunked  
api-supported-versions: 1.0  
- Тело ответа:
```
[
{
"id":  0,
"idBook":  0,
"firstName":  "string",
"lastName":  "string"
}
]
```

### POST Тест 46 - Смена типа передаваемых данных

- URL https://{{baseurl}}/Authors
- Ожидаемый результат:  
HTTP Status: 200 OK, Тип данных изменен
- Заголовки запроса:  
Content-Type: application/json  
User-Agent: PostmanRuntime/7.33.0  
Accept: */*  
Cache-Control: no-cache  
Postman-Token: 5301b565-78c1-43a5-b42f-4dfb7a7ff291  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  
- Тело запроса:
```
[
{
"id":  0,
"idBook":  0,
"firstName":  "string",
"lastName":  "string"
}
]
```
- Заголовки ответа:  
Content-Type: application/json; charset=utf-8; v=1.0  
Date: Tue, 26 Sep 2023 21:34:18 GMT  
Server: Kestrel  
Transfer-Encoding: chunked  
api-supported-versions: 1.0  
- Тело ответа:
```
[
{
"id":  0,
"idBook":  0,
"firstName":  "string",
"lastName":  "string"
}
]
```

### POST Тест 47 - Проверка корректности кода

- URL https://{{baseurl}}/Authors
- Ожидаемый результат:  
HTTP Status: 200 OK, Получен корректный код  
- Заголовки запроса:  
Content-Type: application/json  
User-Agent: PostmanRuntime/7.33.0  
Accept: */*  
Cache-Control: no-cache  
Postman-Token: 0383ea81-37b0-4cb4-af1e-3b738effb5d0  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  
- Тело запроса:
```
[
{
"id":  0,
"idBook":  0,
"firstName":  "string",
"lastName":  "string"
}
]
```
- Заголовки ответа:  
Content-Type: application/json; charset=utf-8; v=1.0  
Date: Wed, 27 Sep 2023 06:34:04 GMT  
Server: Kestrel  
Transfer-Encoding: chunked  
api-supported-versions: 1.0  
- Тело ответа:
```
[
{
"id":  0,
"idBook":  0,
"firstName":  "string",
"lastName":  "string"
}
]
```

### POST Тест 48 - Проверка нагрузки ответа

- URL https://{{baseurl}}/Authors
- Ожидаемый результат:  
HTTP Status: 200 OK, Тело ответа содержит данные, согласно запросу  
- Заголовки запроса:  
Content-Type: application/json  
User-Agent: PostmanRuntime/7.33.0  
Accept: */*  
Cache-Control: no-cache  
Postman-Token: c106e2d5-caa5-4522-82fa-63b42ca97797  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  
- Тело запроса:
```
[
{
"id":  0,
"idBook":  0,
"firstName":  "string",
"lastName":  "string"
}
]
```
- Заголовки ответа:  
Content-Type: application/json; charset=utf-8; v=1.0  
Date: Tue, 26 Sep 2023 21:39:30 GMT  
Server: Kestrel  
Transfer-Encoding: chunked  
api-supported-versions: 1.0  
- Тело ответа:
```
[
{
"id":  0,
"idBook":  0,
"firstName":  "string",
"lastName":  "string"
}
]
```

### POST Тест 49 - Проверка заголовков ответа

- URL https://{{baseurl}}/Authors
- Ожидаемый результат:  
HTTP Status: 200 OK, Выведены заголовки ответа согласно спецификации  
- Заголовки запроса:  
Content-Type: application/json  
User-Agent: PostmanRuntime/7.33.0  
Accept: */*  
Cache-Control: no-cache  
Postman-Token: 82a3b678-8d39-4f6e-8902-600e257a52ed  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  
- Тело запроса:
```
[
{
"id":  0,
"idBook":  0,
"firstName":  "string",
"lastName":  "string"
}
]
```
- Заголовки ответа:  
Content-Type: application/json; charset=utf-8; v=1.0  
Date: Tue, 26 Sep 2023 21:39:30 GMT  
Server: Kestrel  
Transfer-Encoding: chunked  
api-supported-versions: 1.0  
- Тело ответа: 
```
[
{
"id":  0,
"idBook":  0,
"firstName":  "string",
"lastName":  "string"
}
]
```

### POST Тест 50 - Проверка базовой работоспособности

- URL https://{{baseurl}}/Authors
- Ожидаемый результат: HTTP Status:  
200 OK, Получен ответ в разумные сроки, согласно плану тестирования
- Заголовки запроса:  
Content-Type: application/json  
User-Agent: PostmanRuntime/7.33.0  
Accept: */*  
Cache-Control: no-cache  
Postman-Token: adeade2d-f09f-4f7d-84e0-dc9bce1def2a  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  
- Тело запроса:
```
[
{
"id":  0,
"idBook":  0,
"firstName":  "string",
"lastName":  "string"
}
]
```
- Заголовки ответа:  
Content-Type: application/json; charset=utf-8; v=1.0  
Date: Tue, 26 Sep 2023 21:43:31 GMT  
Server: Kestrel  
Transfer-Encoding: chunked  
api-supported-versions: 1.0  
- Тело ответа:
```
[
{
"id":  0,
"idBook":  0,
"firstName":  "string",
"lastName":  "string"
}
]
```

### POST Тест 51 - Создание новых авторов с неверными данными

- URL https://{{baseurl}}/Authors
- Ожидаемый результат:  
HTTP Status: 400 Bad Request, Новые данные не отправлены
- Заголовки запроса:  
Content-Type: application/json  
User-Agent: PostmanRuntime/7.33.0  
Accept: */*  
Cache-Control: no-cache  
Postman-Token: 80dfd2ba-bd03-4308-852d-7845c27d9feb  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  
-   Тело запроса:
```
[
{
"id":  ,
"idBook":  0,
"firstName":  "string",
"lastName":  "string" 
}
]
```
- Заголовки ответа:  
Content-Type: application/problem+json; charset=utf-8  
Date: Wed, 27 Sep 2023 06:16:05 GMT  
Server: Kestrel  
Transfer-Encoding: chunked   
- Тело ответа:
```
[
{
"type":  "https://tools.ietf.org/html/rfc7231#section-6.5.1",
"title":  "One or more validation errors occurred.",
"status":  400,
"traceId":  "00-f58bdbd64d959843a43d948c9c0103fb-8f796d4df6d14641-00",
"errors":  {
"$.id":  [
"',' is an invalid start of a value. Path: $.id | LineNumber: 1 | BytePositionInLine: 8."]}
}
]
```

### PATCH Тест 52 - Создание новых авторов неверным методом

- URL https://{{baseurl}}/Authors
- Ожидаемый результат:  
HTTP Status: 405 Method Not Allowed, Выбран неверный метод, новые авторы не созданы  
- Заголовки запроса:  
Content-Type: application/json  
User-Agent: PostmanRuntime/7.33.0  
Accept: */*  
Cache-Control: no-cache  
Postman-Token: 688e49f9-2fd6-43a2-b8a2-7ffe3214d66b  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  
- Тело запроса:
```
[
{
"id":  0,
"idBook":  0,
"firstName":  "string",
"lastName":  "string"
}
]
```
- Заголовки ответа:  
Content-Length: 0  
Date: Wed, 27 Sep 2023 06:19:57 GMT  
Server: Kestrel  
Allow: GET, POST  

### GET Тест 195 - Получение списка авторов по id

- URL https://{{baseurl}}/Authors/authors/books/5
- Ожидаемый результат:  
HTTP Status: 200 OK, Получен список авторов с заданным id
- Заголовки запроса:  
User-Agent: PostmanRuntime/7.33.0  
Accept: */*  
Cache-Control: no-cache  
Postman-Token: 19e7f7a8-db55-4aad-be56-37ca4e6a01c5  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  
- Заголовки ответа:  
Content-Type: application/json; charset=utf-8; v=1.0  
Date: Wed, 27 Sep 2023 06:23:48 GMT  
Server: Kestrel  
Transfer-Encoding: chunked  
api-supported-versions: 1.0  
- Тело ответа:
```
[
{
"id":  13,
"idBook":  5,
"firstName":  "First Name 13",
"lastName":  "Last Name 13"
},
{
"id":  14,
"idBook":  5,
"firstName":  "First Name 14",
"lastName":  "Last Name 14"
},
{
"id":  15,
"idBook":  5,
"firstName":  "First Name 15",
"lastName":  "Last Name 15"
},
{
"id":  16,
"idBook":  5,
"firstName":  "First Name 16",
"lastName":  "Last Name 16"
}
]
```

### GET Тест 196 - Получение списка авторов по id с неверными данными

- URL https://{{baseurl}}/Authors/authors/books/8345678876586
- Ожидаемый результат:  
HTTP Status: 400 Bad Request, Новые данные не отправлены
- Заголовки запроса:  
User-Agent: PostmanRuntime/7.33.0  
Accept: */*  
Cache-Control: no-cache  
Postman-Token: 4eda2eb8-1659-445e-8560-970bb94fed96  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  
- Заголовки ответа:  
Content-Type: application/problem+json; charset=utf-8  
Date: Wed, 27 Sep 2023 06:37:22 GMT  
Server: Kestrel  
Transfer-Encoding: chunked  
- Тело ответа:
```
[
{
"type":  "https://tools.ietf.org/html/rfc7231#section-6.5.1",
"title":  "One or more validation errors occurred.",
"status":  400,
"traceId":  "00-25b8a445871a2948a14e51bd96101646-773a7f51b97af948-00",
"errors":  {
"idBook":  [
"The value '8345678876586' is not valid."]}
}
]
```

### PATCH Тест 197 - Получение списка авторов по id неверным методом

- URL https://{{baseurl}}/Authors/authors/books/5
- Ожидаемый результат:  
HTTP Status: 405 Method Not Allowed, Выбран неверный метод, список авторов с выбранным id не получен  
- Заголовки запроса:  
User-Agent: PostmanRuntime/7.33.0  
Accept: */*  
Cache-Control: no-cache  
Postman-Token: 4eda2eb8-1659-445e-8560-970bb94fed96  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  
- Заголовки ответа:  
Content-Type: application/problem+json; charset=utf-8  
Date: Wed, 27 Sep 2023 06:37:22 GMT  
Server: Kestrel  
Transfer-Encoding: chunked  

### POST Тест 198 - Создание новых авторов - дублирование

- URL https://{{baseurl}}/Authors
- Ожидаемый результат:  
HTTP Status: 400 Bad Request  
- Заголовки запроса:  
Content-Type: application/json  
User-Agent: PostmanRuntime/7.33.0  
Accept: */*  
Cache-Control: no-cache  
Postman-Token: c65c4e12-12cc-4079-997f-bba5fae47599  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  
- Тело запроса:  
```
[
{
"id":  15,
"idBook":  0,
"firstName":  "string",
"lastName":  "string"
}
]
```
- Заголовки ответа:  
Content-Type: application/json; charset=utf-8; v=1.0  
Date: Wed, 27 Sep 2023 06:45:29 GMT  
Server: Kestrel  
Transfer-Encoding: chunked  
api-supported-versions: 1.0  
- Тело ответа:
```
[
{
"id":  15,
"idBook":  0,
"firstName":  "string",
"lastName":  "string"
}
]
```

### POST Тест 199 - Создание новых авторов - неполная модель

- URL https://{{baseurl}}/Authors
- Ожидаемый результат:  
HTTP Status: 400 Bad Request, Новые данные не отправлены  
- Заголовки запроса:  
Content-Type: application/json  
User-Agent: PostmanRuntime/7.33.0  
Accept: */*  
Cache-Control: no-cache  
Postman-Token: a5d5e023-ae87-46f2-af4a-ed4d9e639f3b  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  
-   Тело запроса:
```
[
{ "id": , 
"lastName": "string" }
]
```
- Заголовки ответа:  
Content-Type: application/problem+json; charset=utf-8  
Date: Wed, 27 Sep 2023 06:47:34 GMT  
Server: Kestrel  
Transfer-Encoding: chunked  
- Тело ответа:
```
[
{
"type":  "https://tools.ietf.org/html/rfc7231#section-6.5.1",
"title":  "One or more validation errors occurred.",
"status":  400,
"traceId":  "00-60f9ce3cff421d4b8ea2da5a08e455a5-a0e3488fa4d59e44-00",
"errors":  {
"$.id":  [
"',' is an invalid start of a value. Path: $.id | LineNumber: 1 | BytePositionInLine: 8."]}
}
]
```

### GET Тест 200 - Проверка корректности кода по id

- URL https://{{baseurl}}/Authors/5
- Ожидаемый результат:  
HTTP Status: 200 OK, Получен корректный код  
- Заголовки запроса:  
User-Agent: PostmanRuntime/7.33.0  
Accept: */*  
Cache-Control: no-cache  
Postman-Token: bdb84577-f386-426d-b7a7-deafd76a134e  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  
- Заголовки ответа:  
Content-Type: application/json; charset=utf-8; v=1.0  
Date: Wed, 27 Sep 2023 06:49:41 GMT  
Server: Kestrel  
Transfer-Encoding: chunked  
api-supported-versions: 1.0  
- Тело ответа:
```
[
{
"id":  5,
"idBook":  2,
"firstName":  "First Name 5",
"lastName":  "Last Name 5"
}
]
```

### GET Тест 201 - Проверка нагрузки ответа по id

- URL https://{{baseurl}}/Authors/5
- Ожидаемый результат:  
HTTP Status: 200 ОК, Тело ответа содержит данные, согласно запросу  
- Заголовки запроса:  
User-Agent: PostmanRuntime/7.33.0  
Accept: */*  
Cache-Control: no-cache  
Postman-Token: 942b2ef2-8876-49c8-b6d8-6d43b8cccc10  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  
- Заголовки ответа:  
Content-Type: application/json; charset=utf-8; v=1.0  
Date: Wed, 27 Sep 2023 06:51:13 GMT  
Server: Kestrel  
Transfer-Encoding: chunked  
api-supported-versions: 1.0  
- Тело ответа:
```
[
{
"id":  5,
"idBook":  2,
"firstName":  "First Name 5",
"lastName":  "Last Name 5"
}
]
```

### GET Тест 202 - Проверка заголовков ответа по id

- URL https://{{baseurl}}/Authors/7
- Ожидаемый результат:  
HTTP Status: 200 ОК, Выведены заголовки ответа согласно спецификации  
- Заголовки запроса:  
User-Agent: PostmanRuntime/7.33.0  
Accept: */*  
Cache-Control: no-cache  
Postman-Token: 174d6b58-d7ab-4c9f-a206-e0738d23a76b  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  
- Заголовки ответа:  
Content-Type: application/json; charset=utf-8; v=1.0  
Date: Wed, 27 Sep 2023 06:52:17 GMT  
Server: Kestrel  
Transfer-Encoding: chunked  
api-supported-versions: 1.0  
- Тело ответа:
```
[
{
"id":  7,
"idBook":  3,
"firstName":  "First Name 7",
"lastName":  "Last Name 7"
}
]
```

### GET Тест 203 - Проверка базовой работоспособности по id

- URL https://{{baseurl}}/Authors/5
- Ожидаемый результат: HTTP Status: 200 ОК, Получен ответ в разумные сроки, согласно плану тестирования  
- Заголовки запроса:  
User-Agent: PostmanRuntime/7.33.0  
Accept: */*  
Cache-Control: no-cache  
Postman-Token: 3ace1c0f-0c4e-4649-a2b8-ce66d0fdca87  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  
- Заголовки ответа:  
Content-Type: application/json; charset=utf-8; v=1.0  
Date: Wed, 27 Sep 2023 06:53:29 GMT  
Server: Kestrel  
Transfer-Encoding: chunked  
api-supported-versions: 1.0  
- Тело ответа:
```
[
{
"id":  5,
"idBook":  2,
"firstName":  "First Name 5",
"lastName":  "Last Name 5"
}
]
```

### GET Тест 204 - Получение списка авторов по неверному id: производительность

- URL https://{{baseurl}}/Authors/8909999800
- Ожидаемый результат: HTTP Status: 400 Bad Request, Список авторов не получен  
- Заголовки запроса:  
User-Agent: PostmanRuntime/7.33.0  
Accept: */*  
Cache-Control: no-cache  
Postman-Token: 5ab469bb-5dd8-403f-8584-3e1f56089084  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
- Заголовки ответа:  
Content-Type: application/problem+json; charset=utf-8  
Date: Wed, 27 Sep 2023 06:54:57 GMT  
Server: Kestrel  
Transfer-Encoding: chunked  
- Тело ответа:
```
[
{
"type":  "https://tools.ietf.org/html/rfc7231#section-6.5.1",
"title":  "One or more validation errors occurred.",
"status":  400,
"traceId":  "00-57b6f9c4e1e7654d990f825c0e224d6a-dd984ec21964ed47-00",
"errors":  {
"id":  [
"The value '8909999800' is not valid."]}
}
]
```

### PUT Тест 205 - Обновление списка авторов по id

- URL https://{{baseurl}}/Authors/3
- Ожидаемый результат: HTTP Status: 200 ОК, Список авторов обновлен  
- Заголовки запроса:  
Content-Type: application/json  
User-Agent: PostmanRuntime/7.33.0  
Accept: */*  
Cache-Control: no-cache  
Postman-Token: 1f696e21-f4c1-4f90-801d-b62665fb2e16  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  
- Тело запроса:
```
[
{
"id":  3,
"idBook":  2,
"firstName":  "First Name 2",
"lastName":  "Last Name 2",
"title":  "Book 1"
}
]
```
- Заголовки ответа:  
Content-Type: application/json; charset=utf-8; v=1.0  
Date: Wed, 27 Sep 2023 06:56:49 GMT  
Server: Kestrel  
Transfer-Encoding: chunked  
api-supported-versions: 1.0  
- Тело ответа:
```
[
{
"id":  3,
"idBook":  2,
"firstName":  "First Name 2",
"lastName":  "Last Name 2"
}
]
```

### PUT Тест 206 - Смена типа передаваемых данных по id

- URL https://{{baseurl}}/Authors/2
- Ожидаемый результат: HTTP Status: 200 ОК
- Заголовки запроса:  
Content-Type: application/json
User-Agent: PostmanRuntime/7.33.0  
Accept: */*  
Cache-Control: no-cache  
Postman-Token: 8e7ce499-8683-4eb4-9b99-39b8213b100c  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  
- Тело запроса:
```
[
{
"id":  2,
"idBook":  2,
"firstName":  "First Name 2",
"lastName":  "Last Name 2",
"title":  "Book 1"
}
]
```
- Заголовки ответа:  
Content-Type: application/json; charset=utf-8; v=1.0  
Date: Wed, 27 Sep 2023 06:58:01 GMT  
Server: Kestrel  
Transfer-Encoding: chunked  
api-supported-versions: 1.0  
- Тело ответа:
```
[
{
"id":  2,
"idBook":  2,
"firstName":  "First Name 2",
"lastName":  "Last Name 2"
}
]
```

### PUT Тест 207 - Проверка корректности кода по id

- URL https://{{baseurl}}/Authors/3
- Ожидаемый результат: HTTP Status: 200 ОК, Получен корректный код  
- Заголовки запроса:  
Content-Type: application/json  
User-Agent: PostmanRuntime/7.33.0  
Accept: */*  
Cache-Control: no-cache  
Postman-Token: 2403845e-ec8c-48cb-a9f9-bbf0fab749a6  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  
- Тело запроса:
```
[
{
"id":  3,
"idBook":  2,
"firstName":  "First Name 2",
"lastName":  "Last Name 2",
"title":  "Book 1"
}
]
```
- Заголовки ответа:  
Content-Type: application/json; charset=utf-8; v=1.0  
Date: Wed, 27 Sep 2023 06:59:24 GMT  
Server: Kestrel  
Transfer-Encoding: chunked  
api-supported-versions: 1.0  
- Тело ответа:
```
[
{
"id":  3,
"idBook":  2,
"firstName":  "First Name 2",
"lastName":  "Last Name 2"
}
]
```

### PUT Тест 208 - Проверка нагрузки ответа по id

- URL https://{{baseurl}}/Authors/11
- Ожидаемый результат: HTTP Status: 200 ОК, Тело ответа содержит данные, согласно запросу  
- Заголовки запроса:  
Content-Type: application/json  
User-Agent: PostmanRuntime/7.33.0  
Accept: */*  
Cache-Control: no-cache  
Postman-Token: 390306d9-f958-4d1f-bc59-3b0ad12c18f9  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  
- Тело запроса:
```
[
{
"id":  11,
"idBook":  2,
"firstName":  "First Name 2",
"lastName":  "Last Name 2",
"title":  "Book 1"
}
]
```
- Заголовки ответа:  
Content-Type: application/json; charset=utf-8; v=1.0  
Date: Wed, 27 Sep 2023 07:00:39 GMT  
Server: Kestrel  
Transfer-Encoding: chunked  
api-supported-versions: 1.0  
- Тело ответа:
```
[
{
"id":  11,
"idBook":  2,
"firstName":  "First Name 2",
"lastName":  "Last Name 2"
}
]
```

### PUT Тест 209 - Проверка заголовков ответа по id

- URL https://{{baseurl}}/Authors/8
- Ожидаемый результат: HTTP Status: 200 ОК, Выведены заголовки ответа согласно спецификации  
- Заголовки запроса:  
Content-Type: application/json  
User-Agent: PostmanRuntime/7.33.0  
Accept: */*  
Cache-Control: no-cache  
Postman-Token: 951fd18f-4d77-45c3-a078-f3dec2125085
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  
- Тело запроса:
```
[
{
"id":  8,
"idBook":  2,
"firstName":  "First Name 2",
"lastName":  "Last Name 2",
"title":  "Book 1"
}
]
```
- Заголовки ответа:  
Content-Type: application/json; charset=utf-8; v=1.0  
Date: Wed, 27 Sep 2023 07:02:12 GMT  
Server: Kestrel  
Transfer-Encoding: chunked  
api-supported-versions: 1.0  
- Тело ответа:  
```
[
{
"id":  8,
"idBook":  2,
"firstName":  "First Name 2",
"lastName":  "Last Name 2"
}
]
```

### PUT Тест 210 - Проверка базовой работоспособности по id

- URL https://{{baseurl}}/Authors/10
- Ожидаемый результат: HTTP Status: 200 ОК, Получен ответ в разумные сроки, согласно плану тестирования  
- Заголовки запроса:  
Content-Type: application/json  
User-Agent: PostmanRuntime/7.33.0  
Accept: */*  
Cache-Control: no-cache  
Postman-Token: 2bbbb715-956f-4d60-9185-07837bc9077e  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  
-   Тело запроса:
```
[
{
"id":  10,
"idBook":  2,
"firstName":  "First Name 2",
"lastName":  "Last Name 2",
"title":  "Book 1"
}
]
```
- Заголовки ответа:  
Content-Type: application/json; charset=utf-8; v=1.0  
Date: Wed, 27 Sep 2023 07:03:35 GMT  
Server: Kestrel  
Transfer-Encoding: chunked  
api-supported-versions: 1.0  
- Тело ответа:
```
[
{
"id":  10,
"idBook":  2,
"firstName":  "First Name 2",
"lastName":  "Last Name 2"
}
]
```

### PUT Тест 211 - Обновление списка авторов с неверными данными

- URL https://{{baseurl}}/Authors/9
- Ожидаемый результат:  
HTTP Status: 400 Bad Request, список не обновлен  
- Заголовки запроса:  
Content-Type: application/json  
User-Agent: PostmanRuntime/7.33.0  
Accept: */*  
Cache-Control: no-cache  
Postman-Token: ce3192ae-6707-41ab-b58f-9b22a5294ae6  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  
-   Тело запроса:
```
[
{
"id":  ,
"idBook":  2,
"firstName":  "First Name 2",
"lastName":  "Last Name 2",
"title":  "Book 1"
}
]
```
- Заголовки ответа:  
Content-Type: application/problem+json; charset=utf-8  
Date: Wed, 27 Sep 2023 07:05:26 GMT  
Server: Kestrel  
Transfer-Encoding: chunked  
- Тело ответа:
```
[
{
"type":  "https://tools.ietf.org/html/rfc7231#section-6.5.1",
"title":  "One or more validation errors occurred.",
"status":  400,
"traceId":  "00-fa1ea3341d0eb54daa81c30342175cbe-1db831c2c9dc2146-00",
"errors":  {
"$.id":  [
"',' is an invalid start of a value. Path: $.id | LineNumber: 1 | BytePositionInLine: 8."]}
}
]
```

### HEAD Тест 212 - Обновление списка авторов неверным методом

- URL https://{{baseurl}}/Authors/9
- Ожидаемый результат:  
HTTP Status: 405 Method Not Allowed, Выбран неверный метод, список авторов не обновлен  
- Заголовки запроса:  
Content-Type: application/json  
User-Agent: PostmanRuntime/7.33.0  
Accept: */*  
Cache-Control: no-cache  
Postman-Token: d11826d1-6a4b-42bc-b0ee-7f5e6aad4af8  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive
-   Тело запроса:
```
[
{
"id":  1,
"idBook":  2,
"firstName":  "First Name 2",
"lastName":  "Last Name 2",
"title":  "Book 1"
}
]
```
- Заголовки ответа:  
Date: Wed, 27 Sep 2023 07:06:39 GMT  
Server: Kestrel  
Allow: DELETE, GET, PUT  

### PUT Тест 213 - Обновление списка авторов - неполная модель запроса

- URL https://{{baseurl}}/Authors/23
- Ожидаемый результат:  
HTTP Status: 400 Bad Request, Список авторов не обновлен
- Заголовки запроса:  
Content-Type: application/json  
User-Agent: PostmanRuntime/7.33.0  
Accept: */*  
Cache-Control: no-cache  
Postman-Token: 3c911863-1a40-4d1c-828a-2b7f3b23d660  
Host: fakeestai.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  
- Тело запроса:
```
[
{
"id":  1,
"idBook":  2,
"firstName":  ,
"title":  "Book 1"
}
]
```
- Заголовки ответа:  
Content-Type: application/problem+json; charset=utf-8  
Date: Wed, 27 Sep 2023 07:07:45 GMT  
Server: Kestrel  
Transfer-Encoding: chunked  
- Тело ответа:
```
[
{
"type":  "https://tools.ietf.org/html/rfc7231#section-6.5.1",
"title":  "One or more validation errors occurred.",
"status":  400,
"traceId":  "00-0ca191c0092f7f4795234364115be019-6813c43630e9554e-00",
"errors":  {
"$.firstName":  [
"',' is an invalid start of a value. Path: $.firstName | LineNumber: 3 | BytePositionInLine: 15."]}
}
]
```

### DELETE Тест 214 - Удаление авторов по id

- URL https://{{baseurl}}/Authors/25
- Ожидаемый результат:  
HTTP Status: 200 ОК, Авторы с введенным id удалены
- Заголовки запроса:  
User-Agent: PostmanRuntime/7.33.0  
Accept: */*  
Cache-Control: no-cache  
Postman-Token: 4e534818-8841-4106-8646-bad8de971631  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  
- Заголовки ответа:  
Content-Length: 0  
Date: Wed, 27 Sep 2023 07:12:19 GMT  
Server: Kestrel  
api-supported-versions: 1.0  

### DELETE Тест 215 - Проверка корректности кода по id

- URL https://{{baseurl}}/Authors/3
- Ожидаемый результат:  
HTTP Status: 200 ОК, Получен корректный код 
- Заголовки запроса:  
User-Agent: PostmanRuntime/7.33.0  
Accept: */*  
Cache-Control: no-cache  
Postman-Token: f45e47ea-4896-4385-8992-3f51c5be4e15  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  
- Заголовки ответа:  
Content-Length: 0  
Date: Wed, 27 Sep 2023 07:13:38 GMT  
Server: Kestrel  
api-supported-versions: 1.0  

### DELETE Тест 216 - Проверка нагрузки ответа по id

- URL https://{{baseurl}}/Authors/18
- Ожидаемый результат:  
HTTP Status: 200 ОК, Тело ответа содержит данные, согласно запросу  
- Заголовки запроса:  
User-Agent: PostmanRuntime/7.33.0  
Accept: */*  
Cache-Control: no-cache  
Postman-Token: 95f3a437-aeaf-4d3d-bf49-0d2af851651d  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, b  
Connection: keep-alive
- Заголовки ответа:  
Content-Length: 0  
Date: Wed, 27 Sep 2023 07:14:37 GMT  
Server: Kestrel  
api-supported-versions: 1.0  

### DELETE Тест 217 - Проверка заголовков ответа по id

- URL https://{{baseurl}}/Authors/18  
- Ожидаемый результат:  
HTTP Status: 200 ОК, Выведены заголовки ответа согласно спецификации  
- Заголовки запроса:  
User-Agent: PostmanRuntime/7.33.0  
Accept: */*  
Cache-Control: no-cache  
Postman-Token: 292c01ba-3fd2-4a63-91d2-690307229194  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  
- Заголовки ответа:  
Content-Length: 0  
Date: Wed, 27 Sep 2023 07:15:35 GMT  
Server: Kestrel  
api-supported-versions: 1.0  

### DELETE Тест 218 - Проверка базовой работоспособности по id

- URL https://{{baseurl}}/Authors/15
- Ожидаемый результат:  
HTTP Status: 200 ОК, Получен ответ в разумные сроки, согласно плану тестирования  
- Заголовки запроса:  
User-Agent: PostmanRuntime/7.33.0  
Accept: */*  
Cache-Control: no-cache  
Postman-Token: 4da24be2-aa55-407d-b4ab-78e4aeddc1b5  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  
- Заголовки ответа:  
Content-Length: 0  
Date: Wed, 27 Sep 2023 07:16:22 GMT  
Server: Kestrel  
api-supported-versions: 1.0  

### DELETE Тест 219 - Удаление авторов с неверными данными

- URL https://{{baseurl}}/Authors/5500000000
- Ожидаемый результат:  
HTTP Status: 400 Bad Request, Новые данные не отправлены
- Заголовки запроса:  
User-Agent: PostmanRuntime/7.33.0  
Accept: */*  
Cache-Control: no-cache  
Postman-Token: 4f4a1070-bb08-48ee-9768-df5fd0a11f72  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  
- Заголовки ответа:  
Content-Type: application/problem+json; charset=utf-8  
Date: Wed, 27 Sep 2023 07:17:13 GMT  
Server: Kestrel  
Transfer-Encoding: chunked  
- Тело ответа:  
```
[
{
"type":  "https://tools.ietf.org/html/rfc7231#section-6.5.1",
"title":  "One or more validation errors occurred.",
"status":  400,
"traceId":  "00-dc81214911d41246940c4b229775d979-8c978d5883567d42-00",
"errors":  {
"id":  [
"The value '5500000000' is not valid.]}
}
]
```

### OPTIONS Тест 220 - Удаление авторов неверным методом

- URL https://{{baseurl}}/Authors/15
- Ожидаемый результат:  
HTTP Status: 405 Method Not Allowed, Выбран неверный метод, автор не удален  
- Заголовки запроса:  
User-Agent: PostmanRuntime/7.33.0  
Accept: */*  
Cache-Control: no-cache  
Postman-Token: 8251bb17-1474-4ca2-9c3c-b5101f90e2c1  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  
- Заголовки ответа:  
Content-Length: 0  
Date: Wed, 27 Sep 2023 10:15:17 GMT  
Server: Kestrel  

### GET Тест 225 - Проверка корректности кода по id

- URL https://{{baseurl}}/Authors/authors/books/32
- Ожидаемый результат:  
HTTP Status: 200 ОК, Получен корректный код  
- Заголовки запроса:  
User-Agent: PostmanRuntime/7.33.0  
Accept: */*  
Cache-Control: no-cache  
Postman-Token: e8deeb45-03ad-4bae-be01-ffafc0f5577b  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  
- Заголовки ответа:  
Content-Type: application/json; charset=utf-8; v=1.0  
Date: Wed, 27 Sep 2023 10:16:45 GMT  
Server: Kestrel  
Transfer-Encoding: chunked  
api-supported-versions: 1.0  
- Тело ответа:
```[
{
"id":  101,
"idBook":  32,
"firstName":  "First Name 101",
"lastName":  "Last Name 101"
},
{
"id":  102,
"idBook":  32,
"firstName":  "First Name 102",
"lastName":  "Last Name 102"
}
]
```

### GET Тест 226 - Проверка нагрузки ответа по id

- URL https://{{baseurl}}/Authors/authors/books/33
- Ожидаемый результат:  
HTTP Status: 200 ОК, Тело ответа содержит данные, согласно запросу
- Заголовки запроса:  
User-Agent: PostmanRuntime/7.33.0  
Accept: */*  
Cache-Control: no-cache  
Postman-Token: 743cb2d6-e91b-4225-80b3-5c70319033ec  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  
- Заголовки ответа:  
Content-Type: application/json; charset=utf-8; v=1.0  
Date: Wed, 27 Sep 2023 10:17:56 GMT  
Server: Kestrel  
Transfer-Encoding: chunked  
api-supported-versions: 1.0  
- Тело ответа:
```
[
{
"id":  92,
"idBook":  33,
"firstName":  "First Name 92",
"lastName":  "Last Name 92"
},
{
"id":  93,
"idBook":  33,
"firstName":  "First Name 93",
"lastName":  "Last Name 93"
},
{
"id":  94,
"idBook":  33,
"firstName":  "First Name 94",
"lastName":  "Last Name 94"
}
]
```

### GET Тест 227 - Проверка заголовков ответа по id

- URL https://{{baseurl}}/Authors/authors/books/33
- Ожидаемый результат:  
HTTP Status: 200 ОК, Выведены заголовки ответа согласно спецификации
- Заголовки запроса:  
User-Agent: PostmanRuntime/7.33.0  
Accept: */*  
Cache-Control: no-cache  
Postman-Token: 1b5539a4-86fe-422b-83ca-3ede93b878fb  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  
- Заголовки ответа:  
Content-Type: application/json; charset=utf-8; v=1.0  
Date: Wed, 27 Sep 2023 10:19:52 GMT  
Server: Kestrel  
Transfer-Encoding: chunked  
api-supportd-versions: 1.0  
- Тело ответа:
```
[
{
"id":  94,
"idBook":  33,
"firstName":  "First Name 94",
"lastName":  "Last Name 94"
},
{
"id":  95,
"idBook":  33,
"firstName":  "First Name 95",
"lastName":  "Last Name 95"
},
{
"id":  96,
"idBook":  33,
"firstName":  "First Name 96",
"lastName":  "Last Name 96"
},
{
"id":  97,
"idBook":  33,
"firstName":  "First Name 97",
"lastName":  "Last Name 97"
}
]
```

### GET Тест 228 - Проверка базовой работоспособности по id

- URL https://{{baseurl}}/Authors/authors/books/14
- Ожидаемый результат:  
HTTP Status: 200 ОК, Получен ответ в разумные сроки, согласно плану тестирования
- Заголовки запроса:  
User-Agent: PostmanRuntime/7.33.0  
Accept: */*  
Cache-Control: no-cache  
Postman-Token: 6eff1aa2-3752-4c14-b4f7-2ab44336c681  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  
- Заголовки ответа:  
Content-Type: application/json; charset=utf-8; v=1.0  
Date: Wed, 27 Sep 2023 10:20:59 GMT  
Server: Kestrel  
Transfer-Encoding: chunked  
api-supported-versions: 1.0  
- Тело ответа:
```
[
{
"id":  36,
"idBook":  14,
"firstName":  "First Name 36",
"lastName":  "Last Name 36"
},
{
"id":  37,
"idBook":  14,
"firstName":  "First Name 37",
"lastName":  "Last Name 37"
}
]
```

### GET Тест 229 - Получение объекта книги по id с неверными данными

- URL https://{{baseurl}}/Authors/authors/books/15330000000
- Ожидаемый результат:  
HTTP Status: 400 Bad Request, Новые данные не отправлены
- Заголовки запроса:  
User-Agent: PostmanRuntime/7.33.0  
Accept: */*  
Cache-Control: no-cache  
Postman-Token: 3a5b57d4-1b02-4065-840a-796bcf5e2237  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  
- Заголовки ответа:  
Content-Type: application/problem+json; charset=utf-8  
Date: Wed, 27 Sep 2023 10:22:26 GMT  
Server: Kestrel  
Transfer-Encoding: chunked  
- Тело ответа:
```
[
{"type":  "https://tools.ietf.org/html/rfc7231#section-6.5.1",
"title":  "One or more validation errors occurred.",
"status":  400,
"traceId":  "00-19b430898e11fe4e96df57dee7679493-312a70497aa89e43-00",
"errors":  {
"idBook":  [
"The value '15330000000' is not valid."]}}
]
```

### HEAD Тест 230 - Получение объекта книги автора по id неверным методом

- URL https://{{baseurl}}/Authors/authors/books/14
- Ожидаемый результат:  
HTTP Status: 405 Method Not Allowed, Выбран неверный метод, объект не получен
- Заголовки запроса:  
User-Agent: PostmanRuntime/7.33.0  
Accept: */*  
Cache-Control: no-cache  
Postman-Token: bf3e578c-9028-4fe7-9745-8c3a4140451d  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  
- Заголовки ответа:  
Date: Wed, 27 Sep 2023 10:23:39 GMT  
Server: Kestrel  
Allow: GET  

### GET Тест 231 - Получение объекта книги автора по неверному id: производительность

- URL https://{{baseurl}}/Authors/authors/books/8909999800
- Ожидаемый результат:  
HTTP Status: 400 Bad Request, Новые данные не отправлены
- Заголовки запроса:  
User-Agent: PostmanRuntime/7.33.0  
Accept: */*  
Cache-Control: no-cache  
Postman-Token: 6abf3d43-ef01-4caf-b4de-a7876f187005  
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br  
Connection: keep-alive  
- Заголовки ответа:  
Content-Type: application/problem+json; charset=utf-8  
Date: Wed, 27 Sep 2023 10:25:08 GMT  
Server: Kestrel  
Transfer-Encoding: chunked  
- Тело ответа:
```
[
{"type":  "https://tools.ietf.org/html/rfc7231#section-6.5.1",
"title":  "One or more validation errors occurred.",
"status":  400,
"traceId":  "00-52ed94c409690f4fad107b401ee6b204-0385027ca4e16040-00",
"errors":  {
"idBook":  [
"The value '8909999800' is not valid."]}}
]
```

### GET Тест 224 - Получение данных объекта авторов по id 

- URL https://{{baseurl}}/Authors/authors/books/31  
- Ожидаемый результат:  
HTTP Status: 200 ОК, Данные получены  
- Заголовки запроса:  
User-Agent: PostmanRuntime/7.33.0  
Accept: */*  
Cache-Control: no-cache  
Postman-Token: 43d836a1-16f7-4109-a6f4-8197bbddc3a2. 
Host: fakerestapi.azurewebsites.net  
Accept-Encoding: gzip, deflate, br. 
Connection: keep-alive  
- Заголовки ответа:  
Content-Type: application/json; charset=utf-8; v=1.0  
Date: Wed, 27 Sep 2023 18:20:31 GMT  
Server: Kestrel  
Transfer-Encoding: chunked  
api-supported-versions: 1.0  
- Тело ответа:  
```
[
    {
        "id": 92,
        "idBook": 31,
        "firstName": "First Name 92",
        "lastName": "Last Name 92"
    },
    {
        "id": 93,
        "idBook": 31,
        "firstName": "First Name 93",
        "lastName": "Last Name 93"
    },
    {
        "id": 94,
        "idBook": 31,
        "firstName": "First Name 94",
        "lastName": "Last Name 94"
    },
    {
        "id": 95,
        "idBook": 31,
        "firstName": "First Name 95",
        "lastName": "Last Name 95"
    }
]
```







