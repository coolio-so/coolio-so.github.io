---
title: Maven 플러그인을 통한 Sonar 실행
description:
author: coolioso
date: 2023-07-21 00:00:00 +0800
categories: [개발이야기, DevOPS, Maven, Sonar]
tags: [maven, mvn, plugin, sonar ]
pin: false
math: true
mermaid: true
---

## Sonar Maven Plugin 추가

```xml
<plugin>
  <groupId>org.sonarsource.scanner.maven</groupId>
  <artifactId>sonar-maven-plugin</artifactId>
  <version>3.7.0.1746</version>
</plugin>
```

 

## Properties에 Sonar 관련 속성값 추가

```xml
<properties>
	...
  <!-- Sonar Project Configuration -->
  <sonar.projectkey>coolioso-sonar-demo</sonar.projectkey>
  <sonar.projectName>CoolioSo SonarDemo</sonar.projectName>
  <sonar.host.url>http://sonar.domain.com</sonar.host.url>
  <sonar.sourceEncoding>UTF-8</sonar.sourceEncoding>
  
  <sonar.login>Token Key Value</sonar.login>
  
  <sonar.sources>src/main</sonar.sources>
  <sonar.java.binaries>target/classes</sonar.java.binaries>
  <sonar.exclusions>file:**/*.xml</sonar.exclusions>
  <sonar.exclusions>file:**/views/**/*</sonar.exclusions>
  <!--// Sonar Project Configuration -->
</properties>
```

 

## Maven Command

```shell
mvn sonar:sonar
```
