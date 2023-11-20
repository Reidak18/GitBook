# API

## Project

{% swagger method="post" path="/projects" baseUrl="" summary="Create user project" fullWidth="false" %}
{% swagger-description %}
Создает проект пользователя. Записывает в БД
{% endswagger-description %}

{% swagger-parameter in="header" name="Authorization" type="uuid" %}
Bearer user token
{% endswagger-parameter %}

{% swagger-parameter in="query" name="name" type="str" required="true" %}
Project name
{% endswagger-parameter %}

{% swagger-parameter in="header" name="Idempotency-Key" type="uuid" %}

{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
```
{
    "id": uuid,
    "created_at": datetime
}
```
{% endswagger-response %}

{% swagger-response status="401: Unauthorized" description="" %}

{% endswagger-response %}

{% swagger-response status="403: Forbidden" description="" %}

{% endswagger-response %}

{% swagger-response status="409: Conflict" description="" %}

{% endswagger-response %}

{% swagger-response status="422: Unprocessable Entity" description="" %}
```
{
    "code": int,
    "message": str
}
```
{% endswagger-response %}

{% swagger-response status="500: Internal Server Error" description="" %}

{% endswagger-response %}
{% endswagger %}

{% swagger method="get" path="/projects" baseUrl="" summary="List user projects" fullWidth="false" %}
{% swagger-description %}
Показывает все проекты пользователя
{% endswagger-description %}

{% swagger-parameter in="header" name="token" type="uuid" %}
Bearer user token
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
```
[
    {
        "id": uuid,
        "name": str,
        "created_at": datetime
    }
    ...   
]
```
{% endswagger-response %}

{% swagger-response status="401: Unauthorized" description="" %}

{% endswagger-response %}

{% swagger-response status="403: Forbidden" description="" %}

{% endswagger-response %}

{% swagger-response status="500: Internal Server Error" description="" %}

{% endswagger-response %}
{% endswagger %}

{% swagger method="get" path="/projects/{project_id}" baseUrl="" summary="Get project information" fullWidth="false" %}
{% swagger-description %}
Показывает все cцены пользователя в проекте, мета-информация
{% endswagger-description %}

{% swagger-parameter in="header" name="token" type="uuid" %}
Bearer user token
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
```
[
    {
        "id": uuid,
        "name": str,
        "created_at": datetime
    }
    ...   
]
```
{% endswagger-response %}

{% swagger-response status="401: Unauthorized" description="" %}

{% endswagger-response %}

{% swagger-response status="403: Forbidden" description="" %}

{% endswagger-response %}

{% swagger-response status="500: Internal Server Error" description="" %}

{% endswagger-response %}
{% endswagger %}

{% swagger method="put" path="/projects/{project_id}" baseUrl="" summary="Update user projects / Add scenes " fullWidth="false" %}
{% swagger-description %}
Обновляет проект&#x20;
{% endswagger-description %}

{% swagger-parameter in="header" name="token" type="uuid" required="true" %}
Bearer user token
{% endswagger-parameter %}

{% swagger-parameter in="path" name="project_id" type="str" required="true" %}

{% endswagger-parameter %}

{% swagger-parameter in="body" name="name" type="str" required="false" %}

{% endswagger-parameter %}

{% swagger-parameter in="body" name="scenes" type="list" %}
List of scene IDs&#x20;
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}

{% endswagger-response %}

{% swagger-response status="401: Unauthorized" description="" %}

{% endswagger-response %}

{% swagger-response status="403: Forbidden" description="" %}

{% endswagger-response %}

{% swagger-response status="404: Not Found" description="Scene not found" %}

{% endswagger-response %}

{% swagger-response status="500: Internal Server Error" description="" %}

{% endswagger-response %}
{% endswagger %}

{% swagger method="delete" path="/projects/{project_id}" baseUrl="" summary="Delete user project" fullWidth="false" %}
{% swagger-description %}
Создает проект пользователя. Записывает в БД
{% endswagger-description %}

{% swagger-parameter in="header" name="token" type="uuid" %}
Bearer user token
{% endswagger-parameter %}

{% swagger-parameter in="path" name="project_id" type="str" required="true" %}

{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
```
{
    "id": uuid,
    "created_at": datetime
}
```
{% endswagger-response %}

{% swagger-response status="401: Unauthorized" description="" %}

{% endswagger-response %}

{% swagger-response status="403: Forbidden" description="" %}

{% endswagger-response %}

{% swagger-response status="404: Not Found" description="" %}

{% endswagger-response %}

{% swagger-response status="422: Unprocessable Entity" description="" %}

{% endswagger-response %}

{% swagger-response status="500: Internal Server Error" description="" %}

{% endswagger-response %}
{% endswagger %}

## Scene

{% swagger method="get" path="/scenes/" baseUrl="" summary="List all scenes" fullWidth="false" %}
{% swagger-description %}
Показывает все сцены пользователя
{% endswagger-description %}

{% swagger-parameter in="header" name="Authorization" type="uuid" %}
Bearer user token
{% endswagger-parameter %}

{% swagger-parameter in="query" name="name" type="str" required="true" %}
Project name
{% endswagger-parameter %}

{% swagger-parameter in="header" name="Idempotency-Key" type="uuid" %}

{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
```
{
    "id": uuid,
    "created_at": datetime
}
```
{% endswagger-response %}

{% swagger-response status="401: Unauthorized" description="" %}

{% endswagger-response %}

{% swagger-response status="403: Forbidden" description="" %}

{% endswagger-response %}

{% swagger-response status="409: Conflict" description="" %}

{% endswagger-response %}

{% swagger-response status="422: Unprocessable Entity" description="" %}
```
{
    "code": int,
    "message": str
}
```
{% endswagger-response %}

{% swagger-response status="500: Internal Server Error" description="" %}

{% endswagger-response %}
{% endswagger %}

{% swagger method="get" path="/scenes/{scene_id}" baseUrl="" summary="Get scene information" fullWidth="false" %}
{% swagger-description %}
Создает проект пользователя. Записывает в БД
{% endswagger-description %}

{% swagger-parameter in="header" name="Authorization" type="uuid" %}
Bearer user token
{% endswagger-parameter %}

{% swagger-parameter in="query" name="name" type="str" required="true" %}
Project name
{% endswagger-parameter %}

{% swagger-parameter in="header" name="Idempotency-Key" type="uuid" %}

{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
```
{
    "id": uuid,
    "created_at": datetime
}
```
{% endswagger-response %}

{% swagger-response status="401: Unauthorized" description="" %}

{% endswagger-response %}

{% swagger-response status="403: Forbidden" description="" %}

{% endswagger-response %}

{% swagger-response status="409: Conflict" description="" %}

{% endswagger-response %}

{% swagger-response status="422: Unprocessable Entity" description="" %}
```
{
    "code": int,
    "message": str
}
```
{% endswagger-response %}

{% swagger-response status="500: Internal Server Error" description="" %}

{% endswagger-response %}
{% endswagger %}

{% swagger method="put" path="/scenes/{scene_id}" baseUrl="" summary="Update scene information" fullWidth="false" %}
{% swagger-description %}
Создает проект пользователя. Записывает в БД
{% endswagger-description %}

{% swagger-parameter in="header" name="Authorization" type="uuid" %}
Bearer user token
{% endswagger-parameter %}

{% swagger-parameter in="query" name="name" type="str" required="true" %}
Project name
{% endswagger-parameter %}

{% swagger-parameter in="header" name="Idempotency-Key" type="uuid" %}

{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
```
{
    "id": uuid,
    "created_at": datetime
}
```
{% endswagger-response %}

{% swagger-response status="401: Unauthorized" description="" %}

{% endswagger-response %}

{% swagger-response status="403: Forbidden" description="" %}

{% endswagger-response %}

{% swagger-response status="409: Conflict" description="" %}

{% endswagger-response %}

{% swagger-response status="422: Unprocessable Entity" description="" %}
```
{
    "code": int,
    "message": str
}
```
{% endswagger-response %}

{% swagger-response status="500: Internal Server Error" description="" %}

{% endswagger-response %}
{% endswagger %}

{% swagger method="delete" path="/scenes/{scene_id}" baseUrl="" summary="Delete scene " fullWidth="false" %}
{% swagger-description %}
Создает проект пользователя. Записывает в БД
{% endswagger-description %}

{% swagger-parameter in="header" name="Authorization" type="uuid" %}
Bearer user token
{% endswagger-parameter %}

{% swagger-parameter in="query" name="name" type="str" required="true" %}
Project name
{% endswagger-parameter %}

{% swagger-parameter in="header" name="Idempotency-Key" type="uuid" %}

{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
```
{
    "id": uuid,
    "created_at": datetime
}
```
{% endswagger-response %}

{% swagger-response status="401: Unauthorized" description="" %}

{% endswagger-response %}

{% swagger-response status="403: Forbidden" description="" %}

{% endswagger-response %}

{% swagger-response status="409: Conflict" description="" %}

{% endswagger-response %}

{% swagger-response status="422: Unprocessable Entity" description="" %}
```
{
    "code": int,
    "message": str
}
```
{% endswagger-response %}

{% swagger-response status="500: Internal Server Error" description="" %}

{% endswagger-response %}
{% endswagger %}

{% swagger method="post" path="/scenes/{scene_id}/analysis" baseUrl="" summary="Get analysis for photo " fullWidth="false" %}
{% swagger-description %}
Создает проект пользователя. Записывает в БД
{% endswagger-description %}

{% swagger-parameter in="header" name="Authorization" type="uuid" %}
Bearer user token
{% endswagger-parameter %}

{% swagger-parameter in="query" name="name" type="str" required="true" %}
Project name
{% endswagger-parameter %}

{% swagger-parameter in="header" name="Idempotency-Key" type="uuid" %}

{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
```
{
    "id": uuid,
    "created_at": datetime
}
```
{% endswagger-response %}

{% swagger-response status="401: Unauthorized" description="" %}

{% endswagger-response %}

{% swagger-response status="403: Forbidden" description="" %}

{% endswagger-response %}

{% swagger-response status="409: Conflict" description="" %}

{% endswagger-response %}

{% swagger-response status="422: Unprocessable Entity" description="" %}
```
{
    "code": int,
    "message": str
}
```
{% endswagger-response %}

{% swagger-response status="500: Internal Server Error" description="" %}

{% endswagger-response %}
{% endswagger %}

{% swagger method="post" path="/scenes/{scene_id}/run" baseUrl="" summary="Run scene processing" fullWidth="false" %}
{% swagger-description %}
Создает проект пользователя. Записывает в БД
{% endswagger-description %}

{% swagger-parameter in="header" name="Authorization" type="uuid" %}
Bearer user token
{% endswagger-parameter %}

{% swagger-parameter in="query" name="name" type="str" required="true" %}
Project name
{% endswagger-parameter %}

{% swagger-parameter in="header" name="Idempotency-Key" type="uuid" %}

{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
```
{
    "id": uuid,
    "created_at": datetime
}
```
{% endswagger-response %}

{% swagger-response status="401: Unauthorized" description="" %}

{% endswagger-response %}

{% swagger-response status="403: Forbidden" description="" %}

{% endswagger-response %}

{% swagger-response status="409: Conflict" description="" %}

{% endswagger-response %}

{% swagger-response status="422: Unprocessable Entity" description="" %}
```
{
    "code": int,
    "message": str
}
```
{% endswagger-response %}

{% swagger-response status="500: Internal Server Error" description="" %}

{% endswagger-response %}
{% endswagger %}

## Parse

{% swagger method="post" path="/parse" baseUrl="" summary="Parse video into n scenes" %}
{% swagger-description %}
Разделяет видео на сцены - создает в sv папки со сценами - раскадровку
{% endswagger-description %}

{% swagger-parameter in="header" name="token" type="uuid" %}
Bearer user token
{% endswagger-parameter %}

{% swagger-parameter in="query" name="video" type="bytes " required="true" %}
input video
{% endswagger-parameter %}

{% swagger-parameter in="query" name="project_id" type="uuid" %}
Append scenes to project
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
```json
[
    {
       "id": uuid,
       "frame_num": int,
       "duration": datetime
    },
    ...
]

```
{% endswagger-response %}

{% swagger-response status="401: Unauthorized" description="" %}

{% endswagger-response %}

{% swagger-response status="404: Not Found" description="" %}

{% endswagger-response %}

{% swagger-response status="422: Unprocessable Entity" description="" %}
```
{
    ""
}
```
{% endswagger-response %}

{% swagger-response status="500: Internal Server Error" description="" %}

{% endswagger-response %}
{% endswagger %}

## Other
