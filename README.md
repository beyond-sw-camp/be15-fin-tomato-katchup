<table>
  <tr>
    <td align="center"><img src="https://github.com/user-attachments/assets/16718841-7a79-4187-86f9-4134cd4aae6c" width="1300" /></td>
    <td align="center"><img src="https://github.com/user-attachments/assets/12bbb73f-0bcf-40bc-ba8b-62eb5d9a2d83" width="1300"/></td>
    <td align="center"><img src="https://github.com/user-attachments/assets/a5947ee8-37e2-4173-a958-75f46a2d2df7" width="1300"/></td>
    <td align="center"><img src="https://github.com/user-attachments/assets/4d70299d-f045-464c-bbb7-270c0b316086" width="1300"/></td>
    <td align="center"><img src="https://github.com/user-attachments/assets/d09d3065-f01a-415c-8c6c-492f6a966d10" width="1300"/></td>
    <td align="center"><img src="https://github.com/user-attachments/assets/4f097953-3860-4d2e-8203-fc791a10ac71" width="1300"/></td>
  </tr>
  <tr>
    <td align="center"><a href="https://github.com/Jangwoo0710">박장우</a></td>
    <td align="center"><a href="https://github.com/Joonspar">박준서</a></td>
    <td align="center"><a href="https://github.com/oyk0510">오유경</a></td>
    <td align="center"><a href="https://github.com/lddocy">윤채영</a></td>
    <td align="center"><a href="https://github.com/kkkwid">이승재</a></td>
    <td align="center"><a href="https://github.com/Cho-Hyun-Seung">조현승</a></td>
  </tr>
</table>

# 🍅 KATCHUP 프로젝트

> **MCN 기업 전용 광고주 관리 및 캠페인 협업을 위한 CRM 플랫폼**

---

## 📍 목차

<a href="#1">1. 프로젝트 기획</a>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<a href="#1-1">1-1. 프로젝트 소개</a>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<a href="#1-2">1-2. 주요 기능</a>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<a href="#1-3">1-3. 기술 스택</a>

<a href="#2">2. 설계 문서</a>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<a href="#2-1">2-1. 요구사항 명세서</a>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<a href="#2-2">2-2. WBS</a>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<a href="#2-3">2-3. ERDCloud</a>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<a href="#2-4">2-4. FIGMA 화면 설계서</a>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<a href="#2-5">2-5. 아키텍처 구조도</a>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<a href="#2-6">2-6. 프로그램 사양서(REST API 명세서)</a>

<a href="#3">3. Back & Front 테스트 결과 </a>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<a href="#3-1">3-1. 백엔드 단위 테스트 결과서</a>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<a href="#3-2">3-2. 프론트엔드 UI/UX 단위 테스트 결과서</a>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<a href="#3-3">3-3. GIT 브랜치 전략</a>

<a href="#4">4. 시스템 통합 </a>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<a href="#4-1">4-1. CI/CD 계획서</a>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<a href="#4-2">4-2. 통합 테스트 결과서</a>

<a href="#5">5. 트러블 슈팅 </a>

<a href="#6">6. 팀원 회고 </a>
<br>

---

## <p id="1"> 🪐 1. 프로젝트 기획</p>

## <p id="1-1">1-1. 프로젝트 소개</p>

### 📌 프로젝트 개요

**프로젝트명**: `KATCHUP`  
**주제**: MCN 기업의 광고주 중심 B2B 협업을 효율화하는 CRM 시스템

---

### 🖼️ 프로젝트 배경

KATCHUP은 인플루언서 콘텐츠 관리, 캠페인 성과 분석, 계약서 처리, 커뮤니케이션 이력 등 광고주와의 관계를 중심으로 업무를 통합 관리하는 플랫폼입니다.
MCN(Multi-Channel Network) 기업은 유튜브와 인스타그램 등 다양한 플랫폼에서 인플루언서 마케팅을 진행하지만, 현재까지의 업무 방식은 플랫폼별 데이터 분석, 광고 성과 관리, 광고주 커뮤니케이션, 계약 문서 처리 등을 각각 개별적으로 운영하는 데에 많은 한계가 존재합니다. 유튜브와 인스타그램의 콘텐츠 데이터를 통합적으로 조회하거나, 광고한 영상의 성과를 체계적으로 분석할 수 있는 시스템이 부재하고, 기획부터 계약까지 이어지는 전체 캠페인 파이프라인을 통합 관리하기 어려워 담당자들의 수작업 부담과 정보 누락 가능성이 높습니다. 또한 반복적으로 작성되는 제안서나 계약서 같은 문서는 템플릿화가 되어 있지 않아 효율적인 업무 처리가 어렵습니다. 이러한 비효율성과 단절된 업무 흐름을 해결하기 위해, KATCHUP은 광고주 중심의 업무 프로세스를 하나의 CRM 시스템으로 통합하고, 인플루언서 콘텐츠 성과 분석, 캠페인 파이프라인 단계별 관리, 계약서 템플릿 기반 자동화 등을 통해 MCN 기업의 운영 효율성과 데이터 기반 의사결정을 지원하고자 합니다.

---

### 🗓️ 프로젝트 기간

- **시작일**: 2025년 5월 28일
- **종료일**: 2025년 7월 21일
- **총 기간**: 54일

---

### 🎯 프로젝트 목표

- 광고주–인플루언서 협업 과정 시스템화 및 자동화
- 캠페인 성과 통합 분석 및 시각화
- 문서 기반 업무 전자화 및 이력 관리
- 고객 커뮤니케이션 이력 기록 및 만족도 측정

---

### 👥 타겟 사용자

- MCN 기업의 마케팅 실무자 및 캠페인 담당자
- 콘텐츠 기획/제안 담당자
- 광고주 관리 책임자
- 인플루언서 운영 관리자

---

### 📈 시장 배경

- 인플루언서 마케팅 시장은 **2025년 약 28조 원 규모**로 성장 전망
- MCN 기업 내 업무는 여전히 **엑셀/수기 중심**
- 캠페인 성과 수집, 계약서 처리 등에서 **효율성 저하**  
  → KATCHUP은 이러한 한계를 해결하는 전용 CRM 시스템입니다.

---

### 💡 기대 효과

- ✅ 반복 업무 자동화 (제안/계약/견적/매출 등)
- ✅ 커뮤니케이션 체계화
- ✅ 콘텐츠 및 수익 통계 기반 분석
- ✅ 문서 전자화
- ✅ 고객 만족도 향상 (설문 기반 피드백)

---

### 🚀 추가 개발 제안

- AI 기반 콘텐츠 추천 기능
- Google Calendar API 연동
- TikTok, X(Twitter) 연동 확장
- 광고주 전용 외부 포털 뷰 제공

---

## <p id="1-2">1-2. ⚙️ 주요 기능</p>

### 🔎 1. 인플루언서 계정 및 성과 분석

- YouTube, Instagram 연동
- 평균 조회수, 구독자 변화율, 시청자 분석
- 인기 콘텐츠 자동 분류 및 캠페인별 성과 분석

### 📊 2. 캠페인 대시보드

- 콘텐츠 유입 경로, 검색 비율 분석
- 성과 리포트 생성 및 자동 전송

### 💼 3. 파이프라인 및 영업 기회 관리

- 제안서, 견적서, 계약서 등록 및 의견 관리
- 계약서 PDF 업로드/전송

### 💰 4. 매출 및 문서 관리

- 계약 기반 매출 등록 및 문서 이력 자동화

### 👤 5. 광고주 및 고객사 관리

- 광고 업체 및 담당자 관리, 메일 전송
- 커뮤니케이션 이력 통합 관리

### 💬 6. 채팅 및 커뮤니케이션

- 실시간 채팅, 파일 첨부, 읽음 여부 확인

### ⏰ 7. 알림 및 일정 기능

- 계약 상태 및 이벤트 알림
- 팀/개인 일정 관리

---

## <p id="1-3">1-3. 🛠️ 기술 스택</p>

<div align="center">

<h3>Backend & DB</h3>
<div dir="auto">
<img src="https://img.shields.io/badge/java-007396?style=for-the-badge&logo=java&logoColor=white"/>
<img src="https://img.shields.io/badge/springboot-6DB33F?style=for-the-badge&logo=springboot&logoColor=white">
<img src="https://img.shields.io/badge/Spring%20Security-6DB33F?style=for-the-badge&logo=springsecurity&logoColor=white"/>
<img src="https://img.shields.io/badge/JWT-000000?style=for-the-badge&logo=JSON%20web%20tokens&logoColor=white"/>
<img src="https://img.shields.io/badge/gradle-02303A?style=for-the-badge&logo=gradle&logoColor=white">
<img src="https://img.shields.io/badge/mariaDB-003545?style=for-the-badge&logo=mariaDB&logoColor=white">
<img src="https://img.shields.io/badge/MongoDB-47A248?style=for-the-badge&logo=mongodb&logoColor=white">
<img src="https://img.shields.io/badge/Redis-FF4438?style=for-the-badge&logo=redis&logoColor=white">
<img src="https://img.shields.io/badge/git-F05032?style=for-the-badge&logo=git&logoColor=white">
<img src="https://img.shields.io/badge/Firebase-FFCA28?style=for-the-badge&logo=Firebase&logoColor=black" />
</div>

<h3>Frontend</h3>
<div dir="auto">
<img src="https://img.shields.io/badge/html5-E34F26?style=for-the-badge&logo=html5&logoColor=white"> 
<img src="https://img.shields.io/badge/css-1572B6?style=for-the-badge&logo=css3&logoColor=white"> 
<img src="https://img.shields.io/badge/javascript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black"> 
<img src="https://img.shields.io/badge/vue.js-4FC08D?style=for-the-badge&logo=vue.js&logoColor=white"> 
<img src="https://img.shields.io/badge/bootstrap-7952B3?style=for-the-badge&logo=bootstrap&logoColor=white">
<img src="https://img.shields.io/badge/tailwindcss-%2338B2AC.svg?style=for-the-badge&logo=tailwind-css&logoColor=white"/>
<img src="https://img.shields.io/badge/vite-%23646CFF.svg?style=for-the-badge&logo=vite&logoColor=white"/>
</div>

<h3>Devops</h3>
<div dir="auto">
<img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=Docker&logoColor=white"/>
<img src="https://img.shields.io/badge/Terraform-7B42BC?style=for-the-badge&logo=Terraform&logoColor=white"/>
<img src="https://img.shields.io/badge/GitHub_Actions-2088FF?style=for-the-badge&logo=github-actions&logoColor=white" />
<img src="https://img.shields.io/badge/AWS_ECR-FF9900?style=for-the-badge&logo=amazon-aws&logoColor=white" />

</div>

<h3>Tools & Communication</h3>
<div dir="auto">
<img src="https://img.shields.io/badge/github-181717?style=for-the-badge&logo=github&logoColor=white">
<img src="https://img.shields.io/badge/Postman-FF6C37?style=for-the-badge&logo=Postman&logoColor=white"/>
<img src="https://img.shields.io/badge/ERDCLOUD-339AF0?style=for-the-badge&logoColor=white">
<img src="https://img.shields.io/badge/Notion-000000?style=for-the-badge&logo=notion&logoColor=white">
<img src="https://img.shields.io/badge/-Swagger-%23Clojure?style=for-the-badge&logo=swagger&logoColor=white"/>
<img src="https://img.shields.io/badge/jira-%230A0FFF.svg?style=for-the-badge&logo=jira&logoColor=white"/>
<img src="https://img.shields.io/badge/Figma-F24E1E?style=for-the-badge&logo=figma&logoColor=white"/>
<img src="https://img.shields.io/badge/Discord-5865F2?style=for-the-badge&logo=discord&logoColor=white"/>
</div>
</div>

---

## <p id="2"> 2. 📁 설계 문서</p>

## <p id="2-1">2-1. 요구사항 명세서</p>

[![요구사항명세서](https://img.shields.io/badge/요구사항명세서-바로가기-yellow?style=for-the-badge)](https://docs.google.com/spreadsheets/d/1q12NH0h5hOcvCFU6CqA1my5h5tuPUZwJ_3G9Ezj80LA/edit?gid=759019660#gid=759019660)

---

## <p id="2-2">2-2. WBS</p>

[![WBS](https://img.shields.io/badge/WBS-바로가기-pink?style=for-the-badge)](https://docs.google.com/spreadsheets/d/1q12NH0h5hOcvCFU6CqA1my5h5tuPUZwJ_3G9Ezj80LA/edit?gid=764235756#gid=764235756)

---

## <p id="2-3">2-3. ERDCloud</p>

[![화면설계서](https://img.shields.io/badge/ERDCLoud-바로가기-purple?style=for-the-badge)](https://www.erdcloud.com/d/oHcHYPjm2Z4JXpG8f)
![image](https://github.com/user-attachments/assets/add751a8-5c6c-4e84-8c81-1c0aa7f10b80)

---

## <p id="2-4">2-4. FIGMA 화면 설계서</p>

[![화면설계서](https://img.shields.io/badge/Figma-바로가기-blue?style=for-the-badge)](https://www.figma.com/design/qBcsAhrNiPfBEJJqcAIGZk/%F0%9F%8D%85?node-id=0-1&t=q3nKm5IJwOSsfwtd-1)

---

## <p id="2-5">2-5. 아키텍처 구조도</p>

[![화면설계서](https://img.shields.io/badge/Architecture-바로가기-red?style=for-the-badge)](https://file.notion.so/f/f/d5de5c40-db63-8184-b2a5-00036fc324c3/feb97e5b-0d4b-4936-8108-4e3847f189db/%EC%95%84%ED%82%A4%ED%85%8D%EC%B2%98_%EA%B5%AC%EC%A1%B0%EB%8F%84.png?table=block&id=217e5c40-db63-8066-9741-fa2604c03940&spaceId=d5de5c40-db63-8184-b2a5-00036fc324c3&expirationTimestamp=1750377600000&signature=ZcBROztnF72hEGIFp6Z2Z47BoWMNGVdKxQm2zEEpT18&downloadName=%EC%95%84%ED%82%A4%ED%85%8D%EC%B2%98+%EA%B5%AC%EC%A1%B0%EB%8F%84.png)
![아키텍처 구조도](https://github.com/user-attachments/assets/19ae487f-6bfd-46a7-83b3-5c994f851e1f)

---

## <p id="2-6">2-6. 프로그램 사양서 (REST API 명세서)</p>
[![REST API 명세서](https://img.shields.io/badge/REST_API-바로가기-green?style=for-the-badge)](https://cho-hyun-seung.github.io/apidocs/dist/index.html)
<details>
<summary>📄 API 명세서 보기</summary>

<br>

<img alt="api 명세서" src="https://github.com/user-attachments/assets/55805390-7bee-47ea-ac49-cb4b20001051" />

</details>

## <p id="3"> 3. 🌸 Back & Front 테스트 결과</p>

## <p id="3-1">3-1. 백엔드 단위 테스트 결과서</p>

<img alt="localhost_63342_be15-fin-tomato-katchup-BE_build_reports_tests_test_index html__ijt=4nbt8fj5k9dvemcib5fq7gsjgq _ij_reload=RELOAD_ON_SAVE" src="https://github.com/user-attachments/assets/a6e9501b-01e4-4eff-ae0f-6195e4226a2f" />

---

## <p id="3-2">3-2. 프론트엔드 UI/UX 단위 테스트 결과서</p>

<details>
<summary><strong>회원</strong></summary>
<div>

<h4>로그인 & 로그아웃</h4>
<img src="https://github.com/user-attachments/assets/ca9b4bce-00b8-4bd8-8308-11be748d99fe" alt="로그인 로그아웃">

<h4>비밀번호 찾기</h4>
<img src="https://github.com/user-attachments/assets/97e4201d-40e0-4d66-a697-9632edb0931a" alt="비밀번호 찾기(임시비번)">

<h4>비밀번호 변경</h4>
<img src="https://github.com/user-attachments/assets/1b6fb0ed-5047-462a-bd85-95a60be4f30b" alt="비밀번호 변경">

<h4>개인정보 및 프로필사진 수정</h4>
<img src="https://github.com/user-attachments/assets/89594c2d-76d1-41c2-90ef-7bd736205403" alt="개인정보 및 프로필사진 수정">

<h4>내 인플루언서 목록 조회</h4>
<img src="https://github.com/user-attachments/assets/8c319149-0213-42b5-94bc-36652367a802" alt="내 인플루언서 목록 조회">

</div>
</details>

<details>
<summary><strong>인플루언서 관리</strong></summary>
<div>

<h4>인플루언서 목록 조회</h4>
<img src="https://github.com/user-attachments/assets/bf852699-dd01-4938-9b34-f3cd2281a79e" alt="인플루언서 목록 조회">

<h4>인플루언서 등록</h4>
<img src="https://github.com/user-attachments/assets/37c75438-14ac-4766-9a36-7100c9f05181" alt="인플루언서 등록">

<h4>인플루언서 검색</h4>
<img src="https://github.com/user-attachments/assets/9cb1f508-533b-48d8-aa9d-a396ce15b487" alt="인플루언서 검색">

<h4>인플루언서 수정</h4>
<img src="https://github.com/user-attachments/assets/c4d486e3-c076-4c3f-9509-4e7088a0a0cf" alt="인플루언서 수정">

<h4>인플루언서 삭제</h4>
<img src="https://github.com/user-attachments/assets/1c40e4fa-ce63-446a-8970-4ee37907ccc1" alt="인플루언서 삭제">

</div>
</details>

<details>
<summary><strong>AI 인플루언서 추천 매칭</strong></summary>
<div>

<img src = "https://github.com/user-attachments/assets/a15d6b29-a32a-40a0-afe6-300f958b3fc7" alt="AI 추천 매칭">

</div>
</details>

<details>
<summary><strong>유튜브 대시보드</strong></summary>
<div>

<h4>유튜브 대시보드 1</h4>
<img src="https://github.com/user-attachments/assets/40e79450-fdfa-447d-ab42-fe2284d2f629" alt="유튜브 대시보드 1">

<h4>유튜브 대시보드 2</h4>
<img src="https://github.com/user-attachments/assets/9508d559-2262-46bc-98e5-c010271a1925" alt="유튜브 대시보드 2">

</div>
</details>

<details>
<summary><strong>인스타그램 대시보드</strong></summary>
<div>

<h4>인스타그램 대시보드 1</h4>
<img src="https://github.com/user-attachments/assets/f3a6bf7a-b754-47c8-8fd6-1eeef3c02e13" alt="인스타그램 대시보드 1">

<h4>인스타그램 대시보드 2</h4>
<img src="https://github.com/user-attachments/assets/f1a2e61b-7a9e-4c4f-b0e8-7fcbbbb6e8b3" alt="인스타그램 대시보드 2">

</div>
</details>

<details>
<summary><strong>파이프라인</strong></summary>
<div>

<h4>파이프라인 목록 조회</h4>
<img src="https://github.com/user-attachments/assets/118aa32c-02d1-4353-a974-e60318ddf299" alt="파이프라인 목록 조회">

<h4>파이프라인 상세 조회</h4>
<img src="https://github.com/user-attachments/assets/dac7890d-76c0-44ad-ad85-1dd8499f56b9" alt="파이프라인 상세 조회">

<h4>파이프라인 등록</h4>
<img src="https://github.com/user-attachments/assets/14fc249e-da61-4030-9357-48c692e1ba5e" alt="파이프라인 등록">

<h4>파이프라인 수정</h4>
<img src="https://github.com/user-attachments/assets/6e31f3be-ab80-4ca2-b8b2-65cc9b4bee62" alt="파이프라인 수정">

<h4>파이프라인 삭제</h4>
<img src="https://github.com/user-attachments/assets/b75aca6d-9b30-4d0c-ac85-7226fa8bd91d" alt="파이프라인 삭제">

</div>
</details>

<details>
<summary><strong>계약서</strong></summary>
<div>

<h4>계약서 등록</h4>
<img src="https://github.com/user-attachments/assets/a09b87b8-9904-4b6b-9488-364d9d2838b4" alt="계약서 등록_converted">

<h4>템플릿 등록</h4>
<img src="https://github.com/user-attachments/assets/a1b01ceb-3129-4341-8f2f-af060b50159e" alt="계약서 템플릿 등록_converted">

<h4>템플릿 목록 조회</h4>
<img src="https://github.com/user-attachments/assets/0c7da040-f02c-4e7c-9e90-9cc38eab5a19" alt="계약서 템플릿 목록 조회_converted">

<h4>계약서 다운로드</h4>
<img src="https://github.com/user-attachments/assets/4e7be909-f549-47b1-bc80-7eed61b6c0a6" alt="계약서 다운로드 조회_converted">

<h4>이메일 전송</h4>
<img src="https://github.com/user-attachments/assets/2f7529c9-aad4-420a-86fe-49260562db75" alt="계약서 이메일 전송_converted">

</div>
</details>

<details>
<summary><strong>알림</strong></summary>
<div>

<h4>전체 조회</h4>
<img src="https://github.com/user-attachments/assets/8ab4db71-8a32-4c13-99fc-01fac86c64b8" alt="알림 전체 조회 GIF">

<h4>알림 확인</h4>
<img src="https://github.com/user-attachments/assets/af65bf03-bfea-4fea-bc08-4e87428fc93e" alt="알림 확인 GIF">

<h4>수신 개수 조회</h4>
<img src="https://github.com/user-attachments/assets/c97deaa7-3ba6-423d-b61d-4735abf97518" alt="알림 수신 개수 조회 GIF">

<h4>알림 삭제</h4>
<img src="https://github.com/user-attachments/assets/88524b99-f642-4ce5-a3f7-2bfdc90a887a" alt="알림 삭제 GIF">

</div>
</details>

<details>
<summary><strong>고객 관리</strong></summary>
<div>

<details>
<summary><strong>고객사</strong></summary>
<div>
  <h4>고객사 목록 조회</h4>
  <img src="https://github.com/user-attachments/assets/e264d34c-7bc4-4744-8b1c-3970ac93cae8" alt="고객사 목록 조회">

  <h4>고객사 상세 조회</h4>
  <img src="https://github.com/user-attachments/assets/c49ddcf5-f0e1-4dd3-99ee-b69b0f21f779" alt="고객사 상세 조회">

  <h4>고객사 등록</h4>
  <img src="https://github.com/user-attachments/assets/b2c5cde8-0de6-44d9-942e-c202d1913641" alt="고객사 등록">

  <h4>고객사 수정</h4>
  <img src="https://github.com/user-attachments/assets/0967c19e-b1cc-4176-b455-4ecc851924ae" alt="고객사 수정">

  <h4>고객사 삭제</h4>
  <img src="https://github.com/user-attachments/assets/9ac1e3b7-4c7e-4771-9876-473b551c1061" alt="고객사 삭제">

</div>
</details>

<details>
<summary><strong>고객사원</strong></summary>
<div>
  <h4>고객사원 등록</h4>
  <img src="https://github.com/user-attachments/assets/4d16a71e-b5a8-4138-a9d5-13acb33f3b05" alt="고객사원 등록">

  <h4>고객사원 수정</h4>
  <img src="https://github.com/user-attachments/assets/ae78e204-e033-411c-910e-dc66547e05ec" alt="고객사원 수정">

  <h4>고객사원 삭제</h4>
  <img src="https://github.com/user-attachments/assets/d617450e-95d3-4733-a9e8-e285ba21faa1" alt="고객사원 삭제">
</div>
</details>

<details>
<summary><strong>만족도 조사 목록</strong></summary>
<div>
<img src="https://github.com/user-attachments/assets/f0adaca9-b985-49b4-826d-eac01a188e17" alt="만족도 조사 목록">
</div>
</details>

<details>
<summary><strong>캠페인 성과 대시보드</strong></summary>
<div>
<h4>캠페인 컨텐츠 정보 조회</h4>
<img src="https://github.com/user-attachments/assets/44fcd577-1087-458d-a1b1-bd848d532274" alt="캠페인 컨텐츠 정보 조회">

<h4>유입 분석 & 수익 요약</h4>
<img src="https://github.com/user-attachments/assets/16dc9a33-f880-4155-90c5-23ce85b46b78" alt="유입 분석, 수익 요약 조회">

<h4>검색 비율 조회</h4>
<img src="https://github.com/user-attachments/assets/7b8c4f2a-0048-40ae-acdc-31cac87f82a2" alt="검색 비율 조회">
</div>
</details>

</div>
</details>

<details>
<summary><strong>이메일 시스템</strong></summary>
<div>

<h4>만족도 평가 요청</h4>
<img src="https://github.com/user-attachments/assets/0b8cfe79-c7a5-4616-95f8-0cb44fccf860" alt="만족도 평가 요청_converted">

<h4>만족도 평가 조회</h4>
<img src="https://github.com/user-attachments/assets/bb5c35ca-b737-416a-a611-396796e149ef" alt="만족도 평가 조회_converted">

</div>
</details>

<details>
<summary><strong>채팅</strong></summary>
<div>

<h4>채팅방 생성</h4>
<img src="https://github.com/user-attachments/assets/b31b8fb1-4340-42ad-9f67-67ec0204f2a8" alt="채팅방 생성">

<h4>채팅방 퇴장</h4>
<img src="https://github.com/user-attachments/assets/1101ab87-d976-4d3e-b6eb-80ae7637e8f6" alt="채팅방 나가기">

<h4>목록/읽지 않은 메시지/마지막 메시지</h4>
<img src="https://github.com/user-attachments/assets/8cd8a5cc-c3ce-41e6-bf9f-c9082837e5e6" alt="채팅방 목록, 읽지 않은 메세지 수, 마지막 수신 메세지 조회">

<h4>메시지 전송</h4>
<img src="https://github.com/user-attachments/assets/90ddf175-4baa-4aa8-b07f-c7a8dcd59356" alt="메세지 전송">

<h4>채팅방 검색</h4>
<img src="https://github.com/user-attachments/assets/9e87e4f6-5892-4ad0-aa7d-cb23c4b1e59c" alt="채팅방 검색">

<h4>채팅방 초대</h4>
<img src="https://github.com/user-attachments/assets/f147eb93-4bb4-4244-8f0e-0618fe8998c1" alt="채팅방 초대">

</div>
</details>

<details>
<summary><strong>캘린더</strong></summary>
<div>

<h4>일정 조회 (개인/파이프라인)</h4>
<img src="https://github.com/user-attachments/assets/e1806b43-d8ae-470b-b235-b62e5e8c31c6" alt="개인 일정 파이프라인 일정 조회">

<h4>일정 등록</h4>
<img src="https://github.com/user-attachments/assets/b70a4dd1-f3f8-463f-aaf5-0ea4af8098c6" alt="캘린더 일정 등록">

<h4>일정 수정</h4>
<img src="https://github.com/user-attachments/assets/abda9fe8-183c-47b1-9220-f54c827317fa" alt="캘린더 일정 수정">

<h4>일정 삭제</h4>
<img src="https://github.com/user-attachments/assets/a3cd8511-2aed-4c1f-84b3-3fd53d3f5491" alt="캘린더 일정 삭제">

</div>
</details>

<details>
<summary><strong>메인 대시보드</strong></summary>
<div>

<img src="https://github.com/user-attachments/assets/04f64326-e77a-4333-b279-76687e3c02d5" alt="메인대시보드">

</div>
</details>

---

## <p id="3-3">3-3. GIT 브랜치 전략</p>

### ✅ 브랜치 전략

|  브랜치 이름  |                        용도                          |
| ------------- | ---------------------------------------------------- |
| `main`        | 운영 배포용 브랜치. 항상 안정적인 상태를 유지         |
| `dev`         | 개발 통합 브랜치. 기능 개발 브랜치들이 머지되는 대상  |
| `feat`, `TMT` | 기능 개발 브랜치                                     |
| `fix`         | 버그 수정 브랜치                                     |
| `chore`       | 설정, 배포, 문서 작업 등 기타 작업용 브랜치           |
| `hotfix`      | 긴급 수정 및 배포 브랜치                             |

### ✅ 기능 브랜치 네이밍 컨벤션

- 형식: `TMT-{이슈번호}-{be|fe}-{간단한설명}`

```
예시 : TMT-19-fe-광고업체-등록-페이지-구현
```

### ✅ 커밋 컨벤션

`[타입]: 작업 내용` 형태로 커밋 컨벤션 구성

| 타입       | 설명                      | 예시 커밋 메시지                  |
| ---------- | ------------------------- | --------------------------------- |
| `feat`     | 새로운 기능 추가          | `feat: 로그인 기능 구현`          |
| `fix`      | 버그 수정                 | `fix: 비밀번호 오류 수정`         |
| `chore`    | 빌드/배포/설정 관련 잡무  | `chore: CI 파이프라인 수정`       |
| `refactor` | 리팩토링 (기능 변화 없음) | `refactor: 중복 코드 정리`        |
| `test`     | 테스트 코드 추가 및 수정  | `test: 회원가입 유닛 테스트 추가` |
| `hotfix`   | 운영 중 긴급 버그 수정    | `hotfix: API 응답 오류 수정`      |

---

## <p id="4"> 4. 시스템 통합</p>

## <p id="4-1">4-1. CI/CD 계획</p>
### 4-1-1. 백엔드 CI/CD 계획
<img src="https://github.com/user-attachments/assets/01e36ef6-a9f8-4fce-8455-0a7053f4eada" width="50%" />

### 4-1-2. 프론트엔드 CI/CD 계획
<img src="https://github.com/user-attachments/assets/dd2a0388-aad5-4d3a-8418-fed3dd48a2aa" width="50%" />

## <p id="4-2">4-2. 통합 테스트 결과서</p>

[![통합_테스트_결과서](https://img.shields.io/badge/통합_테스트_결과서-바로가기-green?style=for-the-badge)](https://docs.google.com/spreadsheets/d/1q12NH0h5hOcvCFU6CqA1my5h5tuPUZwJ_3G9Ezj80LA/edit?gid=1250570749#gid=1250570749)

---

## <p id="5"> 5. 트러블 슈팅</p>

### ✅ [TOMATO] JWT 에러 상태 값 수정하기

#### 1️⃣ 문제 상황

Axios 인터셉터를 활용하여 JWT 만료 시 토큰을 재발급하는 로직을 구성하려고 했으나,  
서버로부터 오는 에러 응답의 상태 코드가 항상 `500` 또는 `400`으로 고정되어 있었다.  
JWT 토큰 만료와 같은 인증 관련 에러는 `401 Unauthorized`로 받고 싶었다.

#### 2️⃣ 문제 해결 시도

#### 🔸 1. `@ExceptionHandler`로 처리 시도 ❌

- `BusinessException`을 핸들링하는 `GlobalExceptionHandler`에 로깅 추가

```java
@RestControllerAdvice
@Slf4j
public class GlobalExceptionHandler {

    @ExceptionHandler(BusinessException.class)
    public ResponseEntity<ApiResponse<Void>> handleBusinessException(BusinessException e) {
        ErrorCode errorCode = e.getErrorCode();
        log.error("에러코드 : {}", errorCode.getHttpStatus());
        ApiResponse<Void> response = ApiResponse.failure(errorCode.getCode(), errorCode.getMessage());
        return new ResponseEntity<>(response, errorCode.getHttpStatus());
    }
}
```

🔸 2. JwtErrorResponse를 통해 명시적으로 상태 코드 지정 ⭕

- 기존에는 검증 실패 시 단순히 예외를 던졌기 때문에 Spring Security의 기본 예외 처리기가 500을 반환
- JwtErrorResponse를 활용하여 직접 상태 코드를 설정하도록 변경.

🔧 개선 전 코드

```java
if (token != null && jwtTokenProvider.validateToken(token)) {
    // 검증 실패 시 예외 발생
}
```

🔧 개선 후 코드

```java
public class JwtAuthenticationFilter extends OncePerRequestFilter {

    private final JwtTokenProvider jwtTokenProvider;
    private final JwtErrorResponse jwtErrorResponse;

    @Override
    protected void doFilterInternal(HttpServletRequest request, HttpServletResponse response, FilterChain filterChain)
        throws ServletException, IOException {
        try {
            String upgradeHeader = request.getHeader("Upgrade");
            if ("websocket".equalsIgnoreCase(upgradeHeader)) {
                filterChain.doFilter(request, response);
                return;
            }

            String token = parseToken(request);
            if (token != null && jwtTokenProvider.validateToken(token)) {
                // 인증 성공 로직
                ...
            }

            filterChain.doFilter(request, response);
        } catch (BusinessException e) {
            jwtErrorResponse.setErrorResponse(response, e.getErrorCode()); // ✅ 에러 상태 코드 직접 지정
        } catch (Exception e) {
            jwtErrorResponse.setErrorResponse(response, GlobalErrorCode.INTERNAL_SERVER_ERROR);
        }
    }
}
```

#### 3️⃣ 결과

- 백엔드에서 JWT 토큰 오류 시 401 Unauthorized 상태 코드를 정상적으로 응답
- 프론트엔드는 해당 응답을 감지하여 토큰을 재발급 받고 기존 요청을 자동 재시도
- 최종적으로 JWT 재발급 로직이 안정적으로 동작함을 확인

---

---

## <p id="6"> 6. 🤝 팀원 회고</p>

|  이름  | 회고 |
| :----: | :--- |
| 조현승 | 이번 프로젝트를 수행하면서 단순히 기능 구현을 넘어서, 서비스 전체 흐름을 이해하고 운영까지 고려한 개발의 중요성을 깊이 느꼈습니다. 서브쿼리, 윈도우 함수, CTE, 다중 JOIN 등을 직접 활용해 복잡한 데이터를 처리하는 경험 자체가 큰 도전이었고, 그 과정에서 SQL 작성 능력과 데이터 해석력이 눈에 띄게 향상되었습니다. 또한, 배포 단계에서는 Terraform을 통해 AWS 인프라를 코드로 구성하고, GitHub Actions를 활용한 CI/CD 자동화를 구축함으로써 인프라 설계와 배포 자동화에 대한 실질적인 경험을 쌓을 수 있었습니다. |
| 이승재 | 이번 프로젝트를 통해 기술적인 성장뿐 아니라 협업과 커뮤니케이션의 중요성을 다시 한번 느꼈다. 새로운 기술(FCM, SSE, 외부API연동)을 실제 서비스에 적용해보면서 실무 감각을 익힐 수 있었고, 문제 상황에 직접 부딪히며 해결하는 경험을 통해 개발자로서 자신감도 생긴거 같다. 아쉬운 점도 있었지만, 이를 통해 다음 프로젝트에서는 더 효율적으로 일할 수 있을 거란 확신이 들었다. |
| 윤채영 | 이번 프로젝트를 통해 계획 수립(WBS)과 팀 내 소통의 중요성을 깊이 체감했습니다. 유튜브·인스타그램 API 데이터를 수집·가공하고, 스케줄러를 통한 자동 업데이트 구조를 구축하며 백엔드 운영 경험을 쌓았습니다. AWS 인프라(ECS, RDS, S3 등)를 활용해 처음으로 도메인을 구매하고 실제 배포까지 수행한 점이 큰 성과였습니다. 각 페이지별 테스트와 버그 수정으로 완성도를 높였고, 특히 UX 설계의 중요성을 실감할 수 있었습니다.     |
| 오유경 | 이번 최종 프로젝트 토마토 케찹은 단순한 기능 구현을 넘어, 기획부터 배포까지 전 과정을 팀과 함께 완성해본 뜻깊은 경험이었습니다. 처음으로 B2B 서비스를 기획하고 구현하며, 기능에 대한 감이 없는 상태에서 시작했지만 시장 조사와 사용자 리서치, 반복적인 회의를 통해 방향성과 핵심 기능을 명확히 정리해갈 수 있었습니다. 서로 다른 의견을 조율하며 진짜 협업이 무엇인지 체감했고, 단순히 코드를 작성하는 것을 넘어서 서비스 관점에서 문제를 바라보는 시야도 함께 키울 수 있었습니다. 또한 GitHub, Jira, Notion, Discord 등 협업 툴을 적극 활용하며 현업에 가까운 개발 문화를 실습해본 경험이 큰 자산이 되었습니다. |
| 박준서 | 파이널 프로젝트는 이전까지 경험했었던 프로젝트와 많이 달랐던 것을 느꼈다. 기획부터 구현과 배포까지 했던 점이 꽤 많은 노력을 하여서 뿌듯하다고 느낀다. 이번 부트캠프가 아니었다면, 수많은 기술들을 다루지 못하였다고 생각을 하였고 이번 부트캠프를 통해 기술적인 부분 뿐만 아니라 협업적인 부분에서도 많은 성장을 했다고 생각한다. 부트캠프가 끝나고 나서도 이 경험을 통해 회사나 다른 프로젝트에서 많은 성장을 할 수 있기를 기대한다. |
| 박장우 | 벌써 5번째 수행해보는 프로젝트이다 보니 꽤 많이 익숙해져서 감도 많이 잡힌 것 같고 팀원들과 소통하고 협업하는 것에도 많이 능숙해진 것 같다. 전체적인 6개월을 돌이켜봤을 때 우리가 평소에 사용하는 프로그램이 어떤 식으로 이루어져 있고 또 어떻게 만들어지는지를 직접 해봄으로써 잘 알 수 있게 되었고 특히 이번 최종 프로젝트는 주제가 실무와 밀접하게 연관되어 있었던 만큼 현업에 대한 이해도까지 같이 올릴 수 있었기에 매우 좋은 경험이 되었다. 팀원들의 도움을 받아 내 역할을 해낼 수 있었던 경험도 값진 것이었지만 한편으로는 많은 역할을 하지 못했던 건 아쉬움으로 남는다. 이번 최종 프로젝트 경험을 밑거름 삼아 졸업프로젝트를 포함한 앞으로 수행해나갈 많은 과제들에서 좋은 성과를 낼 수 있도록 개인적인 노력을 기울여야겠다. |

---

<div align="center">
  <b>Made with 💖 by Team TOMATO</b><br/>
  <i>“Catch up with your campaign. Catch up with KATCHUP.”</i>
</div>
