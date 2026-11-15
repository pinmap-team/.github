# 핀맵 · Pinmap

핀맵은 저장한 콘텐츠를 다시 찾고, 콘텐츠에 소개된 장소를 지도에서 살펴보는 서비스입니다. 현재는 웹 프로토타입과 모바일 앱 실험을 **서로 다른 저장소**에서 진행하고 있습니다.

## 지금 체험할 수 있는 것

[공식 웹 프로토타입](https://pinmap-prototype.vercel.app/)에는 세 가지 시작 환경이 있습니다.

| 환경 | 현재 동작 | 데이터 |
| --- | --- | --- |
| 프로토타입 체험 | 예시 콘텐츠로 저장함, 검색, 지도, 장소 카드, 코스 등을 살펴봅니다. | 저장·수정한 내용은 해당 브라우저에 보관됩니다. |
| 개발 테스트 | 로그인 없이 Instagram 장소 게시물·릴스 링크를 온라인 분석 서버로 보내 장소 후보와 좌표를 지도·상세 화면에서 확인합니다. | 분석 결과는 현재 화면에만 남고 새로고침하면 사라집니다. |
| 로그인 테스트 | Supabase 기반 이메일·소셜 로그인 흐름을 시험합니다. | 로그인 세션은 관리하지만 저장 콘텐츠를 계정 DB에 동기화하지는 않습니다. |

개발 테스트는 게시물 접근 여부와 장소 정보의 명확성에 따라 분석 결과가 달라집니다. 추출한 장소라도 좌표를 확인하지 못하면 지도에 표시되지 않을 수 있습니다. 프로토타입 체험의 AI 분류와 SNS 공유 흐름은 시연용이며, 실제 Instagram 저장 목록 자동 가져오기나 모바일 앱 연동을 뜻하지 않습니다.

## 코드와 진행 상태

| 영역 | 저장소 | 상태 |
| --- | --- | --- |
| 공식 웹 프로토타입 | [pinmap-web-prototype](https://github.com/pinmap-team/pinmap-web-prototype) · 공개 | HTML·CSS·JavaScript 화면과 Vercel 중계 함수. `main`이 공식 웹 배포에 연결됩니다. |
| iOS·Android 앱 | [pinmap](https://github.com/pinmap-team/pinmap) · 비공개 | Expo/React Native로 Instagram 공유 링크 수신·기기 내 저장·지도 화면을 실험 중입니다. 웹의 온라인 장소 추출과 계정 데이터는 아직 연결되지 않았습니다. |

웹의 장소 분석은 Vercel 중계 함수를 거쳐 별도 Cloud Run 서버에서 수행합니다. 인스타그램 원본 수집, AI 분석, 장소 검색 결과는 게시물과 외부 서비스 상태에 따라 제한될 수 있습니다. 모바일 앱의 실기기 공유 수신과 출시 준비는 별도 검증이 필요합니다.

## 팀

사용자경험디자인II (26-2) 팀 프로젝트로 진행하고 있습니다.

- [신서윤 · @ssiissymhnn](https://github.com/ssiissymhnn)
- [이세은 · @wowseen-sketch](https://github.com/wowseen-sketch)
- [정지현 · @stophyun02](https://github.com/stophyun02)

[웹 프로토타입 체험](https://pinmap-prototype.vercel.app/) · [Figma 디자인](https://www.figma.com/design/LdXCdWJrA53sBN9aBgQEDy/?node-id=365-52)
