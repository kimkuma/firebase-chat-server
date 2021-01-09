# Firebase-chat-server
> Firebase를 이용한 채팅서버

RESTful API 방식으로 firebase에 채팅서버를 구성

## Getting Started

### 구성
- firebase-tools
- npm
- express
- cors

### Run in development
#### Run backend server
``` bash
# Using terminal  
firebase serve --only functions
...
+ functions[v1]: http function initialized (http://localhost:5000/{프로젝트ID}/us-central1/v1 
출력시 정상 기동
```

### Project folder structure
``` bash
fire-chat-server
├── firebase.json
│── functions
│   ├── index.js
│   ├── node_modules
│   ├── package-lock.json
│   └── package.json
└── public
```

## API Specifications

----
* 채널만들기 : `POST /channels`
* 채널명목록확인: `GET /channels`
* 특정 채널에 새 메시지 추가 : `POST /channels/:채널명/messages`
* 채널 메시지 목록 확인 : `GET /channels/:채널명/messages`
* 초기상태로 돌아가기 : `POST /reset`
