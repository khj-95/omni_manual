---
description: Agent 성능 측정 결과입니다.
---

# 성능

## 테스트 조건

**메시지 건수**: 50만 건

* 3개의 통합 메시지:  20만 건
* 2개의 통합 메시지: 20만 건
* 단 건 발송 메시지: 10만 건

**send session 개수**: 20개

## 테스트 결과

<table data-full-width="true"><thead><tr><th>DB</th><th>세션수</th><th>시작 시간</th><th>종료 시간</th><th>진행 시간</th><th>진행 시간(분)</th><th>평균</th><th>전체 평균</th></tr></thead><tbody><tr><td>Oracle</td><td>20개</td><td>16:37:17</td><td>16:49:50</td><td>0:12:33</td><td>12.55</td><td>39841</td><td>39841</td></tr><tr><td>Mysql</td><td>20개</td><td>16:27:20</td><td>16:40:52</td><td>0:13:32</td><td>13.533</td><td>36946</td><td>36946</td></tr><tr><td>Mssql</td><td>20개</td><td>23:16:25</td><td>23:30:44</td><td>0:14:19</td><td>14.317</td><td>34924</td><td>34924</td></tr></tbody></table>
