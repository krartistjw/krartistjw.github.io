---
layout: default
title: WorkoutAPI
has_children: true
nav_order: 51
---

# 운동 API

## 개요


## 사전 준비 사항
1.  회원 가입
2.  로그인
    1.  로그인 시 발행되는 **access token key**를 헤더에 `Authorization: Bearer {ACCESS_TOKEN}` 값을 설정
3. API 요청


## 운동 API 레퍼런스

### 운동 리스트 조회

#### 설명
운동 리스트 조회 API 입니다.

#### 요청 URL
|HTTP 메서드|URL|
|---|------|
|GET|api.energyboostlab.com/workout/|

#### 파라미터
|파라미터|타입|필수여부|설명|
|----|---|---|------|
|테스트|테스트|Y|테스트|

#### Request Example
```javascript
GET /workout/ HTTP/1.1
Host: api.energyboostlab.com
Content-Type: application/json
Authorization: Bearer {ACCESS_TOKEN}
{

}
```

#### Response Example
```javascript
Content-Type: application/json
Authorization: Bearer {ACCESS_TOKEN}
charset=UTF-8
{

}
```

#### Return Code
|구분|코드|내용|설명|
|----|---|---|------|
|성공|200|성공|OK|
|실패|401|권한 없음|API 사용 권한이 없습니다|
||403|비정상 접근|잘못된 요청입니다|
||404|존재하지 않은 요청|존재하지 않은 요청입니다|
||500|시스템 에러|테스트|

### 운동 상세 조회

#### 설명
운동 상세 조회 API 입니다.

#### 요청 URL
|HTTP 메서드|URL|
|---|------|
|GET|api.energyboostlab.com/workout/{ID}|

#### 파라미터
|파라미터|타입|필수여부|설명|
|----|---|---|------|
|테스트|테스트|Y|테스트|

#### Request Example
```javascript
GET /workout/{ID}/ HTTP/1.1
Host: api.energyboostlab.com
Content-Type: application/json
Authorization: Bearer {ACCESS_TOKEN}
{

}
```

#### Response Example
```javascript
Content-Type: application/json
Authorization: Bearer {ACCESS_TOKEN};
charset=UTF-8
{

}
```

#### Return Code
|구분|코드|내용|설명|
|----|---|---|------|
|성공|200|성공|OK|
|실패|401|권한 없음|API 사용 권한이 없습니다|
||403|비정상 접근|잘못된 요청입니다|
||404|존재하지 않은 요청|존재하지 않은 요청입니다|
||500|시스템 에러|테스트|


### 운동 생성

#### 설명
운동 생성 API 입니다.

#### 요청 URL
|HTTP 메서드|URL|
|---|------|
|POST|api.energyboostlab.com/workout/|

#### 파라미터
|파라미터|타입|필수여부|설명|
|----|---|---|------|
|테스트|테스트|Y|테스트|

#### Request Example
```javascript
POST /workout/ HTTP/1.1
Host: api.energyboostlab.com
Content-Type: application/json
Authorization: Bearer {ACCESS_TOKEN}
{

}
```

#### Response Example
```javascript
Content-Type: application/json
Authorization: Bearer {ACCESS_TOKEN}
charset=UTF-8
{

}
```

#### Return Code
|구분|코드|내용|설명|
|----|---|---|------|
|성공|200|성공|OK|
|실패|401|권한 없음|API 사용 권한이 없습니다|
||403|비정상 접근|잘못된 요청입니다|
||404|존재하지 않은 요청|존재하지 않은 요청입니다|
||500|시스템 에러|테스트|


### 운동 수정

#### 설명
운동 수정 API 입니다.

#### 요청 URL
|HTTP 메서드|URL|
|---|------|
|PUT|api.energyboostlab.com/workout/{ID}|

#### 파라미터
|파라미터|타입|필수여부|설명|
|----|---|---|------|
|테스트|테스트|Y|테스트|

#### Request Example
```javascript
PUT /workout/{ID}/ HTTP/1.1
Host: api.energyboostlab.com
Content-Type: application/json
Authorization: Bearer {ACCESS_TOKEN}
{

}
```

#### Response Example
```javascript
Content-Type: application/json
Authorization: Bearer {ACCESS_TOKEN}
charset=UTF-8
{

}
```

#### Return Code
|구분|코드|내용|설명|
|----|---|---|------|
|성공|200|성공|OK|
|실패|401|권한 없음|API 사용 권한이 없습니다|
||403|비정상 접근|잘못된 요청입니다|
||404|존재하지 않은 요청|존재하지 않은 요청입니다|
||500|시스템 에러|테스트|


### 운동 삭제

#### 설명
운동 리스트 조회 API 입니다.

#### 요청 URL
|HTTP 메서드|URL|
|---|------|
|DELETE|api.energyboostlab.com/workout/{ID}/|

#### 파라미터
|파라미터|타입|필수여부|설명|
|----|---|---|------|
|테스트|테스트|Y|테스트|

#### Request Example
```javascript
DELETE /workout/{ID}/ HTTP/1.1
Host: api.energyboostlab.com
Content-Type: application/json
Authorization: Bearer {ACCESS_TOKEN}
{

}
```

#### Response Example
```javascript
Content-Type: application/json
Authorization: Bearer {ACCESS_TOKEN}
charset=UTF-8
{

}
```

#### Return Code
|구분|코드|내용|설명|
|----|---|---|------|
|성공|200|성공|OK|
|실패|401|권한 없음|API 사용 권한이 없습니다|
||403|비정상 접근|잘못된 요청입니다|
||404|존재하지 않은 요청|존재하지 않은 요청입니다|
||500|시스템 에러|테스트|


