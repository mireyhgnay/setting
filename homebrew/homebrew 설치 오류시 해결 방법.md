## homebrew 오류 해결

설치되던 중에 네트워크 연결 문제로 중간에 끊긴 경우, 다시 깔려고 해도 기존에 깔리던 것 때문에 오류 발생함

[https://worldseawater.tistory.com/87](https://worldseawater.tistory.com/87)

uninstall.sh 로 기존에 깔렸던걸 지우고 다시 설치! 

```bash
% /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/uninstall.sh)"
```