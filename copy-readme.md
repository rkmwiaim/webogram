### 프로그램 설치 방법
```
sudo npm install -g gulp
npm install
```

### 프로그램 실행 방법
```
gulp watch
```
이후 http://localhost:8000/app/index.html 로 접속하면 telegram web 프로그램이 뜬다

로그인도 가능하고 채팅방 목록도 전부 확인 가능하다

### 복사 방법
copy_relationships.json 에 아래와 같이 from, to 를 입력해준다

```
[
    {
        from: -123456789,
        to: -111111111 
    },
    {
        from: -222222222,
        to: -333333333 
    },
    ...
]
```

from, to 는 telegram에서 발급하는 채팅방 아이디 이다.

### telegram 채팅방 아이디 확인법
로그인 하고 채팅방이 모두 뜨고 나면, chrome developer tool을 열어준다.
(윈도우의 경우 F12)

developer tool 에서 위쪽의 탭 중 Console 을 선택한다.

아래 콘솔 창의 메세지들이 많이 떠 있을 것이다.
그 중 아래와 같은 메세지를 확인한다.
```
----------------------- chat list ----------------------- 
(17) [{…}, {…}, {…}, {…}, {…},
----------------------- chat list end -----------------------
```

맨 앞의 (17)은 자신의 채팅방 숫자이다.
17 앞에 있는 화살표를 눌러보면 채팅방 목록이 뜨고, 아래의 화살표를 계속 따라 누르면 채팅방들 각각의 정보가 나온다.
이 중 id 라고 되어 있는 항목이 채팅방 아이디 이다.
