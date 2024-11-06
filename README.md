# Mac Terminal Session

## Terminal Emulator이란?

먼저 터미널 에뮬레이터 개념에 대해서 알아봅시다.

터미널 에뮬레이터란 사용자가 컴퓨터 시스템과 상호작용할 수 있는 GUI 소프트웨어입니다. 뒤에서 언급하겠지만 `shell`을 동작시키는 소프트웨어입니다.

쉽게 말해서 우리가 Mac에서 사용하는 `Terminal`, 가장 많은 추천 터미널 에뮬레이터인 `iTerm2 `가 있습니다.

## 추천 터미널 에뮬레이터

> 각 터미널 밑에 적혀있는 설명들은 지극히 제이시 개인적인 생각입니다 ^^

### [iTerm2](https://iterm2.com/)

- 가장 익숙한 터미널 에뮬레이터
- Mac을 처음에 개발환경으로 세팅할 때, 블로그에서 가장 많이 보이는 에뮬레이터

### [hyper](https://hyper.is/)
- `JavaScript` 기반으로 작성된 터미널 에뮬레이터
- 그래서 에뮬레이터에 대한 설정도 웹브라우저로 확인할 수 있다

### [warp](https://www.warp.dev/)
- 요즘 사용하고 있는 에뮬레이터
- AI가 붙어서 자연어(Natural Language)를 창에 입력해도 적절한 CLI를 에뮬레이터가 생성해준다

> 솔직히 디자인 차이인 것 같습니다. 여러분이 가장 마음에 드는 에뮬레이터를 사용하시면 되겠습니다. 또한 에뮬레이터 별로 설정할 수 있는 기능이 전부 달라서 정말 마음에 드는 것을 골라서 사용해도 좋을 것 같아요.

## Shell의 등장

여기서 하나 짚고 넘어가야 하는 부분에는 `Terminal`과 `iTerm2`를 실행해도 하나의 `shell`을 사용하는 것을 확인할 수 있습니다.

`bash`나 `zsh`에 대해서 쉽게 접할 수 있는데, 해당 개념에 대해서 알아봅시다.

### What is Shell?

쉘(Shell)은 사용자와 운영 체제의 커널 사이에서 명령을 해석하고 실행하는 명령어 해석기입니다. 쉘을 통해 사용자는 시스템에 명령을 입력하고, 이를 커널이 이해할 수 있는 형태로 전달하여, 그 결과를 다시 사용자에게 보여주는 방식으로 컴퓨터와 상호작용합니다. 쉘은 터미널 에뮬레이터에서 실행되며, 사용자가 명령어를 입력할 수 있는 텍스트 기반의 인터페이스를 제공합니다.

위의 설명은 정석적으로 설명하는 쉘에 대한 개념이고, 제가 느낀 쉘이란 에뮬레이터 위에서 컴퓨터와 소통하는 창이라고 생각합니다.

### [Bash](https://www.gnu.org/software/bash/)

`bash`는 맥을 처음 샀을 때 기본적으로 활성화 되어있는 쉘 입니다. 리눅스를 조금 공부해보신 분은 아시겠지만, 리눅스 시스템에서도 기본적으로 사용하는 쉘 입니다. 리눅스와 macOS는 유닉스라는 공통적인 분모를 가지고 있어서 Mac에서도 `bash` 쉘을 기본으로 사용하고 있습니다.

### [Zsh](https://www.zsh.org/)

`Zsh`은 `iTerm2`와 같이 Mac을 초기에 세팅할 때, 가장 많이 언급되는 쉘 입니다. 사용자에게 제공하는 기능이 정말 많기 때문에 가장 널리 사용되는 쉘입니다.

### [Fish](https://fishshell.com/)

`Fish` 쉘은 사용자 친화적인 쉘이라는 성격을 강조합니다. 하지만 저한테는 `zsh`과 크게 다르지는 않은 것 같아요. `zsh`이 워낙 사용하는 사람도 많고 오픈소스이다보니 별의별 기능이 들어가 있습니다.

### shell 관련 커맨드

```zsh
which $SHELL
```

위의 명령어는 내가 사용하고 있는 쉘을 확인할 수 있는 쉘

```zsh
cat /etc/shells
```

위의 명령어는 현재 나의 Mac에서 사용가능한 쉘의 리스트를 보여준다

> 주로 zsh을 사용하는 것을 추천합니다. 저는 그냥 호기심에 터미널 에뮬레이터마다 별개의 쉘을 사용하고 있는데, 이러면 쉘마다 설정하는 스크립트를 작성해야 해서 많이 번거롭습니다.

## 터미널 세션의 핵심

> 아래의 자료들을 통해서 꿀팁들을 알아가요!

### [HomeBrew](https://brew.sh/) 패키지 매니저

> 개발하다보면 다양한 라이브러리를 사용하기 위해서 패키지 매니저를 사용합니다. iOS에서 같은 경우는 `CocoaPods`, `SPM(Swift Package Manager)`, `Carthage`가 있고 안드로이드에서는 빌드도구인 gradle에 `implementation` 스크립트를 사용해서 라이브러리를 사용하고, 웹에서는 `npm`, 파이썬에서는 `pip`와 같은 도구를 사용합니다.

Mac에서도 Apple 시스템에서 사용하기 위한 다양한 패키지들을 설치할 수 있는 도구가 있습니다.

HomeBrew를 사용해서 개발 도구뿐만 아니라 생각보다 많은 어플리케이션도 설치할 수 있습니다.

---

```zsh
brew install "설치하고자 하는 프로그램"
```

위의 명령어를 사용해서 내가 사용하고자 하는 프로그램을 설치할 수 있습니다.

---

```zsh
brew install --cask "설치하고자 하는 어플리케이션 프로그램"
```

위의 명령어를 사용해서 내가 사용하고자 하는 어플리케이션 프로그램을 설치할 수 있습니다.

---

```zsh
brew list
```

위의 명령어를 사용해서 내가 설치한 프로그램의 항목을 확인할 수 있습니다.

---

```zsh
brew update
```

홈브루 패키지 매니저의 버전을 업데이트 합니다.

---

```zsh
brew upgrade
```

패키니 매니저를 통해서 설치한 프로그램들의 항목들을 업데이트 합니다.

## Code Command

> CLI를 사용하다보면 해당 디렉터리 기준으로 편집기를 열 수 있는 강력한 기능이 있습니다. 

Visual Studio Code를 사용한다면 코드뿐만 아니라 마크다운 문서 편집 등 문서 편집기로서 사용하고 싶을 때가 많습니다. 이럴 때 마다 VSC를 열어서 폴더 열기 하는 작업은 너무 번거롭죠.

`Command + Shift + P`를 눌러서 `Shell Command`를 입력하면 `code` 명령을 `PATH`에 추가할 수 있습니다.

```zsh
code .
```



## Customize ZSH Shell

> 터미널 에뮬레이터는 어떤 것을 사용해도 무방합니다. 다만 쉘에서 제공하는 기능은 개발자 여러분들을 다소 편하게 해줄 수 있기 떄문에 해당 문서에서는 ZSH의 다양한 기능을 소개하겠습니다.

### [Oh-my-zsh](https://ohmyz.sh/)

Oh-my-zsh(omz)는 zsh 위에서 다양한 기능을 사용하기 위한 프레임워크입니다.

> 설치가 되어있지 않다면 위의 사이트에서 설치해주세요

### [Zsh Theme](https://github.com/ohmyzsh/ohmyzsh/wiki/themes)

zsh에서는 수많은 테마를 사용할 수 있는데, 타이틀의 하이퍼링크를 따라가면 수많은 테마를 확인할 수 있습니다. 이 중에서 마음에 드는 테마를 선택해주세요.

```zsh
source .zshrc
```

가장 상위 디렉터리로 가서 위의 커맨스를 실행해주어야 변경사항이 적용됩니다. 아니면 쉘을 종료하고 다시 열면 됩니다!

이 때 폰트가 깨져있는 것을 볼 수 있는데, 사용하고자 하는 터미널 에뮬레이터의 폰트를 변경해야 합니다.

저는 `MesloLGS NF` 폰트를 사용하는데, 사용할 수 있는 수많은 폰트가 있습니다. 확인 후 터미널 에뮬레이터에 적용해보면 되겠습니다!

대표적으로 [Nerd font](https://www.nerdfonts.com/)에서 다운로드 할 수 있습니다.

### Zsh Plugin

> 제이시가 정말 잘 사용하고 있는 Zsh 플러그인에 대해서 소개하겠습니다.

### [Zsh Syntax Highlighting](https://github.com/zsh-users/zsh-syntax-highlighting/blob/master/INSTALL.md)

```.zshrc
source ~/.oh-my-zsh/custom/plugins/zsh-syntax-highlighting/zsh-syntax-highlighting.zsh
```

위의 커맨드를 `.zshrc` 파일에 붙여넣으면 되겠습니다.

![sample1](/zsh-syntax-highlighting1.png)

위의 이미지를 보면 알 수 있듯이, `git` 명령어를 사용할 때 초록색으로 syntax를 하이라이트 해주는 것을 볼 수 있습니다.

![sample2](/zsh-syntax-highlighting2.png)

또한 정상적인 명령어가 아니라면, 위의 이미지와 같이 빨간색으로 표기되는 것을 확인할 수 있습니다.

### autojump

정말 강력한 기능입니다. `j` 커맨드를 사용해서 내가 이동하고자 하는 디렉터리를 넘나들 수 있습니다.

```.zshrc
plugins=(autojump)
```

`zshrc` 파일에 위와 같이 플러그인을 활성화 해주시면 됩니다.

### zsh-autosuggestion

커맨드를 입력하면 자동으로 추천 CLI를 표기합니다.

```.zshrc
plugins=(zsh-autosuggestions)
```

![zsh-autosugestion](/zsh-autosuggestion1.png)

