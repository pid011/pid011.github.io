---
title: Jetbrains IDE (IntelliJ, Rider)에서 좌우 패널 길이 확장하는 방법
categories:
  - IDE
tags:
  - IDE
description: 
toc: true
comments: true
mermaid: true
---
제가 기존에 사용하던 ide 및 에디터들은 사진과 같이 좌측 탭이 전체길이를 차지하는 형태입니다. 이 형태는 탐색기에서 파일 목록을 확인하기에 용이해서 제가 선호하는 형태죠.

![vscode panel](../assets/blobs/250731-vs.png)

![](../assets/blobs/250731-vscode.png)


그러나 Jetbrains IDE는 기본이 하단 패널이 전체 길이를 차지하는 형태입니다.

![Rider Before](../assets/blobs/250731-rider-before.png)

이 형태는 좁은 가로 길이에서는 잘 어울리지만 와이드 스크린에서는 쓸데없이 하단 패널이 공간을 많이 차지합니다.

이를 설정에서 변경하여 수정할 수 있습니다.

적용하기 위해서는 `Settings` → `Appearance & Behaviour` → `Apearance` → `Tool Windows`에서 `Widescreen tool window layout` 을 체크해줍니다.

![IDE Settings image](../assets/blobs/250731-ide-settings.png)

그러면 아래 사진과 같이 좌측 패널이 전체 길이를 차지하는 형태가 됩니다.

![Rider After](../assets/blobs/250731-rider-after.png)