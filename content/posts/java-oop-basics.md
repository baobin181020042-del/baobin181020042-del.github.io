---
title: "Lập trình hướng đối tượng (OOP) trong Java"
date: 2024-12-20
draft: false
tags: ["Java", "OOP", "Lập trình"]
categories: ["Java"]
featured_image: "/images/anh4.jpg"
---

## Lập trình hướng đối tượng trong Java

Lập trình hướng đối tượng (OOP) là một paradigm lập trình quan trọng trong Java. Bài viết này sẽ giới thiệu các khái niệm cơ bản của OOP.

### 4 Trụ cột của OOP

1. **Encapsulation (Đóng gói)** - Che giấu dữ liệu bên trong class
2. **Inheritance (Kế thừa)** - Lớp con kế thừa từ lớp cha
3. **Polymorphism (Đa hình)** - Cùng một phương thức, nhiều cách thực hiện
4. **Abstraction (Trừu tượng)** - Ẩn chi tiết phức tạp, chỉ hiển thị giao diện

### Ví dụ cơ bản

```java
public class Animal {
    protected String name;
    
    public Animal(String name) {
        this.name = name;
    }
    
    public void sound() {
        System.out.println("Animal makes a sound");
    }
}

public class Dog extends Animal {
    public Dog(String name) {
        super(name);
    }
    
    @Override
    public void sound() {
        System.out.println(name + " barks: Woof Woof");
    }
}
```

OOP giúp code dễ bảo trì, mở rộng và tái sử dụng.
