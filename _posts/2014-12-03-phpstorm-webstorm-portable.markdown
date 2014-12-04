---
layout: post
title:  "PhpStorm 및 WebStorm을 portable(포터블)하게 사용하기!"
date:   2014-12-03 12:57:32
author: Seoklae Kim
categories: none
---

### PhpStorm및 WebStorm 설치파일 다운로드

JetBrain홈페이지에서 Webstorm이나 PhpStorm을 다운받으세요. 저는 `PhpStorm-8.0.1.exe`를 다운받았습니다.

<a href="https://www.jetbrains.com/phpstorm/" class="btn btn-primary btn-block btn-lg" target="_blank">PhpStorm 홈페이지 링크</a>


### 압축해제

다운받은 exe파일의 확장자를 zip으로 바꾸세요. 파일 탐색기에서 확장자 확인이 안된다면, 보기옵션에서 확장자명 보기가 활성화 되어있어야 합니다. `PhpStorm-8.0.1.zip`이 되었군요. 이걸 압축해제하였습니다.


### 설정 파일 주석 해제

압축 해제한 디렉토리 안에 있는 `idea.properties`파일을 편집합니다. 전 기본 메모장으로 편집하였습니다. `idea.properties`파일의 가장상위 2개의 설정을 주석해제 합니다.

{% highlight bash %}

#---------------------------------------------------------------------
# Uncomment this option if you want to customize path to IDE config folder. Make sure you're using forward slashes.
#---------------------------------------------------------------------
idea.config.path=${user.home}/.WebIde/config

#---------------------------------------------------------------------
# Uncomment this option if you want to customize path to IDE system folder. Make sure you're using forward slashes.
#---------------------------------------------------------------------
idea.system.path=${user.home}/.WebIde/system

{% endhighlight %}

위 처럼 2가지 주석을 해제하였습니다. 혹시 이외에도 `${user.home}`가 있다면 역시 주석해제 합니다.

### 설정 파일 주석 해제

이제 아래와 같이 모든 `${user.home}`을 `${idea.home}`으로 변경합니다.

{% highlight bash %}

#---------------------------------------------------------------------
# Uncomment this option if you want to customize path to IDE config folder. Make sure you're using forward slashes.
#---------------------------------------------------------------------
idea.config.path=${idea.home}/.WebIde/config

#---------------------------------------------------------------------
# Uncomment this option if you want to customize path to IDE system folder. Make sure you're using forward slashes.
#---------------------------------------------------------------------

idea.system.path=${idea.home}/.WebIde/system

{% endhighlight %}

### 사용

이제 bin디렉토리의 PhpStorm.exe를 실행하면, portable(포터블)하게 사용가능합니다.

