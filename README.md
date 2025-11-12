# 김동현 Backend Engineer

<table>
  <tr>
    <td>
      <img src="https://github.com/user-attachments/assets/e5faca76-a866-48dd-8427-48426839d0e4" width="120">
    </td>
    <td>
      <b>Phone</b>: 010-6271-7762<br>
      <b>Email</b>: <a href="mailto:kim138762@gmail.com">kim138762@gmail.com</a><br>
      <b>Github</b>: <a href="https://github.com/ehdgusdl">https://github.com/ehdgusdl</a><br>
      <b>Blog</b>: <a href="https://velog.io/@kim138762/posts">https://velog.io/@kim138762/posts</a>
    </td>
  </tr>
</table>

## Summary

- End-to-End 프로젝트를 통해 기획부터 배포까지 리딩 경험

## Education

- 단국대학교 소프트웨어학과 학사 졸업 예정(2021 ~  2027. 02)

## Project

### URL 단축기 / Fullstack 2025.09~ / [Github](https://github.com/Shorten-it)

Skill: springboot, redis, Nginx, postgresql

**[Redis Pub/Sub 기반 캐시 무효화 아키텍처도입]**

- 문제 상황: 만료된 단축 URL 접근 시 Redis 캐시와 DB 데이터 불일치가 발생하여 리디렉션 오류 발생
- 해결 방식: Redis Pub/Sub 기반 캐시 무효화 아키텍처를 도입하여 모든 인스턴스에서 캐시를 동기화
- 성과: 만료 URL 리디렉션 오류율 0% 달성

**[서버 다중화 및 Nginx 로드 밸런서 도입 ]** 

- 문제 상황: 애플리케이션 서버가 1대로 운영되어 트래픽 급증 시 장애 발생
- 해결 방식:  Nginx를 로드 밸런서로 도입하여 트래픽을 분산하는 구조로 변경
- 성과: SPOF 문제 해결 및 장애가 발생해도 중단 없는 고가용성 제공

**[스케쥴러 기반 만료 데이터 삭제]** 

- 문제 상황: 만료 시간이 지난 URL 데이터가 DB에 계속 유지되어 스토리지 낭비
- 해결 방식: 스케줄러를 활용하여 자동화 배치 구현
- 성과: URL 만료 및 삭제 라이프사이클을 100% 자동화하여 운영 리소스 절감

### 피부 분석 서비스 **/** Backend 2025.07~2025.08 /[Github](https://github.com/2025-Techeer-Summer-Bootcamp-Team-J)

Skill: FASTapi, rabbitmq, celery, redis, mysql

**[AI모델 학습]**

- 문제 상황: 일반 멀티모달 LLM을 사용하여도 정확도면에서 신뢰도가 부족문제 발생
- 해결 방식: ResNet-50 모델에 사진 30000장을 학습
- 성과: 사진 분석시 결과 신뢰도 강화

**[RAG 시스템 구축으로 인한 LLM 할루시네이션 억제]**

- 문제 상황: LLM의 피부질환 설명에서 신뢰성 부족 문제가 발생
- 해결 방식: firestorefmf Vector DB와 검색도구로 사용해 관련성 높은 문서를 검색하고 이를 바탕으로 LLM모델이 응답을 생성하는 RAG 시스템 구축
- 성과: LLM의 할루시네이션 억제를 통한 신뢰성 강화

**[rabbitmq, celery를 활용한 비동기 병렬 처리]**

- 문제 상황: python의 GIL로 인한 CPU bound 작업의 비동기 병렬 처리 제약
- 해결 방식: rabbitmq, celery, redis를 사용하여 비동기 병렬 처리 구현
- 성과: 비동기 병렬 처리 도입으로인 한 N개의 사진을 분석 요청하면 N*8초 걸리던 시간이 10~12초로 감소

### **AI 기반 발음 교정 서비스 /** Backend 2024.12 ~ 2025.01 /[Github](https://github.com/2024-WinterBootcamp-Team-E)

Skill: FASTapi, mongoDB, mysql

**[SSE를 활용한 챗봇 시스템 구축]**

- 문제 상황: 비동기 처리 이후에도 챗봇의 답변 생성시 오래걸리는 문제 발생
- 해결 방식: LLM의 응답 stream설정과 SSE를 통해 사용자에게 응답을 chunk단위로 제공
- 성과: LLM의 응답 생성이 끝날 때 까지 기다리지 않고 확인할수 있어 사용자 경험 향상

**[Mongo DB를 활용한 채팅 내역 저장]**

- 문제 상황: 비정형 데이터인 채팅내역을 저장시 오버헤드 발생
- 해결 방식: 스키마 유연성이 장점인 Mongo DB 사용
- 성과: 채팅내역 저장시 오버헤드 감소

**[CI/CD 파이프라인을 통한 PR검사, 배포 자동화]**

- 문제 상황: 개발을 진행시 팀원의 무분별한 병합으로 인한 오류 발생
- 해결 방식: CI/CD 파이프라인을 구축하여 PR검사와 배포를 자동화
- 성과: 빠르고 안정적인 검사를 자동화하여 재발 방지와 팀의 능률 향상

### SKill

- Framework: Springboot, FastAPI
- Database: MySQL, PostgreSQL
- Message Queue and Cashe: RabbitMQ, Redis
- ETC: Docker, GCP, K6, Github Actions


