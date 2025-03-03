---
title: 언리얼에서 UI 텍스처 해상도에 맞게 DPI 설정하기
categories: ["Unreal Engine"]
tags: ["UnrealEngine", "Game"]
description:
toc: true
comments: true
---

UI 소스 텍스처의 기준 해상도가 4K일 때, 언리얼엔진에서 DPI 스케일 1.0일 때의 해상도 값이 1080일 경우 위젯에 이미지를 넣으면 매우 크게 나오게 된다.

이를 해결하기 위해서는 project Settigns > Engine > User Interface에서 Design Screen Size를 3840x216으로 설정해주면 자동으로 에디터에서의 스케일이 4K 기준으로 표시되어 정상적으로 4K 텍스처를 적용할 수 있다.

![settings](../assets/blobs/240904-settings.png)
