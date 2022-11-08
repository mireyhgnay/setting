### 설치 방법

[https://brew.sh/index_ko](https://brew.sh/index_ko) 

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

중간에 tapping하라는게 나오는데, `done.` 이 나오면 

tapping 하라는 문구 > **homebrew/core** 를 입력하기

```bash
==> Tapping homebrew/core
```

설치완료👇

```bash
==> Next steps:
- Run these two commands in your terminal to add Homebrew to your PATH:
    **echo 'eval "$(/opt/homebrew/bin/brew shellenv)"' >> /Users/yanghr/.zprofile
    eval "$(/opt/homebrew/bin/brew shellenv)"**
- Run brew help to get started
- Further documentation:
    https://docs.brew.sh
```

안내를 따라 다음 2줄을 실행

```bash
echo 'eval "$(/opt/homebrew/bin/brew shellenv)"' >> /Users/yanghr/.zprofile
eval "$(/opt/homebrew/bin/brew shellenv)"
```

최신 homebrew가 잘 설치 되었는지 위치와 버전을 확인

```bash
# homebrew 설치된 위치 확인
$ which brew
/opt/homebrew/bin/brew

# homebrew 버전 확인
$ brew --version
Homebrew 3.3.16
Homebrew/homebrew-core (git revision bd1001ba9a9; last commit 2022-02-23)
```