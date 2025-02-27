---
title: (Eclipse) Java Save Action 설정
description:
author: coolioso
date: 2022-08-18 00:00:00 +0800
categories: [개발이야기, Eclipse]
tags: [ action, eclipse, java, save, SaveAction, 이클립스 ]
pin: false
math: true
mermaid: true
---

## Java Save Actions 설정

> 자바 코드 수정 후에 저장시에 자동으로 지정된 액션을 수행한다.
>
> 불필요한 코드 및 코드 포맷에 대한 일치화를 위한 작업

 

### Save Actions 활성화

`Preferences > Java > Editor > Save Actions`

1. `Perform the selected actions on save` 체크

2. `Addtional actions` 체크
- 저장시에 추가적인 액션에 대한 정의

![Save Actions 설정 창](../../cms-assets/posts/2022/0818/java-save-action-step1.png){: .normal}

#### Code Organizing

- Formatter 설정
  - 공백 제거 : `Remove trailing whitespace > All lines`
  - 들여쓰기 : `Correct indentation`

![Code Organizing 설정](../../cms-assets/posts/2022/0818/java-save-action-step2.png){: .normal}

#### Code Style

- Control statements 설정
  - 블록 구분자 : `Use blocks in if/while/for/do statements > Always`

![Code Style 설정](../../cms-assets/posts/2022/0818/java-save-action-step3.png){: .normal}

#### Missing Code

- Annotations

  - 어노테이션 추가 : `Add missing Annotations`

    - `@Override`
    - `@Deprecated

![Missing Code 설정](../../cms-assets/posts/2022/0818/java-save-action-step4.png){: .normal}

#### Unnecessary Code

- Unused code
  - 불필요한 Imports 제거 : `Remove unused imports`
- Unnecessary code
  - 불필요한 Cast 제거 : `Remove unnecessary casts`
  - 불필요한 `$NON-NLS$` 태그 제거 : `Remove unnecessary '$NON-NLS$' tags`

![Unused Code](../../cms-assets/posts/2022/0818/java-save-action-step5.png){: .normal}