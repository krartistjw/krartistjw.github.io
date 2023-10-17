---
layout: default
grand_parent: EnergyboostAPI
parent: BodyAPI
title: BodyDetail
nav_order: 2
---

# 신체 상세 정보 API

## 개요
골격근, 체지방률 등 신체 상세 정보에 관한 API 입니다

## 사전 준비 사항
1.  회원 가입
2.  로그인
    1.  로그인 시 발행되는 **access token key**를 헤더에 X-CSRFToken 값을 설정
3. API 요청


## 신체 상세 정보 API 레퍼런스

### 신체 상세 정보 리스트 조회

#### 설명
신체 상세 정보 리스트 조회 API 입니다.

#### 요청 URL

|HTTP 메서드|URL|
|:---:|:------|
|GET|api.energyboostlab.com/body/detail/|

#### 파라미터

|파라미터|타입|필수여부|설명|
|:----:|:---:|:---:|:------|
|테스트|테스트|Y|테스트|

#### Request Example
```javascript
GET /body/detail/ HTTP/1.1
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
|:----:|:---:|:---:|------|
|성공|200|성공|OK|
|실패|401|권한 없음|API 사용 권한이 없습니다|
||403|비정상 접근|잘못된 요청입니다|
||404|존재하지 않은 요청|존재하지 않은 요청입니다|
||500|시스템 에러|테스트|

### 신체 상세 정보 상세 조회

#### 설명
신체 상세 정보 상세 조회 API 입니다.

#### 요청 URL

|HTTP 메서드|URL|
|:---:|:------|
|GET|api.energyboostlab.com/body/detail/{ID}/|

#### 파라미터

|파라미터|타입|필수여부|설명|
|:----:|:---:|:---:|:------|
|테스트|테스트|Y|테스트|

#### Request Example
```javascript
GET /body/detail/{ID}/ HTTP/1.1
Host: api.energyboostlab.com
Content-Type: application/json
Authorization: Bearer {ACCESS_TOKEN}
{

}
```

#### Response Example
```javascript
{}
```

#### Return Code

|구분|코드|내용|설명|
|:----:|:---:|:---:|------|
|성공|200|성공|OK|
|실패|401|권한 없음|API 사용 권한이 없습니다|
||403|비정상 접근|잘못된 요청입니다|
||404|존재하지 않은 요청|존재하지 않은 요청입니다|
||500|시스템 에러|테스트|


### 신체 상세 정보 생성

#### 설명
신체 상세 정보 생성 API 입니다.

#### 요청 URL

|HTTP 메서드|URL|
|:---:|:------|
|POST|api.energyboostlab.com/body/detail/|

#### 파라미터

|파라미터|타입|필수여부|설명|
|:----:|:---:|:---:|:------|
|user|Integer|Y|사용자 번호|
|recode_date|String|Y|등록일|
|weight|Integer|Y|체중|
|skeletal_muscle_mass|Integer|N|골격근량|
|percent_body_fat|Integer|N|체지방률|
|body_mass_index|Integer|N|BMI|
|basal_metabolic_rate|Integer|N|기초 대사량|
|total_body_water|Integer|N|체수분|
|protein|Integer|N|단백질|
|minerals|Integer|N|무기질|
|waist_hip_ratio|Integer|N|복부 지방률|
|body_fat_mass|Integer|N|체 지방량|
|visceral_fat_level|Integer|N|내장 지방 레벨|
|height|Integer|N|키|
|body_info|Integer|N|신체 기본정보 아이디|
|muscle_top_left|Integer|N|부위별 근육 분석(상체 왼쪽)|
|muscle_top_right|Integer|N|부위별 근육 분석(상체 오른쪽)|
|muscle_center|Integer|N|부위별 근육 분석(상체 중앙)|
|muscle_bottom_left|Integer|N|부위별 근육 분석(하체 왼쪽)|
|muscle_bottom_right|Integer|N|부위별 근육 분석(하체 오른쪽)|
|fat_top_left|Integer|N|부위별 체지발(상체 왼쪽)|
|fat_top_right|Integer|N|부위별 체지발(상체 오른쪽)|
|fat_center|Integer|N|부위별 체지발(중앙)|
|fat_bottom_left|Integer|N|부위별 체지발(하체 왼쪽)|
|fat_bottom_right|Integer|N|부위별 체지발(하체 오른쪽)|


#### Request Example
```javascript
POST /body/detail/ HTTP/1.1
Host: api.energyboostlab.com
Content-Type: application/json
Authorization: Bearer {ACCESS_TOKEN}
{
    "user": 2,
    "recode_date": "2023-09-01T10:44",
    "weight": 80.0,
    "skeletal_muscle_mass": 33.7,
    "percent_body_fat": 27.3,
    "body_mass_index": 28.0,
    "basal_metabolic_rate": 1642.0,
    "total_body_water": 42.9,
    "protein": 11.8,
    "minerals": 4.21,
    "waist_hip_ratio": 0.86,
    "body_fat_mass": 22.1,
    "visceral_fat_level": 7,
    "height": 165,
    "body_info": 1,
    "muscle_top_left": 3.07,
    "muscle_top_right": 3.17,
    "muscle_center": 25.3,
    "muscle_bottom_left": 9.40,
    "muscle_bottom_right": 9.39,
    "fat_top_left": 2,
    "fat_top_right": 2,
    "fat_center": 2,
    "fat_bottom_left": 2,
    "fat_bottom_right": 2
}
```

#### Response Example
```javascript
{
    "id": 2,
    "user": {
        "id": 2,
        ...
    },
    "body_info": {
        "id": 4,
        "user": {
            "id": 2,
            ...
        },
        "update_date": "2023-10-18T00:45:43.641446",
        "create_date": "2023-10-18T00:45:43.641479",
        "gender": "male",
        "height": 165.0,
        "date_of_birth": "1987-11-18",
        "recode_date": "2023-10-18T00:45:43.637586"
    },
    "update_date": "2023-10-18T00:45:43.652411",
    "create_date": "2023-10-18T00:45:43.652445",
    "total_body_water": 42.9,
    "protein": 11.8,
    "minerals": 4.21,
    "body_fat_mass": 22.1,
    "weight": 80.0,
    "skeletal_muscle_mass": 33.7,
    "body_mass_index": 28.0,
    "percent_body_fat": 27.3,
    "muscle_top_left": 3.07,
    "muscle_top_right": 3.17,
    "muscle_center": 25.3,
    "muscle_bottom_left": 9.4,
    "muscle_bottom_right": 9.39,
    "fat_top_left": 2.0,
    "fat_top_right": 2.0,
    "fat_center": 2.0,
    "fat_bottom_left": 2.0,
    "fat_bottom_right": 2.0,
    "waist_hip_ratio": 0.86,
    "visceral_fat_level": 7.0,
    "basal_metabolic_rate": 1642.0,
    "recode_date": "2023-09-01T10:44:00"
}
```

#### Return Code

|구분|코드|내용|설명|
|:----:|:---:|:---:|------|
|성공|200|성공|OK|
|실패|401|권한 없음|API 사용 권한이 없습니다|
||403|비정상 접근|잘못된 요청입니다|
||404|존재하지 않은 요청|존재하지 않은 요청입니다|
||500|시스템 에러|테스트|


### 신체 상세 정보 수정

#### 설명
신체 상세 정보 수정 API 입니다.

#### 요청 URL

|HTTP 메서드|URL|
|:---:|:------|
|PUT|api.energyboostlab.com/body/detail/{ID}/|

#### 파라미터

|파라미터|타입|필수여부|설명|
|:----:|:---:|:---:|:------|
|user|Integer|Y|사용자 번호|
|recode_date|String|Y|등록일|
|weight|Integer|Y|체중|
|skeletal_muscle_mass|Integer|N|골격근량|
|percent_body_fat|Integer|N|체지방률|
|body_mass_index|Integer|N|BMI|
|basal_metabolic_rate|Integer|N|기초 대사량|
|total_body_water|Integer|N|체수분|
|protein|Integer|N|단백질|
|minerals|Integer|N|무기질|
|waist_hip_ratio|Integer|N|복부 지방률|
|body_fat_mass|Integer|N|체 지방량|
|visceral_fat_level|Integer|N|내장 지방 레벨|
|height|Integer|N|키|
|body_info|Integer|N|신체 기본정보 아이디|
|muscle_top_left|Integer|N|부위별 근육 분석(상체 왼쪽)|
|muscle_top_right|Integer|N|부위별 근육 분석(상체 오른쪽)|
|muscle_center|Integer|N|부위별 근육 분석(상체 중앙)|
|muscle_bottom_left|Integer|N|부위별 근육 분석(하체 왼쪽)|
|muscle_bottom_right|Integer|N|부위별 근육 분석(하체 오른쪽)|
|fat_top_left|Integer|N|부위별 체지발(상체 왼쪽)|
|fat_top_right|Integer|N|부위별 체지발(상체 오른쪽)|
|fat_center|Integer|N|부위별 체지발(중앙)|
|fat_bottom_left|Integer|N|부위별 체지발(하체 왼쪽)|
|fat_bottom_right|Integer|N|부위별 체지발(하체 오른쪽)|

#### Request Example
```javascript
PUT /body/detail/{ID}/ HTTP/1.1
Host: api.energyboostlab.com
Content-Type: application/json
Authorization: Bearer {ACCESS_TOKEN}
{
    "user": 2,
    "recode_date": "2023-09-01T10:44",
    "weight": 80.0,
    "skeletal_muscle_mass": 33.7,
    "percent_body_fat": 27.3,
    "body_mass_index": 28.0,
    "basal_metabolic_rate": 1642.0,
    "total_body_water": 42.9,
    "protein": 11.8,
    "minerals": 4.21,
    "waist_hip_ratio": 0.86,
    "body_fat_mass": 22.1,
    "visceral_fat_level": 7,
    "height": 165,
    "body_info": 1,
    "muscle_top_left": 3.07,
    "muscle_top_right": 3.17,
    "muscle_center": 25.3,
    "muscle_bottom_left": 9.40,
    "muscle_bottom_right": 9.39,
    "fat_top_left": 2,
    "fat_top_right": 2,
    "fat_center": 2,
    "fat_bottom_left": 2,
    "fat_bottom_right": 2
}
```

#### Response Example
```javascript
{
    "id": 2,
    "user": {
        "id": 2,
        ...
    },
    "body_info": {
        "id": 4,
        "user": {
            "id": 2,
            ...
        },
        "update_date": "2023-10-18T00:45:43.641446",
        "create_date": "2023-10-18T00:45:43.641479",
        "gender": "male",
        "height": 165.0,
        "date_of_birth": "1987-11-18",
        "recode_date": "2023-10-18T00:45:43.637586"
    },
    "update_date": "2023-10-18T00:45:43.652411",
    "create_date": "2023-10-18T00:45:43.652445",
    "total_body_water": 42.9,
    "protein": 11.8,
    "minerals": 4.21,
    "body_fat_mass": 22.1,
    "weight": 80.0,
    "skeletal_muscle_mass": 33.7,
    "body_mass_index": 28.0,
    "percent_body_fat": 27.3,
    "muscle_top_left": 3.07,
    "muscle_top_right": 3.17,
    "muscle_center": 25.3,
    "muscle_bottom_left": 9.4,
    "muscle_bottom_right": 9.39,
    "fat_top_left": 2.0,
    "fat_top_right": 2.0,
    "fat_center": 2.0,
    "fat_bottom_left": 2.0,
    "fat_bottom_right": 2.0,
    "waist_hip_ratio": 0.86,
    "visceral_fat_level": 7.0,
    "basal_metabolic_rate": 1642.0,
    "recode_date": "2023-09-01T10:44:00"
}
```

#### Return Code

|구분|코드|내용|설명|
|:----:|:---:|:---:|------|
|성공|200|성공|OK|
|실패|401|권한 없음|API 사용 권한이 없습니다|
||403|비정상 접근|잘못된 요청입니다|
||404|존재하지 않은 요청|존재하지 않은 요청입니다|
||500|시스템 에러|테스트|


### 신체 상세 정보 삭제

#### 설명
신체 상세 정보 삭제 API 입니다.

#### 요청 URL

|HTTP 메서드|URL|
|:---:|:------|
|DELETE|api.energyboostlab.com/body/detail/{ID}/|

#### 파라미터

|파라미터|타입|필수여부|설명|
|:----:|:---:|:---:|:------|
|삭제||||

#### Request Example
```javascript
DELETE /body/detail/{ID}/ HTTP/1.1
Host: api.energyboostlab.com
Content-Type: application/json
Authorization: Bearer {ACCESS_TOKEN}
{}
```

#### Response Example
```javascript
{}
```

#### Return Code

|구분|코드|내용|설명|
|:----:|:---:|:---:|------|
|성공|204|성공|OK|
|실패|401|권한 없음|API 사용 권한이 없습니다|
||403|비정상 접근|잘못된 요청입니다|
||404|존재하지 않은 요청|존재하지 않은 요청입니다|
||500|시스템 에러|테스트|


