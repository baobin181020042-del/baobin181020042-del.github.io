---
title: "ES6 - JavaScript Modern"
date: 2024-12-17
draft: false
tags: ["JavaScript", "ES6", "Frontend"]
categories: ["JavaScript"]
featured_image: "/images/anh8.jpg"
---

## ES6 (ECMAScript 2015) - Tiêu chuẩn JavaScript Hiện đại

ES6 mang đến nhiều tính năng mới giúp lập trình JavaScript dễ dàng hơn.

### Các tính năng chính

#### 1. Arrow Functions
```javascript
// Traditional
const add = function(a, b) {
    return a + b;
}

// Arrow
const add = (a, b) => a + b;
```

#### 2. Template Literals
```javascript
const name = "Bảo";
const message = `Hello ${name}!`;
```

#### 3. Destructuring
```javascript
const person = { name: "Bảo", age: 20 };
const { name, age } = person;

const [a, b] = [1, 2];
```

#### 4. Classes
```javascript
class Car {
    constructor(brand) {
        this.brand = brand;
    }
    
    drive() {
        console.log(`${this.brand} is driving`);
    }
}
```

ES6 đã trở thành tiêu chuẩn cho phần lớn dự án JavaScript ngày nay.
