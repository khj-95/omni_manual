---
description: config 폴더 내부 dbConfig.yml 설정정보입니다.
---

# DB CONFIGURATION(dbConfig.yml)

## DBMS Connect (JDBC Setting)

```yaml
db:
  vender:
    type: VENDER(ORACLE, MYSQL, MSSQL, POSTGRE, TIBERO, MARIA, DB2)

  config:
    user: 유저ID
    password: 비밀번호
    ip: IP
    port: PORT
    database-name: DBNAME
    driver-class-name: net.sf.log4jdbc.sql.jdbcapi.DriverSpy
    #ORACLE
    url: jdbc:log4jdbc:oracle:thin:@${db.config.ip}:${db.config.port}:${db.config.database-name}
    #MYSQL
    url: jdbc:log4jdbc:mysql://${db.config.ip}:${db.config.port}/${db.config.database-name}
    #MSSQL
    url: jdbc:log4jdbc:sqlserver://${db.config.ip}:${db.config.port};SelectMethod=cursor;DatabaseName=${db.config.database-name};encrypt=false;trustServerCertificate=false;
    #POSTGRE
    url: jdbc:log4jdbc:postgresql://${db.config.ip}:${db.config.port}/${db.config.database-name}
    #TIBERO
    url: jdbc:log4jdbc:tibero:thin:@${db.config.ip}:${db.config.port}:${db.config.database-name}
    #MARIA
    url: jdbc:log4jdbc:mariadb://${db.config.ip}:${db.config.port}/${db.config.database-name}?useUnicode=true&noAccessToProcedureBodies=true
    #DB2
    url: jdbc:log4jdbc:db2://${db.config.ip}:${db.config.port}/${db.config.database-name}

    # ORACLE, TIBERO 일 경우 추가
    table-space: TABLE-SPACE-NAME
    table-index-space: TABLE-INDEX-SPACE-NAME
```

## LOG 테이블 설정

```yaml
#-------------------------------------------------------------------------------
# log 테이블 설정
# 로그 데이터 월별 테이블 사용 여부 (N:사용안함, Y:사용함)
#-------------------------------------------------------------------------------
  log: 
    seperate:
      yn: Y
```
