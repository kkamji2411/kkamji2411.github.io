---
layout: post
title: Template Method Pattern ( Spring )
tags: [Template Method Pattern, Design Pattern, Java]
---

**Template Method Pattern**은 반복되는 코드를 줄이기 위한 관심사의 분리로
추상화를 통해 확장가능한 기능으로 변경하는 패턴으로, 공통으로 사용하는 부분은 상위 추상클래스에서 구현하고
나머지 필요한 부분은 각각 하위 클래스에서 구현하는 방식입니다.

``` java
public abstract class UserService {
    public void addUser(){
      //
    }
    public void delUser(){
      //
    }
    public abstract User getUser();
}

public class ASiteUserService extends UserService {
    @Override
    public User getUser() {
        // ASite User Return
        return null;
    }
}
public class BSiteUserService extends UserService {
    @Override
    public User getUser() {
        // BSite User Return
        return null;
    }
}

```
