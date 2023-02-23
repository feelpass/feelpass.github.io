---
title: "jekyll와 Github 연동하여 블로그 세팅을 해보자"
categories:
  - jekyll
tags:
  - jekyll
---

## 환경세팅

### RVM(Ruby Version Manager) 설치

최근 공부한 NVM과 동일한 개념 같다. NVM(Node Version Manager)는 Node 버전을 관리하는 용도라면 RVM은 Ruby 버전을 관리 하는 용도입니다..
맥OS에서 설치 방법입니다.

```
$ curl -sSL https://get.rvm.io | bash -s stable --ruby
```

설치가 완료되면 rvm PATH 환경 설정이 업데이트 되었으므로 터미널을 다시 시작하여 아래를 진행합니다.

```
$ rvm list // 설치된 ruby 버전 확인
$ rvm install 2.7.4
$ rvm list // 2.7.4 설치가 제대로 됐는디 확인
$ rvm use 2.7.4 --default // default 옵션을 붙이지 않으면 터미널 다시 시작시 예전 버저으로 다시 돌아옴
$ ruby -v // 2.7.4 제대로 나오는지 확인
```

### bundler 설치

Bundler는 Ruby 프로젝트를 위한 라이브러리 모음으로 라이브러리를 관리하는 용도로 Gemfile 을 관리 합니다.

```
$ gem install bundler
```

### Jekyll 설치 및 블로그 폴더 생성

```
$ gem install jekyll
$ jekyll -v // 버전확인
$ jekyll new {blog name} // {blog name} 폴더 명으로 생성됨
$ bundle exec jekyll serve // 
```

출력된 내용에 Server address를 보고 접속하면 구동 되는 것을 확인 할 수 있습니다.
```
Run in verbose mode to see all warnings.
                    done in 0.331 seconds.
 Auto-regeneration: enabled for '/Users/youngpillee/workspace/blog/feelpass.github.io'
    Server address: http://127.0.0.1:4000/
  Server running... press ctrl-c to stop.
```





### Github 연동하기
[https://github.com/new](https://github.com/new) 에서 Respository 하나 생성합니다.
Repository name은 {userid}.github.io 이름으로 만들어야 합니다.

![](/assets/0001/1.png)

Jekyll로 생성된 폴더와 Github Repository 연동 후 github에 올리면
feelpass.github.io 로 접속시 잘 동작 하는것을 확인 할 수 있습니다.
