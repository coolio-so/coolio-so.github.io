---
title: Sonar 분석시 SVN Plugins E170001 Authentication 에러⁠
author: coolioso
date: 2023-07-21 00:00:00 +0800
categories: [개발이야기, DevOPS, Sonar]
tags: [ E1770001, error, sonar, svn, DevOPS ]
---

## 문제점

> 젠킨스에서 Sonar 배포시에 `SVN Plugins`에 따른 인증 오류가 발생된다.

![](../cms-assets/posts/2023/0721/Sonar-plugin-e170001-step1.png){: .normal}

## 해결 방법

- Sonar의 관리자에서 `SVN` 탭을 선택하여 `Disable the SCM Sensor`를 비활성화 시켜준다.

![Sonar System Configuration - SVN](../cms-assets/posts/2023/0721/Sonar-plugin-e170001-step2.png){: .normal}

- 또는 해당되는 `SVN`에 접속할 수 있는 계정 정보를 입력한다.
  - 해당 정보에서 분석시에 코드를 작성한 개발자의 아이디 정보를 가져온다.
