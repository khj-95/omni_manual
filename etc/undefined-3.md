---
description: OMNI Agent 성능 측정 결과입니다.
---

# 성능

## 테스트 조건

### **메시지 건수**: 50만 건

* 3개의 통합 메시지: 20만 건
* 2개의 통합 메시지: 20만 건
* 단 건 발송 메시지: 10만 건

### **send session 개수**: 20개

## 테스트결과

{% hint style="info" %}
처리 속도는 서버 성능 및 네트워크 전송 속도에 따라 차이가 날 수 있습니다.
{% endhint %}

<table data-full-width="false"><thead><tr><th align="center">DB</th><th align="center">세션수</th><th align="center">건수/min</th><th align="center">건수/hour</th></tr></thead><tbody><tr><td align="center">Oracle</td><td align="center">20개</td><td align="center">39841</td><td align="center">2390460</td></tr><tr><td align="center">Mysql</td><td align="center">20개</td><td align="center">36946</td><td align="center">2216760</td></tr><tr><td align="center">Mssql</td><td align="center">20개</td><td align="center">34924</td><td align="center">2095440</td></tr></tbody></table>
