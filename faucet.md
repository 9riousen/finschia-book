# faucet에서 코인 받기 💰

컨트랙트 배포에 사용할 가스비가 필요하다.

테스트넷은 수도꼭지(faucet)를 제공한다.

![](<.gitbook/assets/image (11).png>)

## 내 주소 알아내기

케플러에서 "주소복사"를 누르고 "Ebony" 항목의 복사버튼을 누른다

![](<.gitbook/assets/image (10).png>)

클립보드에 `tlink1`로 시작하는 주소가 복사된다. 이것이 자신의 개인지갑 주소이다.

`tlink15ujly6rhympqrsqnxgmt2twzesmr8yyqclfsyk` 은 김택배의 주소이니 테스트용 전송 대상으로 사용 가능함&#x20;

## faucet에서 코인 받기

```bash
curl --header "Content-Type: application/json" \
     --request POST \
     --data '{"denom":"tcony","address":"tlink15ujly6rhympqrsqnxgmt2twzesmr8yyqclfsyk"}' \
     https://faucet-ebonynw.line-apps.com/credit
```

즉시 케플러에서 잔액 확인됨 (핀시아 빠르다)

## 참고자료

[https://docs.finschia.network/ko/node-management/node-setup-testnet#faucet](https://docs.finschia.network/ko/node-management/node-setup-testnet#faucet)
