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

- End-to-End 프로젝트를 통해 기획부터 배포까지 리딩한 경험이 있습니다.
- 최신 기술을 맹목적으로 적용하지 않고 각 기술의 장단점을 분석하여 주어진 상황에 최선의 선택을 하는 개발자입니다.

## Education

- 단국대학교 소프트웨어학과 학사 졸업 예정(2021 ~  2027. 02)

### Project

### URL 단축기 / Fullstack 2025.09~ / [Github](https://github.com/Shorten-it)

Skill: Spring Boot, Redis, Nginx, PostgreSQL

**[Redis Pub/Sub 기반 캐시 무효화 아키텍처도입]**

- 문제 상황: URL 만료/삭제 시, 다중화된 서버 인스턴스 간 Redis 캐시 데이터 불일치로 리디렉션 오류 발생.
- 해결 방식: URL 상태 변경 시 특정 Topic으로 메시지를 Publish하고, 모든 인스턴스가 Subscribe하여 즉시 로컬 캐시를 무효화하는 아키텍처 설계 및 도입
- 성과: 만료 URL 접근 시 발생하는 리디렉션 오류율을 0%로 제거하여 데이터 일관성 보장

**[Nginx 로드 밸런싱을 통한 고가용성 확보]** 

- 문제 상황: 단일 서버(SPOF) 운영으로 트래픽 급증 시 장애 발생
- 해결 방식: Nginx를 리버스 프록시로 도입, **Least Connection 방식**의 로드 밸런싱을 적용하여 트래픽 분산
- 성과: SPOF 문제 해결 및 Health Check를 통한 장애 서버 자동 제외로 무중단 고가용성 환경 구축

**[Spring Scheduler 기반 만료 데이터 배치 삭제]** 

- 문제 상황: 만료 시간이 지난 URL 데이터가 DB에 계속 유지되어 스토리지 낭비 및 쿼리 성능 저하
- 해결 방식: Scheduler를 활용하여 만료 된 URL 데이터를 주기적으로 Bulk Delete하는 배치 작업 구현
- 성과: URL 만료 및 삭제 라이프사이클을 100% 구축, 불필요한 데이터 적재를 방지하여 쿼리 성능 저하 예방

### **피부 분석 서비스 / Backend 2025.07~2025.08 /[Github](https://github.com/2025-Techeer-Summer-Bootcamp-Team-J)**

Skill: FASTapi, RabbitMQ, Celery, Redis, MySQL

**[AI모델 학습]**

- 문제 상황: 멀티모달 LLM 사용시 피부 분석 결과의 신뢰도 문제가 발생
- 해결 방식: ResNet-50 모델에 사진 30000장을 학습
- 성과: 피부 질환 분류 정확도를 기존 범용 모델 대비 25% 향상시켜 분석 결과의 신뢰도 강화

**[RAG 시스템 구축으로 인한 LLM 할루시네이션 억제]**

- 문제 상황: LLM의 피부 질환 설명에 의학적 근거가 없거나 부정확한 정보를 생성하는 할루시네이션 문제 발생
- 해결 방식: 피부과 자료를 임베딩하여 Firestore Vector DB에 저장. 사용자 질문 시 관련 문서를 유사도 검색으로 추출, 이를 LLM의 프롬프트 컨텍스트에 주입하여 답변을 생성하는 RAG 시스템 구축
- 성과: LLM 답변의 모든 문장에 검색된 문서를 명시하여 정보 신뢰도 확보

**[Celery/RabbitMQ기반 비동기 병렬 처리로 AI 분석 시간 단축]**

- 문제 상황: Python GIL 제약에 따른 이미지 분석(CPU-Bound) 작업의 성능 병목 현상이 발생
- 해결 방식: 이미지 분석 작업을 Celery Task로 정의하고, RabbitMQ를 메시지 브로커로 사용하여 별도의 Worker 프로세스에서 병렬 처리
- 성과: 비동기 병렬 처리 도입으로 사진 10장 동시 분석 시 총 소요 시간을 10~12초로 단축

### **AI 기반 발음 교정 서비스 / Backend 2024.12 ~ 2025.01 /[Github](https://github.com/2024-WinterBootcamp-Team-E)**

Skill: FASTapi, MongoDB, MySQL

**[SSE를 활용한 챗봇 응답 개선]**

- 문제 상황: LLM의 전체 답변 생성이 완료될 때까지 사용자가 대기해야 하는 지연 문제 발생
- 해결 방식: LLM의 응답을 Stream 방식으로 받아 SSE 프로토콜을 통해 생성되는 텍스트를 Chunk 단위로 즉시 클라이언트에 전송
- 성과: Time To First Byte를 0.5초 이내로 개선하여 체감 대기 시간 90% 이상 단축 및 사용자 경험 향상

**[MongoDB를 활용한 비정형 채팅 데이터 저장]**

- 문제 상황: RDB 사용 시, 텍스트, 음성 인식 결과와 사용자 발음 데이터 저장에 스키마 변경 오버헤드 발생
- 해결 방식: 스키마 유연성이 높은 NoSQL인 MongoDB를 도입, Document 단위로 대화 내역을 저장하여 Read/Write 효율성 증대
- 성과: 향후 신규 기능 추가 시 스키마 변경이 불필요한 유연한 구조를 확보하여 유지보수성 향상

**[Github Actions 기반 CI/CD 파이프라인 구축]**

- 문제 상황: 팀 개발 환경에서 수동 테스트 및 배포로 인한 휴먼 에러 발생
- 해결 방식: Github Actions를 활용하여 PR 생성 시 자동으로 Unit Test 및 Linter를 실행하는 CI 파이프라인 구축, main 브랜치 병합시 개발 서버로 자동 배포 CD 구축
- 성과: PR 검증을 자동화하여, 팀원들이 수동 테스트가 아닌 코드 리뷰에 집중할 수 있는 협업 환경 구축

### SKill

- Framework: Springboot, FastAPI
- Database: MySQL, PostgreSQL
- Message Queue and Cache: RabbitMQ, Redis
- ETC: Docker, GCP, K6, Github Actions

