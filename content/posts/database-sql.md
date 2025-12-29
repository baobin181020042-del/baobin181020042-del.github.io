---
title: "Lập trình hướng đối tượng (OOP) trong Java - Từ lý thuyết đến thực chiến"
date: 2024-12-20
draft: false
tags: ["Java", "OOP", "Lập trình", "Backend"]
categories: ["Java"]
featured_image: "/images/anh4.jpg"
description: "Giải thích chi tiết 4 tính chất của OOP kèm ví dụ minh họa sống động."
---

## 🚀 Giới thiệu
<div style="background-color: #091823ff; padding: 15px; border-left: 5px solid #2196F3; margin-bottom: 20px; border-radius: 4px;">
    <strong>💡 Tổng quan:</strong> Lập trình hướng đối tượng (OOP) không chỉ là viết code, mà là <em>tư duy mô hình hóa</em> thế giới thực vào trong máy tính. Đây là kỹ năng bắt buộc phải có nếu bạn muốn trở thành Java Developer.
</div>

Trong Java, mọi thứ đều xoay quanh **Class (Lớp)** và **Object (Đối tượng)**. Hãy cùng đi sâu vào 4 trụ cột chính đã làm nên sức mạnh của ngôn ngữ này.

---

## 1. Bốn trụ cột của OOP (The 4 Pillars)

Để dễ nhớ, chúng ta hãy hình dung OOP giống như việc lắp ráp một chiếc xe hơi:

### 🛡️ 1. Encapsulation (Tính Đóng gói)
Đóng gói giống như việc **động cơ xe được che chắn dưới nắp capo**. Người lái xe không cần biết động cơ hoạt động thế nào, chỉ cần biết đạp ga là chạy.
* **Mục đích:** Che giấu dữ liệu quan trọng, tránh bị thay đổi lung tung từ bên ngoài.
* **Cách dùng:** Sử dụng từ khóa `private` và cung cấp `Getter/Setter`.

### 🧬 2. Inheritance (Tính Kế thừa)
Giống như việc **Xe Thể Thao** kế thừa các đặc điểm của **Xe Ô tô** (có 4 bánh, có vô lăng) nhưng nâng cấp thêm động cơ mạnh hơn.
* **Mục đích:** Tái sử dụng code, tránh viết lặp lại.
* **Từ khóa:** `extends`.

### 🎭 3. Polymorphism (Tính Đa hình)
Cùng là hành động "bấm còi", nhưng **xe máy kêu "bíp bíp"**, còn **xe tải kêu "hú còi"**. Cùng một hành động nhưng cách thực hiện khác nhau.
* **Mục đích:** Linh hoạt trong việc xử lý đối tượng.

### 👻 4. Abstraction (Tính Trừu tượng)
Bạn chỉ quan tâm đến cái **Vô lăng** (Giao diện) để lái xe, không cần quan tâm trục lái bên trong kết nối ra sao.
* **Mục đích:** Tập trung vào cái người dùng cần, ẩn đi sự phức tạp.

---

## 💻 Ví dụ thực chiến (Code Example)

Dưới đây là ví dụ minh họa sự kết hợp giữa **Kế thừa** và **Đa hình**:

```java
// Lớp cha (Parent Class)
public abstract class Animal {
    protected String name;
    
    public Animal(String name) {
        this.name = name;
    }
    
    // Phương thức trừu tượng (chưa biết kêu như nào)
    public abstract void makeSound();
}

// Lớp con Chó (Dog)
public class Dog extends Animal {
    public Dog(String name) {
        super(name);
    }
    
    @Override
    public void makeSound() {
        System.out.println(name + " sủa: Gâu Gâu! 🐕");
    }
}

// Lớp con Mèo (Cat)
public class Cat extends Animal {
    public Cat(String name) {
        super(name);
    }
    
    @Override
    public void makeSound() {
        System.out.println(name + " kêu: Meow Meow! 🐈");
    }
}

