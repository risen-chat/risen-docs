# 채팅방에 초대하기

### 문제 상황

- 서버에는 채팅방의 Key가 노출되어서는 안됨.
- TLS handshake같은 Key 교환을 사용하면, 클라이언트 둘중 하나라도 오프라인이면 초대가 불가능함.

### 해결 방법

- Key를 암호화하여 서버에 올려둠.
- 클라이언트는 암호화와 동시에 Key를 복호화할 수 있는 임시 Key를 생성함.
- 임시 Key를 초대링크에 포함하여 상대방에게 전달함.
- 상대방은 초대링크를 통해 서버에서 암호화된 Key를 받아오고, 임시 Key로 복호화함.
- 이렇게 Key 노출 없이 안전하게 초대가 가능함.

* 서버에 올려둔 암호화된 Key는 Redis같은 인메모리 데이터베이스에 저장하여, 일정 시간이 지나거나 한번 사용되면 만료되도록 설정함.

<div>
<iframe
  frameBorder="0"
  style={{ width: "100%", height: "383px" }}
  src="https://viewer.diagrams.net/?tags=%7B%7D&lightbox=1&highlight=0000ff&edit=_blank&layers=1&nav=1&title=invite_room.drawio&dark=auto#Uhttps%3A%2F%2Fraw.githubusercontent.com%2Frisen-chat%2Frisen-docs%2Fmain%2Fdiagrams%2Finvite_room.drawio"
/>
</div>
