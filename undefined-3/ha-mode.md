---
description: 이중화 기능에 관한 설명입니다.
---

# ha mode

* 장애가 발생하더라도, 중단없는 서비스를 위해 AGENT 서버 이중화를 제공합니다.
* Active-Active mode, Active-Standby mode 서비스를 제공합니다.
  * Active-Active: 이중화된 Agent가 모두 동작하는 방식
  * Active-Standby: Primary와 Secondary로 구별하여 Primary 서버의 agent가 메인으로 동작하며 서버 장애 시 Secondary 서버가 자동으로 장애를 감지하고 이어서 전송하는 방식

## 모드 관련 설정

[#ha-mode](../undefined-2/message-configuration.md#ha-mode "mention")

## 설정 용례

### none

```yaml
ha: 
    mode: none
    status: primary
    primary: 
      host: Primary 접속 IP 또는 host
      port: Listen port
```

### Active-Active

```yaml
# Server #1 설정
ha: 
    mode: active-active
    id: E1
    status: primary
    primary: 
      host: Primary 접속 IP 또는 host
      port: Listen port
# Server #2 설정
ha: 
    mode: active-active
    id: E2
    status: secondary
    primary: 
      host: Primary 접속 IP 또는 host
      port: Primary 서버 접속 port
```

### Active-Standby

```yaml
# Server #1 설정
ha: 
    mode: active-standby
    status: primary
    primary: 
      host: Primary 접속 IP 또는 host
      port: Listen port
# Server #2 설정
ha: 
    mode: active-standby
    status: secondary
    primary: 
      host: Primary 접속 IP 또는 host
      port: Primary 서버 접속 port
```
