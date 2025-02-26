---
title: SonarQube Linux 설치
description:
author: coolioso
date: 2023-07-21 00:00:00 +0800
categories: [개발이야기, Sonar]
tags: [DevOPS, install, linux, sonar ]
pin: false
math: true
mermaid: true
---

## SonarQube Linux Requirements

Reference = https://docs.sonarqube.org/display/SONAR/Requirements

Linux를 사용하고 있다면 리눅스의 다음 설정 값을 확인해야 함.

- vm.max_map_count : 262144 이상
- fs.file-max : 65536 이상
- Open 파일 : 65536 이상

 

### 설정값 확인 방법

```shell
sysctl vm.max_map_count
sysctl fs.file-max
ulimit -n
```

 

### 값 설정

```shell
sysctl -w vm.max_map_count=262144
sysctl -w fs.file-max=65536
ulimit -n 65536
```
