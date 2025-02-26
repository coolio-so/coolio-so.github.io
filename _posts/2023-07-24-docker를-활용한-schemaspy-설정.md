---
title: Docker를 활용한 SchemaSpy 설정
author: coolioso
date: 2023-07-24 00:00:00 +0800
categories: [개발이야기, Docker]
tags: [ docker, docker-compose, pgsql, postgres, schemaspy ]
---

> SchemaSpy는 데이터베이스에 있는 스키마의 메타데이터를 분석하여 HTML 기반으로 볼 수 있는 시각적 표현을 생성해주는 Java 기반의 분석 도구입니다.  
> HTML 링크와 엔티티 관계 다이어그램으로 표시되는 하위 및 상위 테이블 관계를 보여주는 ERD를 제공합니다.

 

# docker-compose.yml

```yaml
version: '3'

services:
  schemaspy:
    image: schemaspy/schemaspy:snapshot
    container_name: "schemaspy-demo"
    volumes:
      - ./output:/output
      - ./config:/config
    command:[
      "-configFile", "/config/schemaspy.properties",
      "-imageformat", "svg"
    ]
```

 

# schemaspy.properties

```properties
# type of database. Run with -dbhelp for details
schemaspy.t=pgsql
# database properties: host, port number, name user, password
schemaspy.host=postgres
schemaspy.port=5432
schemaspy.u=postgres
schemaspy.p=postgres
# db scheme for which generated diagrams
schemaspy.s=public
```

 

## 참고자료

- Schemaspy : https://schemaspy.org/
- 설정 값 : https://schemaspy.readthedocs.io/en/latest/started.html#configuration
