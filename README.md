# 집단 지성 활용을 위한 지식 관리 시스템
## Knowledge Management System


### 기획안 5조 Team_KMS(미정)
* 🐰장준혁 🐂김영광 🐲박세종 🐴윤지용
<br/>

***

# ⭐프로젝트 개요

## 📌주제
사내 지식관리시스템은 조직 내 정보를 효과적으로 관리하고 활용하여 경쟁력을 강화하는 데 필수적인 도구입니다. 시스템을 운영하지 않을 경우 정보 공유 및 접근성 저하, 중복 노력 및 비효율성 증가, 역량 격차 및 숙련도 저하, 노하우 유출 및 정보 유실, 의사 결정 및 문제 해결 어려움 등 다양한 문제점이 발생할 수 있습니다. 따라서 조직의 성공적인 성장과 발전을 위해 사내 지식관리시스템 도입을 적극적으로 고려하고, 시스템을 효과적으로 운영하기 위한 전략을 수립해야 합니다.

## 📌목표 
1) 정보 공유 및 접근성 향상: 조직 내에서 정보의 신속한 공유와 쉬운 접근을 가능하게 하여, 팀원들이 필요한 정보를 빠르게 찾아 활용할 수 있도록 합니다. 이를 통해 업무 효율성과 생산성을 증가시키는 것이 목표입니다.
2) 중복 노력 및 비효율성 감소: 중복된 작업을 최소화하고, 기존에 축적된 지식을 재활용하여 업무 처리 시간을 단축시키는 것을 목표로 합니다. 이는 자원의 효율적인 배분을 가능하게 하여 전체적인 조직의 운영 효율성을 향상시킵니다.
3) 역량 격차 및 숙련도 향상: 조직 내 지식의 공유를 통해 모든 구성원이 동일한 정보와 노하우에 접근할 수 있게 하여, 역량 격차를 줄이고 직원들의 전문성 및 숙련도를 향상시키는 것을 목표로 합니다.
4) 노하우 보호 및 정보 유실 방지: 중요한 지식과 노하우를 체계적으로 관리하고 보호함으로써, 직원 이탈이나 기타 원인으로 인한 지식 유실을 방지하는 것이 목표입니다. 이는 조직의 중요한 자산을 보호하는 데 기여합니다.
5) 의사 결정 및 문제 해결 능력 강화: 신속하고 정확한 정보 제공을 통해 관리자와 팀원들이 보다 효과적으로 의사 결정을 내리고 문제를 해결할 수 있도록 지원하는 것을 목표로 합니다. 이는 조직의 민첩성과 대응력을 향상시킵니다.
6) 지속적인 학습 및 혁신 촉진: 사내 지식관리시스템을 통해 최신의 업계 동향, 기술 발전 및 베스트 프랙티스를 공유하여 조직 내 지속적인 학습 문화를 조성하고, 혁신을 촉진하는 것을 목표로 합니다.
<br/>

***

# ⭐기술 스택

## 📌공통
- 버전 관리 및 협업: GitHub, Git, GitHub Project
- 데이터베이스: MySQL, Redis
- 운영 체제: Linux (CentOS)
- 커뮤니케이션: Slack

## 📌프론트엔드
- 개발 환경: Visual Studio Code
- 프로그래밍 언어: HTML, CSS, JavaScript, Vue.js

## 📌백엔드
- 개발 환경: IntelliJ IDEA
- 프로그래밍 언어: Java 17
- 빌드 도구: Gradle
- 프레임워크: Spring, Spring Boot
- 보안: Spring Security, JSON Web Tokens (JWT)

## 📌데브옵스
- 지속적 통합(CI): github, github action
- 지속적 배포(CD): github action
- 컨테이너화: Docker
- 오케스트레이션: Kubernetes
<br/>

***

# ⭐요구사항 정의서

## 📌 목적
- 높은보안등급의 핵심기술문서를 차등권한을 부여하여 공동으로 관리하는 서비스

## 📌 직무의 구성
- 한화시스템의 임원은 방산부문과 ICT부문의 국장을 관리한다. 
- 한화시스템의 직무구성은 크게 방산부문과 ICT부문으로 2개로 나누며 각각을 관리하는 국장이 있다.
- 방산부문은 6개의 부서(하드웨어, 소프트웨어, 기계, 품질, IPS, 경영지원)으로 나뉘며 각각의 부장이 있다.
- 방산부문의 하드웨어부서는 2개의 팀영역(아날로그, 디지털)이 있으며 각각의 팀에는 팀장이 있다.
- 방산부문의 소프트웨어부서는 4개의 팀영역(시스템, 미들웨어, 어플리케이션, 특화분야)이 있으며 각각의 팀에는 팀장이 있다.
- 각각의 팀들은 유동적으로 여러팀을 가질 수 있으며(아날로그 1팀, 2팀 등... ) 각 팀의 최대인원은 12명 이하로 제한한다.
- ICT부문은 9개의 부서(ICT 서비스, IDC 인프라, 컨설팅, R&D, 아키텍트, 정보보호, 마케팅, 영업, 경영지원)으로 나뉘며 각각의 부장이 있다.
- 방산부문, ICT부문의 각각의 부장들은 12명 이하로 구성된 팀을 수시로 만들 수 있으며 부장은 부서내 팀장을 통해 팀원들을 관리한다.

## 📌 권한 관리
- 12명 이하로 구성된 팀이 구성되면 각 팀은 팀단위로 레포지토리(저장소)가 생성되며 팀장은 팀레포지토리 관리권한을 가진다.
- 팀내 구성원은 팀 레포지토리에 생성되는 파일들을 모두 열람할 수 있는 권한을 가지게 된다. 
- 팀과 팀장을 관리하는 부장은 팀 레포지토리에 내용들을 자유롭게 열람할 수 있는 권한이 생긴다. 
- 부장들을 관리하는 국장은 담당 부문의 모든 레포지토리를 열람할 수 있는 권한이 있다. 
- 한화시스템의 방산부문, ICT부문의 국장을 관리하는 임원은 한화시스탬내 모든 팀 레포지토리를 열람 할 수 있다. 
- 각 팀원, 팀장, 부장, 국장 들은 열람 권한이 없는 타 팀 레포지토리내 문서와 첨부파일들에 대한 권한을 요청할 수 있다. 
- 타 부서의 권한 요청은 권한의 유효기간이 있으며 1일 단위로 최대 30일까지 설정할 수 있고 만료가 되면 재요청을 해야 한다.

## 📌 유저 관리
- 유저는 KMS 서비스 Admain 관리자가 계정을 만들어 준다. 
- 각각의 유저는 하나이상의 권한 그룹에 소속된다. 
- 각각의 유저는 권한그룹을 통해 접근할 수 있는 팀 레포지토리가 결정된다. 
- 권한이 있는 팀 레포지토리내에서 문서내에 각 문단에 수정사항을 요청할 수 있다.
- 각 유저는 팀 레포지토리내에 있는 다른 팀원들의 수정사항들을 열람하고 수정사항들에 댓글을 달 수 있다.
- 각 유저는 수정사항에 동의할지 말지에 대한 투표를 할 수 있다. 
- 팀 레포지토의 팀장유저는 수정사항에 대한 투표결과와 수정 댓글들을 바탕으로 최정 수정을 승락할 수 있다.
- 각 유저는 타 레포지토리의 문서 목록은 자유롭게 열람할 수 있으나 문서 내용을 보고싶을 떄는 권한을 요청할 수 있다.
- 요청 받은 권한에 대한 승락은 각 팀 레포지토리를 관리하는 팀장이 권한의 유효기간을 최대 30일까지 설정하여 승락한다.

## 📌 지식 관리
- 지식을 관리를 위한 문서 작성은 마크 다운 형식을 기반으로한 자체 에디터를 통해 작성된다.
- 팀 레포지토리는 여러 개의 문서를 가질 수 있으며 각 문서별로 타 부서 유저에 대한 접근 권한을 설정할 수 있다. 
- 새로운 문서의 생성은 팀 레포지토리의 팀장을 통해서만 가능하고, 팀원은 생성된 문서의 수정 요청 권한을 가진다. 
- 수정한 모든 기록은 로그로 남으며 팀레포지토리의 팀장이 언제든지 이전 버전으로 되돌릴 수 있다. 
- 각각의 팀 레포지토리내 문서는 팀이 사라질 경우 다른 팀의 승인이 있을 경우 타 팀의 레포지토리로 이력과 함께 옮겨질 수 있다.
- 각각의 팀 레포지토리는 자체 에디터로 작성된 문서 이외에 첨부파일(이미지, 문서, PDF ...) 기능을 제공한다.
- 각각의 문서들은 팀장이 북마크 기능을 통해 상단에 위치 시킬 수 있다. 
- 각각의 문서들은 회사내 모든 사람들이 볼 수 있는 권한을 설정 할 수 있다. 
- 각각의 문서들은 팀원들에게 공개되기 전에 임시저장기능을 제공하며 최종 발행을 통해 권한이 있는 사람들에게 배포된다.

## 📌 통계 관리 
- 사장은 모든 팀 레포지토리내의 작성된 문서 갯수와 팀 래포지토리 목록을 한 페이지에서 조회 할 수 있다.
- 직원별로 회사내 지식문서 작성에 기여한 기여도를 대쉬보드를 통해 그래프와 숫자로 조회 할 수 있다. 
- 이 데이터를 기반으로 매월 보상을 통해 직원들의 노하우를 문서화 하는 일을 촉진할 수 있도록 관련 기능을 제공한다.
<br/>

***

# ⭐조직의 구성(예시)
## 📌방산 조직 구성도
<p align="center">
  <img src="https://github.com/beyond-sw-camp/be03-fin-5TEAM-KMS/assets/148752498/fea7b07f-4003-4051-a430-d85e8f23cdb1">
</p>

## 📌ICT 조직 구성도
<p align="center">
  <img src="https://github.com/beyond-sw-camp/be03-fin-5TEAM-KMS/assets/148752498/89c42cfb-0a12-49b0-a4db-459864afaccb">
</p>

## 📌전체 조직 구성도
<p align="center">
  <img src="https://github.com/beyond-sw-camp/be03-fin-5TEAM-KMS/assets/148752498/382a5abe-3dc9-4b02-a710-edbd3956ed32">
</p>
<br/>

***

# ⭐ERD 초안
<p align="center">
  <img src="https://github.com/beyond-sw-camp/be03-fin-5TEAM-KMS/assets/148752498/23d7692e-6a45-4340-9836-e28e3162c378">
</p>

