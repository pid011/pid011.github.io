---
title: Unreal Engine LNK 2019 컴파일 문제 해결 방법
categories: ["Unreal Engine"]
tags: ["UnrealEngine", "Game"]
description:
toc: true
comments: true
---

Unreal Engine에서 C++ 코드를 컴파일 할 때 LNK 2019 오류를 종종 접한다.

이거는 거의 99% 모듈을 임포트하지 않아서 생긴 문제이니 해당 문제의 코드를 잘 살펴보고 코드가 참조하고 있는 변수의 타입이 속한 모듈이 `Build.cs` 에 `PublicDependencyModuleNames` 또는 `PrivateDependencyModuleNames`에 포함되어 있는지 확인하길 바란다.
