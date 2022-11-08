## Ngrok 사용하기

```
📌 일반적으로는 로컬 개발환경을 구축하고 개발을 진행하지만,     
상황에 따라서 개발 환경에서 외부 접근을 열어주는 일은 굉장히 번거로운 일이 될 수도 있어      
이런 경우 간단하게 사용할 수 있는 Ngrok이라는 프로그램이 있다!
```

### Ngrok란?
Ngrok은 외부(Public)에서 로컬에 접속할 수 있게 도와주는 터널링 프로그램입니다.

### Ngrok 설치

1. Mac OS의 경우 brew를 이용하여 설치합니다.
    
    `$ brew install --cask ngrok`
    

1. [https://dashboard.ngrok.com/get-started/setup](https://dashboard.ngrok.com/get-started/setup) > 로그인 > authtoken 복사
    
    authtoken 값 입력하여 세션 계속 유지시키기
    
    `$ ngrok config add-authtoken 2B0x9BC3U9dW3BcEVNlEcjjX4RF_3xZjgaKnNiSqTt3CZ7oHf`
    
    `$ ngrok http 3000`
    

![스크린샷 2022-06-24 오후 4.50.43.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/5733f212-4b59-45f3-8568-22d92529bfab/스크린샷_2022-06-24_오후_4.50.43.png)

Forwarding 주소 복사하여 공유! 하면 외부 다른 사용자도 로컬에 접속하여 볼 수 있게됩니다🥳

-----

참조 [https://velog.io/@bluearin/Ngrok-사용하여-개발하기](https://velog.io/@bluearin/Ngrok-%EC%82%AC%EC%9A%A9%ED%95%98%EC%97%AC-%EA%B0%9C%EB%B0%9C%ED%95%98%EA%B8%B0)