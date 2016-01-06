---
layout: post
title: Template Method Pattern ( Spring )
tags: [Template Method Pattern, Design Pattern, Java]
---

**Template Method Pattern**은 반복되는 코드를 줄이기 위한 관심사의 분리로
추상화를 통해 확장가능한 기능으로 변경하는 패턴으로, 공통으로 사용하는 부분은 상위 추상클래스에서 구현하고
나머지 필요한 부분은 각각 하위 클래스에서 구현하는 방식이다.
하지만 완벽한 해결방안이 아니며 상위 클래스에서 abstract 메소드가 추가됐을때에는 모든 하위 클래스가 수정되야
한다.
``` java
public abstract class UserDao {
    public abstract void add(User user);
    public void delUser(){
        //
    }
    public User getUser(){
        //
    }
}

public class ASiteUserDao extends UserDao {
    @Override
    public void add(User user) {
        // ASite User Return

    }
}
public class BSiteUserDao extends UserDao {
    @Override
    public void add(User user) {
        // BSite User Return

    }
}

```
