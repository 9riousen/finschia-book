---
cover: .gitbook/assets/wallet.png
coverY: -501.42756183745587
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

# ⚙ 지갑 설정하기

컨트랙트 개발의 배포와 실행에는 가스비가 필요하다. 핀시아에선 `FNSA`, 에보니에선 `TFNSA`가 필요하다.

이를 담아둘 개인지갑이 로컬 컴퓨터에 필요한데 핀시아용 개인지갑은 다음과 같다:

1. [도시 볼트(DOSI Vault)](https://chromewebstore.google.com/detail/dosi-vault/blpiicikpimmklhoiploliaenjmecabp):  크롬확장 형태로 배포되고 핀시아만 지원됨. LINE NEXT 제공
2. [케플러(Keplr)](https://chromewebstore.google.com/detail/keplr/dmkamcknogkgcdfhhbddcghachkejeap): 코스모스 블록체인에서 주로 사용하는 개인지갑. IBC[^1]전송 지원
3. [핀시아 CLI](https://docs.finschia.network/ko/node-management/interaction-with-finschia/using-cli): `fnsad` 실행파일은 블록체인 노드로 사용할 수도 있지만 원격 노드의 CLI[^2]로도 사용 가능. CLI에 지갑관리 기능이 내장됨

이 책에선 케플러와 `fnsad` 를 다룰 예정이다.

### Keplr 설치

[크롬 웹 스토어 Keplr 페이지](https://chromewebstore.google.com/detail/keplr/dmkamcknogkgcdfhhbddcghachkejeap)에서 설치

<figure><img src=".gitbook/assets/image (1).png" alt=""><figcaption><p> </p></figcaption></figure>

&#x20;Keplr는 여러 코스모스 체인을 지원하지만 Ebony 체인은 별도로 추가해 주어야 한다. 현재 Ebony 체인이 추가되어있는지는 "체인 선택하기" 화면에서 볼 수 있다 (`☰` → "체인 표시")



<figure><img src=".gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

### Ebony 체인 추가

[https://chains.keplr.app/](https://chains.keplr.app/) 는 케플러 커뮤니티에서 인정한 체인 목록을 제공한다. "ebony"를 검색하여 "Add to Keplr"를 클릭한다.

케플러는 기본적으로 지원하는 체인 목록([Native chain이라 칭함](https://medium.com/chainapsis/keplr-explained-native-vs-suggest-chain-or-permissionless-integration-8e425f921086)) 이 있고 후에 사용자가 체인을 추가할 수 있는 구조이다. 핀시아와 에보니는 케플러에서 기본으로 제공하지 않는다.

<figure><img src=".gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>

<figure><img src=".gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>

체인이 추가되었나 확인 (체크박스 선택)

<figure><img src=".gitbook/assets/image (5).png" alt=""><figcaption></figcaption></figure>

"자산"에 `TFNSA` 가 나타남

<figure><img src=".gitbook/assets/image (6).png" alt=""><figcaption></figcaption></figure>

[^1]: Inter Blockchain Communication

[^2]: Command Line Interface
