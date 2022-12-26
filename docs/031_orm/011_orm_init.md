---
layout: default
parent: ORM
title: 사전 준비
nav_order: 11
---

# 사전 준비

## 프로젝트 생성
1. IntelliJ 실행

1. 프로젝트 생성
- 상단 메뉴 File -> New -> Project 선택

1. Spring initializr로 프로젝트 생성
- Type: Gradle
- JDK:JDK 11
- Packaging: War  

![orm](../../assets/images/031_orm/orm2.png)


- 라이브러리 선택(Lombok, Spring Web, Spring DataJPA, H2 Database)

![orm](../../assets/images/031_orm/orm3.png)

- build.gradle dependencies 확인
  - JPA 필수 라이브러리: spring-boot-starter-data-jpa
  ![orm](../../assets/images/031_orm/orm4.png)

- application.yml 파일 생성
  - application.properties 파일 확장자 yml로 변경
  ![orm](../../assets/images/031_orm/orm5.png)
