---
title: (Eclipse) Team Ignore 설정
description:
author: coolioso
date: 2022-08-17 00:00:00 +0800
categories: [개발이야기, Eclipse]
tags: [ eclipse, Ignore, SCM, svn, Team, 환경설정]
pin: false
math: true
mermaid: true
---

> 이클립스가 실행되는 개별 환경에 따라서 동적으로 생되는 파일 목록은 형상관리 대상에서 제외
>
> 형상관리에 올라가면 안되는 파일에 대한 설정


```
# Git 관련 이력 폴더
.git
*/.git/*

# SVN 관련 이력 폴더
.svn
*/.svn/*

# 개인별 이클립스 프로젝트 설정 파일
.settings
*/.settings/*
.classpath
.project

# 자바 빌드시에 생성되는 빌드 결과 폴더
bin
*/bin/*

# Gralde 빌드시에 생성되는 빌드 결과 폴더
build
*/build/*

# 스프링 설정시 생성되는 설정정보
.springBeans

# Maven 빌드시에 생성되는 빌드 결과 폴더
target
*/target/*

# 프로젝트 내에서 생성되는 로그 폴더
logs

# NPM 작업으로 생성되는 라이브러리
node_modules
*/node_modules/*
dist
*/dist/*

# NPM에 따른 동적 생성 파일
# 컴파일 시점에 생성되는 파일로 공유되는 개발자들간의 동일 환경을 위해서는 해당 파일로 올라가야 함
# 개발 환경 구성에 따른 선택사항
# package-lock.json
```