---
cover: .gitbook/assets/image (12).png
coverY: -123.48355263157895
layout:
  cover:
    visible: true
    size: hero
  title:
    visible: true
  description:
    visible: true
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
---

# 테스트 코인 받기

컨트랙트를 배포하거나 사용하려면 가스비(gas fee)를 지불해야한다.

핀시아 메인넷의 가스비는 `FNSA`로 지불하는데 빗썸등의 거래소에서 구매할 수 있다.

개발에 사용하는 테스트넷은 다양한 형태로 테스트코인을 배포하는데 간단한 요청으로 무료 코인을 받는 자판기 같은 서비스를 faucet(수도꼭지)라고 부른다.

에보니 테스트넷에서도 수도꼭지를 제공하는데 내 주소를 넘겨주면 테스트코인 1 `TFNSA`를 전송해 준다. (하루에 1번만 됨)

## 내 주소 알아내기

케플러에서 "주소복사"를 누르고 "Ebony" 항목의 복사버튼을 누른다

![](<.gitbook/assets/image (10).png>)

클립보드에 `tlink1`로 시작하는 주소가 복사된다. 이것이 자신의 개인지갑 주소이다.

`tlink15ujly6rhympqrsqnxgmt2twzesmr8yyqclfsyk` 은 김택배의 주소이니 무엇이든 많이 보내도 상관없다.&#x20;

## 수도꼭지에 코인 요청하기

```bash
curl --header "Content-Type: application/json" \
     --request POST \
     --data '{"denom":"tcony","address":"tlink15ujly6rhympqrsqnxgmt2twzesmr8yyqclfsyk"}' \
     https://faucet-ebonynw.line-apps.com/credit
```

즉시 케플러에서 잔액 확인됨 (매우 빠르다)

## 참고자료

[https://docs.finschia.network/ko/node-management/node-setup-testnet#faucet](https://docs.finschia.network/ko/node-management/node-setup-testnet#faucet)
