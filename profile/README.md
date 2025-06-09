<div align="center">
  <h1>👤 Vata</h1>
  <p>
    <strong>나의 개성을 반영한 AI 프로필 사진 만들기</strong><br><br>
    <strong>🛸 배포: <a href="https://vata-fe.vercel.app/" target="_blank">Vata 바로가기</a></strong>
  </p>
</div>

## 📜 목차

| 순번 | 항목 |
| :-: | :-: |
| 1 | 팀원 소개 |
| 2 | 서비스 개요 |
| 3 | 서비스 소개 |
| 4 | 기능 플로우차트 |
| 5 | 시스템 아키텍처 |
| 6 | UI / UX |
| 7 | ERD |
| 8 | 트러블슈팅 & 성능 향상 |

</br>

## 1️⃣ 팀원 소개

| _이름_ | 김준형 | 문형주 | 오주성 |
|:-----:|:----:|:-----:|:----:|
| ___역할___ | BE | BE | FE / AI |
| ___Github___ | <a href="https://github.com/JHZLO"><img src="https://avatars.githubusercontent.com/u/105791673?v=4" width="64" height="64"></a> | <a href="https://github.com/moon4528"><img src="https://avatars.githubusercontent.com/u/166115965?v=4" width="64" height="64"></a> | <a href="https://github.com/jsgo53"><img src="http://avatars.githubusercontent.com/u/198019299?v=4" width="64" height="64"></a> |

</br>

## 2️⃣ 서비스 개요

Vata는 사용자의 개성과 취향을 기반으로 AI 프로필 이미지를 생성해주는 웹 애플리케이션입니다.  
Stable Diffusion 기반의 이미지 생성 모델을 활용하여 사용자가 입력한 정보를 시각적으로 표현합니다.

</br>

## 3️⃣ 서비스 소개

### 🎯 배경 및 문제점
- SNS, 메신저 등에서 나를 표현할 수 있는 프로필 이미지의 중요성이 증가하고 있음
- 하지만 대부분의 유저는 개성 있는 프로필 이미지를 손쉽게 제작하기 어려움
- 기존 아바타 생성 서비스는 획일적이거나 선택지가 제한적인 경우가 많음

### 👥 END USER
- 개성을 드러내고 싶은 SNS 사용자
- MBTI, 취미 등으로 나를 표현하고 싶은 사람
- AI 이미지에 관심 있는 사람 누구나

### 🧩 주요 기능
- 성별, MBTI, 취미, 이미지 스타일을 바탕으로 한 Stable Diffusion 프롬프트 생성
- 사용자가 원하는 스타일로 AI 이미지 생성
- 보관함 기능을 통한 생성 이미지 확인 및 저장
- Access Token 발급 가이드 및 관리 기능

### 🚀 기대 효과
- 손쉬운 사용자 경험으로 누구나 나만의 이미지 생성 가능
- AI 이미지 생성 과정을 통해 사용자 흥미 유도
- 오픈소스 API 및 최신 기술 활용 사례 제공

</br>

## 4️⃣ 기능 플로우차트

![image](https://github.com/user-attachments/assets/cd710cb0-fb79-4b79-9489-771db33cf1f7)

</br>

## 5️⃣ 시스템 아키텍처

![image](https://github.com/user-attachments/assets/a72f3617-b73d-44b9-881f-ade2c53599e8)

</br>

## 6️⃣ UI / UX

- 직관적인 페이지 흐름 (회원가입 → 토큰 입력 → 입력 폼 → 결과 → 보관함)
- 토큰 가이드 포함으로 초심자도 쉽게 접근 가능
- Loading, Error, Alert UI 등 사용자 친화적인 피드백 구성
- 반응형 UI 및 테마 조화로 모바일/웹 환경 모두 대응

</br>

## 7️⃣ ERD

![image](https://github.com/user-attachments/assets/93d33eed-f4fe-49a5-8f1a-58ac6b251a29)

</br>

## 8️⃣ 트러블슈팅 & 성능 향상

### 🧩 트러블슈팅
- Access Token 인증 시 GET → POST로 변경 (보안 이슈 대응)
- 토큰 상태 저장 관련 location state, sessionStorage 혼용 → 상태관리 통일
- Axios Interceptor를 통한 에러 핸들링 일괄 처리

### 💡 성능 향상
- Vercel 배포 환경 캐싱 및 Lazy 로딩 적용
- API 응답 시 loading 처리 적용 → UX 향상
- 프론트/백엔드 기능 분리 및 경량화
