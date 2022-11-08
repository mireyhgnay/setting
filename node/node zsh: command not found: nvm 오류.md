## ⚠️ nvm 설치 오류

‼️ **brew install nvm 설치 잘 하고,**

**nvm 명령어 실행하면  `zsh: command not found: nvm` 오류 발생**

**(확인 결과 OS X 10.15 이상부터 zsh shell을 기본으로 사용하기 때문에 발생하는거라고 한다...)**

### <해결 방안>

1. vi 편집기 열기
    1. **i로 편집 → esc 로 편집모드 끄기**
    
    ```bash
    $ vi ~/.zshrc
    ```
    
2. 아래 코드를 ~/.zshrc 하단에 작성 후 저장 및 종료( **:wq** ) 
    
    ```bash
    export NVM_DIR=~/.nvm 
    source $(brew --prefix nvm)/nvm.sh
    ```
    
3. 터미널을 재로그인하거나, source 명령어로 스크립트 실행
    
    ```bash
    source ~/.zshrc
    ```
    
4. 터미널 완전히 종료 후, 다시 실행
    
    ```bash
    nvm -v // v0.39.0
    ```
    
5. `nvm` 명령어에 대한 설명이 잘 나오시면 성공입니다.