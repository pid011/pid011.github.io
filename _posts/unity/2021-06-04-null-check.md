```
title: "Unity에서 null 체크하는 여러가지 방법들"
date: 2021-06-04T02:53+9
categories: unity
toc: true
published: false
```

Unity에는 fake null 개념이 있다.

기본적으로 유니티 엔진의 모든 오브젝트들은 `UnityEngine.Object` 클래스를 상속받고 있는데, 이 클래스는 `==` 와 `!=`를 오버로딩하고 아래의 `CompareBaseObjects` 메소드로 비교를 수행하게 된다.![image-20210604030133053](C:\Users\pid01\workspace\repos\github.com\pid011\pid011.github.io\_posts\unity\2021-06-04\image-20210604030133053.png)



