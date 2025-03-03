---
title: GitHub 레포지토리를 찾을 수 없는 오류 해결방법 (HTTPS, SSH 관련 오류)
categories:
  - Git
tags:
  - Git
  - GitHub
description: 
toc: true
comments: true
mermaid: true
---

가끔씩 비공개 레포지토리를 포크해서 Git GUI 클라이언트를 통해 pull이나 fetch를 받으려 하면 다음과 같은 에러가 뜹니다.

```shell
Fetching origin  
From github.com:surround-games/UnrealEngine  
 = [up to date]                main       -> origin/main  
Fetching upstream  
remote: Repository not found.  
fatal: repository 'https://github.com/EpicGames/UnrealEngine.git/' not found  
error: could not fetch upstream
```

이 경우 원격 레포지토리에 대한 권한을 Git 클라이언트가 가지고 있지 않아서인데, 권한만 잘 부여해주면 해결됩니다.

Git에서 원격 레포지토리와 연결하는 방법은 HTTPS, SSH가 있는데, HTTPS의 경우 Git Client에서는 서드파티 OAuth 앱 권한을 부여해줘야 정상적으로 작동하지만 접근 권한이 없는 Organization에서 포크한 레포는 권한을 부여할 수 없어 제대로 작동하지 않습니다.

SSH를 사용하면 서드파티 앱 권한을 따로 받을 필요가 없습니다. 유저가 레포지토리가 속한 Organization에 소속되어 있기만 하면 됩니다.

GitHub에서 ssh 키를 새로 등록한 후, GitHub에 등록한 키의 공개키와 비공개 키를 `C:\Users\{유저이름}\.ssh` 디렉토리에 저장한 뒤, git 레포의 origin 주소를 ssh 주소로 변경하면 됩니다. Fork와 같은 Git GUI에서도 SSH를 설정하면 정상적으로 pull과 fetch가 가능해집니다.



![Fork SSH Key config](../assets/blobs/250226-fork-sshkey.png)

### git GUI 에서 ssh 키 설정 후 여전히 연결되지 않는다면

git 클라이언트에서 설정한 ssh키가 GitHub에 정상적으로 등록되어 있는지 확인해봅니다.

### git CLI에서 ssh로 원격지 주소 변경 후 연결되지 않는다면

이 경우는 `.ssh` 디렉토리에서 공개키와 비공개키가 `id_rsa.pub`, `id_rsa`로 설정되어 있지 않는지 확인해봅니다.