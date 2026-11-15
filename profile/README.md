<img src="./assets/pinmap-avatar-2048.png" alt="핀맵 로고" width="160" height="160">

# 핀맵 · Pinmap

핀맵은 저장한 콘텐츠를 다시 찾고, 콘텐츠에 소개된 장소를 지도에서 살펴보는 서비스입니다. 웹 프로토타입, 모바일 앱, 온라인 장소 분석 서버를 각각의 저장소에서 개발하고 있습니다.

## 지금 체험할 수 있는 것

[공식 웹 프로토타입](https://pinmap-prototype.vercel.app/)에서는 예시 콘텐츠 체험과 로그인 화면을 열 수 있습니다.

| 환경 | 현재 동작 | 데이터 |
| --- | --- | --- |
| 프로토타입 체험 | 예시 콘텐츠로 저장함, 검색, 지도, 장소 카드, 코스 등을 살펴봅니다. | 저장·수정한 내용은 해당 브라우저에 보관됩니다. |
| 로그인 테스트 | Supabase 기반 이메일·소셜 로그인 흐름을 시험합니다. | 로그인 세션은 관리하지만 저장 콘텐츠를 계정 DB에 동기화하지는 않습니다. |

Instagram 장소 추출은 [별도 온라인 개발 테스트 화면](https://pinmap-backend.vercel.app/)에서 진행합니다. 게시물·릴스 링크를 분석해 장소 후보, 좌표, 확인이 필요한 이유와 서버 응답을 확인할 수 있습니다. 추출 결과는 공식 웹의 저장함에 자동으로 들어가지 않습니다. 프로토타입 체험의 AI 분류와 SNS 공유 흐름은 시연용이며, Instagram 저장 목록 자동 가져오기나 모바일 앱 연동은 구현되지 않았습니다.

## 코드와 진행 상태

| 영역 | 저장소 | 상태 |
| --- | --- | --- |
| 공식 웹 프로토타입 | [pinmap-web-prototype](https://github.com/pinmap-team/pinmap-web-prototype) · 공개 | HTML·CSS·JavaScript 화면. `main`이 공식 웹 배포에 연결되고 로그인·지도 설정은 백엔드 API를 호출합니다. |
| 온라인 API·장소 추출 | [pinmap-backend](https://github.com/pinmap-team/pinmap-backend) · 비공개 | Vercel API, Cloud Run 분석 서버, 장소 추출 개발 테스트 화면. 서버 설정과 키는 배포 환경에서 관리합니다. |
| iOS·Android 앱 | [pinmap](https://github.com/pinmap-team/pinmap) · 비공개 | Expo/React Native로 Instagram 공유 링크 수신·기기 내 저장·지도 화면을 실험 중입니다. 웹의 온라인 장소 추출과 계정 데이터는 아직 연결되지 않았습니다. |

장소 분석 테스트는 백엔드 저장소의 Vercel API를 거쳐 Cloud Run에서 수행합니다. Instagram 원본 접근, AI 분석, 장소 검색 결과는 게시물과 외부 서비스 상태에 따라 달라질 수 있습니다. 모바일 앱의 실기기 공유 수신과 출시 준비는 별도 검증이 필요합니다.

## 팀

사용자경험디자인II (26-2) 팀 프로젝트로 진행하고 있습니다.

- [신서윤 · @ssiissymhnn](https://github.com/ssiissymhnn)
- [이세은 · @wowseen-sketch](https://github.com/wowseen-sketch)
- [정지현 · @stophyun02](https://github.com/stophyun02)

[웹 프로토타입 체험](https://pinmap-prototype.vercel.app/) · [Figma 디자인](https://www.figma.com/design/LdXCdWJrA53sBN9aBgQEDy/?node-id=365-52)
