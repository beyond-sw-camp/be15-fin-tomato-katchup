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

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<a href="#3-3">3-3. git 형상관리</a>

<a href="#4">4. 시스템 통합 </a>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<a href="#4-1">4-1. 통합 테스트 결과서</a>

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
<img src="https://github.com/user-attachments/assets/ca9b4bce-00b8-4bd8-8308-11be748d99fe" alt="로그인 로그아웃 GIF">

<h4>비밀번호 찾기</h4>
<img src="https://github.com/user-attachments/assets/97e4201d-40e0-4d66-a697-9632edb0931a" alt="비밀번호 찾기(임시비번)_converted">

<h4>비밀번호 변경</h4>
<img src="https://github.com/user-attachments/assets/fda0e661-67e5-4333-a1ef-63ac10afdd62" alt="비밀번호 변경_converted">

<h4>개인정보 및 프로필사진 수정</h4>
<img src="https://github.com/user-attachments/assets/b140296f-aecf-483a-a12a-ca0708e317a5" alt="개인정보 및 프로필사진 수정_converted">

<h4>내 인플루언서 목록 조회</h4>
<img src="https://github.com/user-attachments/assets/61eb5792-90cc-41ed-acb8-424a3730e181" alt="내 인플루언서 목록 조회_converted">

</div>
</details>

<details>
<summary><strong>인플루언서 관리</strong></summary>
<div>

</div>
</details>

<details>
<summary><strong>유튜브 대시보드</strong></summary>
<div>

<h4>유튜브 대시보드 1</h4>
<img src="https://github.com/user-attachments/assets/807c3c33-c22f-457e-99fe-aa3ad3a65772" alt="유튜브 대시보드 GIF 1_converted">

<h4>유튜브 대시보드 2</h4>
<img src="https://github.com/user-attachments/assets/945cb796-91f4-487e-acb8-b912ffab8cd7" alt="유튜브 대시보드 GIF 2_converted">

</div>
</details>

<details>
<summary><strong>인스타그램 대시보드</strong></summary>
<div>

<img src="https://github.com/user-attachments/assets/7b738c3a-cc59-4b0d-8673-3283d5c8ea75" alt="인스타그램 대시보드 GIF 2_converted">

</div>
</details>

<details>
<summary><strong>파이프라인</strong></summary>
<div>

<h4>수정</h4>
<img src="https://github.com/user-attachments/assets/6e31f3be-ab80-4ca2-b8b2-65cc9b4bee62" alt="파이프라인 수정_converted">

<h4>삭제</h4>
<img src="https://github.com/user-attachments/assets/b75aca6d-9b30-4d0c-ac85-7226fa8bd91d" alt="파이프라인 삭제_converted">

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

<h4>만족도 평가</h4>
<img src="https://github.com/user-attachments/assets/877a6d8b-bb96-40f7-ab87-f22774adbf79" alt="만족도 평가 GIF">

<h4>캠페인 컨텐츠 정보 조회</h4>
<img src="https://github.com/user-attachments/assets/d7749118-bab5-4269-bc79-3834631fb865" alt="캠페인 컨텐츠 정보 조회 GIF">

<h4>유입 분석 & 수익 요약</h4>
<img src="https://github.com/user-attachments/assets/f76c097e-5843-4bb1-aa62-7634d2e2d81d" alt="유입 분석, 수익 요약 조회 GIF">

<h4>검색 비율 조회</h4>
<img src="https://github.com/user-attachments/assets/0f488422-6402-4334-8065-68a8bfb9a461" alt="검색 비율 조회">

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
<img src="https://github.com/user-attachments/assets/b31b8fb1-4340-42ad-9f67-67ec0204f2a8" alt="채팅방 생성 GIF mp4">

<h4>채팅방 퇴장</h4>
<img src="https://github.com/user-attachments/assets/1101ab87-d976-4d3e-b6eb-80ae7637e8f6" alt="채팅방 나가기 GIF mp4">

<h4>목록/읽지 않은 메시지/마지막 메시지</h4>
<img src="https://github.com/user-attachments/assets/8cd8a5cc-c3ce-41e6-bf9f-c9082837e5e6" alt="채팅방 목록, 읽지 않은 메세지 수, 마지막 수신 메세지 조회 GIF mp4">

<h4>메시지 전송</h4>
<img src="https://github.com/user-attachments/assets/90ddf175-4baa-4aa8-b07f-c7a8dcd59356" alt="메세지 전송 GIF mp4">

<h4>채팅방 검색</h4>
<img src="https://github.com/user-attachments/assets/9e87e4f6-5892-4ad0-aa7d-cb23c4b1e59c" alt="채팅방 검색 GIF mp4">

<h4>채팅방 초대</h4>
<img src="https://github.com/user-attachments/assets/f147eb93-4bb4-4244-8f0e-0618fe8998c1" alt="채팅방 초대 GIF mp4">

</div>
</details>

<details>
<summary><strong>캘린더</strong></summary>
<div>

<h4>일정 조회 (개인/파이프라인)</h4>
<img src="https://github.com/user-attachments/assets/e1806b43-d8ae-470b-b235-b62e5e8c31c6" alt="개인 일정 파이프라인 일정 조회 GIF mp4">

<h4>일정 등록</h4>
<img src="https://github.com/user-attachments/assets/b70a4dd1-f3f8-463f-aaf5-0ea4af8098c6" alt="캘린더 일정 등록 GIF">

<h4>일정 수정</h4>
<img src="https://github.com/user-attachments/assets/abda9fe8-183c-47b1-9220-f54c827317fa" alt="캘린더 일정 수정 GIF">

<h4>일정 삭제</h4>
<img src="https://github.com/user-attachments/assets/a3cd8511-2aed-4c1f-84b3-3fd53d3f5491" alt="캘린더 일정 삭제 GIF">

</div>
</details>

<details>
<summary><strong>메인 대시보드</strong></summary>
<div>

<img src="https://github.com/user-attachments/assets/04f64326-e77a-4333-b279-76687e3c02d5" alt="메인대시보드_converted">

</div>
</details>

---

## <p id="3-3">3-3. git 브랜치 전략</p>

### ✅ 브랜치 전략

| 브랜치 이름 | 용도                                                 |
| ----------- | ---------------------------------------------------- |
| `main`      | 운영 배포용 브랜치. 항상 안정적인 상태를 유지        |
| `dev`       | 개발 통합 브랜치. 기능 개발 브랜치들이 머지되는 대상 |
| `feat.`     | 기능 개발 브랜치                                     |
| `fix`       | 버그 수정 브랜치                                     |
| `chore`     | 설정, 배포, 문서 작업 등 기타 작업용 브랜치          |
| `hotfix`    | 긴급 수정 및 배포 브랜치                             |

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

## <p id="4-1">4-1. 통합 테스트 결과서</p>

<img src="https://github.com/user-attachments/assets/f404c410-e163-48b5-bc0d-2b848fcc0d78" alt="통합 테스트 결과서">

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
| 조현승 |      |
| 박준서 |
| 이승재 |      |
| 박장우 |      |
| 윤채영 |      |
| 오유경 |      |

---

<div align="center">
  <b>Made with 💖 by Team TOMATO</b><br/>
  <i>“Catch up with your campaign. Catch up with KATCHUP.”</i>
</div>
