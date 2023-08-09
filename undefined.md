---
description: Agent 성능 측정 결과입니다.
---

# 성능

## 테스트 조건

메시지 건수: 50만건&#x20;

(3개의 통합 메시지 20만건, 2개의 통합 메시지 20만건, 단건 발송 메시지 10만건 발송)

send session 개수: 20개

## 테스트 결과

<table><thead><tr><th width="98">DB</th><th width="80">세션수</th><th width="99">시작 시간</th><th width="104">종료 시간</th><th width="103">진행 시간</th><th width="130">진행 시간(분)</th><th width="84">평균</th><th>전체 평균</th></tr></thead><tbody><tr><td>Oracle</td><td>20개</td><td>16:37:17</td><td>16:49:50</td><td>0:12:33</td><td>12.55</td><td>39841</td><td>39841</td></tr><tr><td>Mysql</td><td>20개</td><td>16:27:20</td><td>16:40:52</td><td>0:13:32</td><td>13.533</td><td>36946</td><td>36946</td></tr><tr><td>Mssql</td><td>20개</td><td>23:16:25</td><td>23:30:44</td><td>0:14:19</td><td>14.317</td><td>34924</td><td>34924</td></tr></tbody></table>
