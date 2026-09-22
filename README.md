<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&amp;color=0:0f172a,100:0ea5a4&amp;height=190&amp;section=header&amp;text=JunBeom%20Bae&amp;fontSize=40&amp;fontColor=ffffff&amp;animation=fadeIn&amp;fontAlignY=38&amp;desc=Backend%2C%20Cloud%2C%20Security-aware%20Engineering&amp;descAlignY=60&amp;descSize=15" alt="JunBeom Bae: Backend, Cloud, Security-aware Engineering" width="100%" />
</p>

<div align="center">

### 아이디어를 실제 서비스로 만들고, 배포와 운영, 보안까지 고민하는 개발자 배준범입니다.

사용자의 불편을 발견하면 직접 구현하고 운영해 보며 답을 찾습니다.  
백엔드와 클라우드를 중심으로 공부하며, 보안 경험을 더해 신뢰할 수 있는 소프트웨어를 만들고 있습니다.

[![GitHub](https://img.shields.io/badge/GitHub-baejun10-0f172a?style=flat-square&logo=github&logoColor=white)](https://github.com/baejun10)
[![Tech Blog](https://img.shields.io/badge/Tech%20Blog-PITAS-0ea5a4?style=flat-square&logo=tistory&logoColor=white)](https://pitas.tistory.com/)

</div>

---

## 🚀 Featured Projects

### CommitMe: GitHub 기반 AI 취업 준비 서비스

> GitHub에 쌓인 개발 경험을 이력서와 면접 준비로 연결하는 서비스

- **문제**: 개발자가 여러 저장소와 커밋에 흩어진 경험을 이력서로 정리하고, 프로젝트 기반 면접을 준비하는 데 많은 시간이 필요했습니다.
- **역할**: 백엔드 API 구현과 클라우드 인프라 구성에 참여하고, 웹 서비스, AI 추론, 채팅처럼 성격이 다른 컴포넌트를 하나의 서비스로 통합했습니다.
- **핵심 구현**: Spring Boot와 FastAPI를 분리하고, 정합성이 중요한 서비스 데이터에는 MySQL을, 유연한 메시지 데이터에는 MongoDB를 사용했습니다. GPU가 필요한 LLM 추론은 RunPod Serverless로 분리했으며 AWS와 Nginx 기반으로 서비스를 배포하고 운영했습니다.
- **배운 점**: 기능 구현을 넘어 서버 간 데이터 흐름, 비동기 작업, 저장소 선택, GPU 비용과 확장성, 장애 대응을 함께 고려하는 아키텍처 설계를 경험했습니다.
- **Tech**<br> ![Spring Boot](https://img.shields.io/badge/Spring%20Boot-6DB33F?style=for-the-badge&logo=springboot&logoColor=white) ![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white) ![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white) ![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=for-the-badge&logo=mongodb&logoColor=white) ![RunPod](https://img.shields.io/badge/RunPod-673AB7?style=for-the-badge) ![AWS](https://img.shields.io/badge/AWS-232F3E?style=for-the-badge&logo=amazonwebservices&logoColor=white) ![Nginx](https://img.shields.io/badge/Nginx-009639?style=for-the-badge&logo=nginx&logoColor=white) ![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)

### AI 상품 비교 서비스

> 디지털 정보 격차를 줄이기 위해 여러 상품의 정보를 LLM으로 비교하는 웹 서비스

- **문제**: 상품 정보가 여러 페이지에 흩어져 있어 사용자가 차이를 직접 비교하고 판단하기 어려웠습니다.
- **역할**: Next.js 기반 프론트엔드와 Django REST Framework 백엔드, OAuth 인증, LLM 상품 비교 기능, 검색 및 CRUD 기능을 구현했습니다.
- **핵심 구현**: GPT와 Gemini API를 활용해 비교 결과를 생성하고 PostgreSQL 검색 기능을 적용했습니다. 한국어 형태소 분석이 제한적인 환경에서는 trigram 기반 검색을 적용하며 검색 엔진 선택의 트레이드오프를 검토했습니다.
- **트러블슈팅**: 분리된 프론트엔드와 백엔드 사이의 HttpOnly 쿠키와 CORS 문제를 SSL과 쿠키 정책 조정으로 해결했습니다. 긴 LLM 응답에서 발생한 Gunicorn timeout은 Nginx, Gunicorn, Django 로그를 함께 대조해 원인을 찾았습니다.
- **Tech**<br> ![Next.js](https://img.shields.io/badge/Next.js-000000?style=for-the-badge&logo=nextdotjs&logoColor=white) ![Django REST Framework](https://img.shields.io/badge/Django%20REST-092E20?style=for-the-badge&logo=django&logoColor=white) ![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white) ![OAuth](https://img.shields.io/badge/OAuth-635BFF?style=for-the-badge) ![LLM API](https://img.shields.io/badge/LLM%20API-8B5CF6?style=for-the-badge) ![Nginx](https://img.shields.io/badge/Nginx-009639?style=for-the-badge&logo=nginx&logoColor=white)

### n8n 기반 지식 자동화

> 웹에서 수집한 기술 자료를 자동으로 정리하고 다시 찾기 쉽게 만드는 개인 지식 파이프라인

- **문제**: Notion Web Clipper로 모은 문서를 매번 읽고 요약해야 했고, 기본 Notion API만으로는 페이지 전체를 원하는 형태로 처리하기 어려웠습니다.
- **역할**: n8n 워크플로우와 Docker 이미지를 직접 구성하고, 문서 변환, LLM 요약, 결과 저장 과정을 자동화했습니다.
- **핵심 구현**: Notion 블록을 Markdown으로 변환한 뒤 LLM으로 요약하고, 다시 Notion 블록으로 변환하는 파이프라인을 만들었습니다. 문서 최상단 삽입이 불가능한 API 제약은 요약 페이지를 별도로 만든 뒤 원문 속성에 연결하는 방식으로 우회했습니다.
- **배운 점**: API가 제공하지 않는 기능을 포기하지 않고 데이터 구조와 오픈소스 도구를 조합해 해결하는 방법을 익혔습니다.
- **Tech**<br> ![n8n](https://img.shields.io/badge/n8n-EA4B71?style=for-the-badge&logo=n8n&logoColor=white) ![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white) ![Notion API](https://img.shields.io/badge/Notion%20API-000000?style=for-the-badge&logo=notion&logoColor=white) ![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=111827) ![LLM API](https://img.shields.io/badge/LLM%20API-8B5CF6?style=for-the-badge)

### 이미지 번역 및 API 분석 프로토타입

> 반복적인 이미지 번역 과정을 자동화하기 위한 보안 연구 및 프로토타이핑

- **문제**: 이미지마다 번역 기능을 수동으로 실행해야 하는 불편을 줄이고, 모바일 애플리케이션의 API 통신 구조를 학습하고자 했습니다.
- **역할**: Android 애플리케이션과 네트워크 트래픽을 분석하고, 요청 생성 과정을 Python으로 재구성한 뒤 브라우저 기반 프로토타입에 연결했습니다.
- **핵심 구현**: JADX, Frida, Burp Suite를 사용해 코드와 통신 흐름을 관찰하고 요청 서명 로직과 multipart 응답 구조를 분석했습니다. 분석 결과를 바탕으로 이미지 요청과 응답 처리를 자동화했습니다.
- **배운 점**: 구현 의도와 실제 동작 사이의 차이를 코드, 런타임, 네트워크 계층에서 교차 검증하는 리버스 엔지니어링 과정을 경험했습니다.
- **Tech**<br> ![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white) ![Android](https://img.shields.io/badge/Android-3DDC84?style=for-the-badge&logo=android&logoColor=111827) ![JADX](https://img.shields.io/badge/JADX-37474F?style=for-the-badge) ![Frida](https://img.shields.io/badge/Frida-FF6F00?style=for-the-badge) ![Burp Suite](https://img.shields.io/badge/Burp%20Suite-FF6633?style=for-the-badge&logo=burpsuite&logoColor=white) ![HTTP](https://img.shields.io/badge/HTTP-005C84?style=for-the-badge)

---

## 🧭 Experience & Security

### Education

- 고려대학교 세종캠퍼스 인공지능사이버보안학과 재학 `2022년 ~ 현재`

### 2026년 학부 보안 연구

- **Web API 기반 브라우저 핑거프린팅** 연구에 참여했습니다.
- WebCodecs, WebGPU, WebAssembly의 출력 결과와 실행 특성이 브라우저 식별 신호로 활용되는 최신 연구를 조사했습니다.
- 식별성뿐 아니라 안정성, 재현성, 개인정보 보호 관점에서 기술의 한계와 향후 과제를 정리했습니다.

### 2025.09 ~ 2026.03 카카오테크 부트캠프 (클라우드 네이티브)

- 백엔드, 데이터베이스, 컨테이너, 배포 자동화와 서비스 운영 전반을 학습했습니다.
- 팀 프로젝트에서 Git 기반 협업, 설계 문서화, 코드 리뷰, 부하 테스트와 장애 대응을 경험했습니다.

### 2024.02 ~ 2025.10 공군 사이버작전센터

- 사이버위협 상황 관제와 초기 대응 업무를 수행했습니다.
- 반복적인 보안 운영 업무를 JavaScript와 Python으로 자동화했습니다.

### Activities & Achievements
- **2026** 카카오테크 부트캠프 3기 클라우드 네이티브 과정 수료
- **2025** 공군 창업경진대회 본선 진출
- **2025** 공군 사이버전사경연대회 본선 진출
- **2023** SW 융합클러스터 2.0 기업 애로기술 해결 대회 대상
- **2023** 하나 소셜벤처 유니버시티 창업 교육 수료

### Certifications

- SQLD (한국데이터산업진흥원)
- 네트워크관리사 2급 (한국정보통신자격협회)

---

## 🧰 Tech Stack

### Languages

![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=111827)
![C++](https://img.shields.io/badge/C%2B%2B-00599C?style=for-the-badge&logo=cplusplus&logoColor=white)

### Backend & Web

![Spring Boot](https://img.shields.io/badge/Spring%20Boot-6DB33F?style=for-the-badge&logo=springboot&logoColor=white)
![Django](https://img.shields.io/badge/Django-092E20?style=for-the-badge&logo=django&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white)
![React](https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=react&logoColor=111827)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=for-the-badge&logo=nextdotjs&logoColor=white)

### Cloud & Infrastructure

![AWS](https://img.shields.io/badge/AWS-232F3E?style=for-the-badge&logo=amazonwebservices&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Nginx](https://img.shields.io/badge/Nginx-009639?style=for-the-badge&logo=nginx&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=111827)
![Cloudflare](https://img.shields.io/badge/Cloudflare-F38020?style=for-the-badge&logo=cloudflare&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-2088FF?style=for-the-badge&logo=githubactions&logoColor=white)

### Data & AI

![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=for-the-badge&logo=mongodb&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)

### Security Tools

![Splunk](https://img.shields.io/badge/Splunk-000000?style=for-the-badge&logo=splunk&logoColor=white)
![Burp Suite](https://img.shields.io/badge/Burp%20Suite-FF6633?style=for-the-badge&logo=burpsuite&logoColor=white)

### Engineering Focus

Backend Engineering, Cloud Architecture, CI/CD, Self-hosting  
Threat Monitoring, Reverse Engineering, LLM Integration, Model Fine-tuning

---

## 🗂️ More Projects & Learning

<details>
<summary><strong>C++ File Explorer</strong>: 자료구조와 알고리즘을 적용한 CLI 파일 탐색기</summary>

<br />

- C++ `filesystem`을 활용한 파일과 디렉터리 탐색 및 관리 기능을 구현했습니다.
- heap sort, 문자열 검색, BFS 기반 디렉터리 순회와 CMake 빌드 구성을 담당했습니다.
- 템플릿 기반 정렬 라이브러리와 탐색 함수의 오류를 수정하고 테스트 코드를 작성했습니다.
- Repository: [DataStructure-FileExplorer](https://github.com/baejun10/DataStructure-FileExplorer)

</details>

<details>
<summary><strong>Tag Counter for Datasets</strong>: 이미지 생성 모델 데이터셋 분석 도구</summary>

<br />

- Stable Diffusion 파인튜닝 데이터셋의 캡션 태그 분포를 분석하기 위해 만들었습니다.
- Python과 Pandas로 CSV 형식 라벨의 빈도를 집계해 데이터 불균형과 프롬프트 구성을 점검할 수 있게 했습니다.
- Repository: [Tag-counter-for-datasets](https://github.com/baejun10/Tag-counter-for-datasets)

</details>

<details>
<summary><strong>OCI 셀프호스팅</strong>: 개인 클라우드 서비스 구축과 운영</summary>

<br />

- Oracle Cloud ARM 인스턴스에 Open WebUI와 Vaultwarden을 Docker Compose로 운영했습니다.
- 컨테이너 내부 네트워크, Nginx 리버스 프록시, TLS 인증서, Cloudflare 보안 설정을 구성했습니다.
- 서비스 이전과 볼륨 백업, 네트워크 지연, 접근 제어 문제를 직접 해결했습니다.

</details>

<details>
<summary><strong>Security Practice</strong>: CTF와 LLM 보안 학습</summary>

<br />

- 웹 해킹, 시스템 해킹, 리버싱 문제를 풀며 취약점 분석의 기본기를 학습했습니다.
- AI와 LLM 보안 대회에서 프롬프트 인젝션과 적대적 입력, 모델 API의 공격 표면을 탐구했습니다.
- 개발 경험을 바탕으로 취약점의 재현뿐 아니라 구조적 원인과 대응 방법을 함께 분석하고 있습니다.

</details>

---

## ✍️ What I Write About

PITAS 블로그에 생성형 AI와 모델 파인튜닝, 데이터 처리, 인프라 구축, 개발 중 만난 문제의 원인과 해결 과정을 기록합니다.  
새로운 기술을 단순히 사용해 보는 데 그치지 않고, 직접 실험하고 실패한 과정까지 다음 문제 해결에 활용할 수 있도록 남기고 있습니다.

<p align="center">
  <sub>Build useful things. Understand how they work. Make them safer.</sub>
</p>

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&amp;color=0:0ea5a4,100:0f172a&amp;height=90&amp;section=footer" alt="Footer" width="100%" />
</p>
