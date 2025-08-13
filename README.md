# Risen 소개

Risen은 채팅 전체를 암호화하는 보안 채팅서비스입니다.

client side encryption으로,
Risen은 클라이언트 측에서 모든 메시지를 암호화하고, 서버에는 암호화된 메시지만 저장됩니다.

따라서 Risen은 서버가 메시지를 읽을 수 없으며, 오직 사용자만이 자신의 메시지를 읽을 수 있습니다.

## 팀인원

Server: [이세민](https://github.com/wwwcomcomcomcom),[김태은](https://github.com/snowykte0426), [조수민](https://github.com/suuuuuuminnnnnn)
App: [이주언](https://github.com/aiden30015), [문승덕](https://github.com/bluemoon983)

# Docs Repository Rule

## 커밋 컨벤션

커밋 메세지에 대한 제약은 따로 없으며,
한글위주로 누구나 알아보기 쉽고 간결하게 작성합니다.

## 브랜치 룰

api 문서같은 경우 main에서 브랜치 분기 없이 커밋으로만 관리합니다.

간혹 docusaurus에 기능을 추가하기 위한 js,ts 코드 변경이 일부 생긴다면
"feat/\*\*\*" 형태로 브랜치를 생성합니다.

## 네이밍 규칙

- folder,tsx: camelCase
- markdown: kebab-case
