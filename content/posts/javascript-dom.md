---
title: "DOM Manipulation với JavaScript"
date: 2024-12-15
draft: false
tags: ["JavaScript", "DOM", "Frontend"]
categories: ["JavaScript"]
featured_image: "/images/anh7.jpg"
---

## Thao tác DOM với JavaScript

DOM (Document Object Model) là giao diện để tương tác với HTML từ JavaScript.

### Chọn phần tử

```javascript
// getElementById
const element = document.getElementById('myId');

// querySelector
const element = document.querySelector('.myClass');
const elements = document.querySelectorAll('.item');

// getElementByClassName
const elements = document.getElementsByClassName('myClass');
```

### Sửa đổi nội dung

```javascript
const element = document.getElementById('myId');

// Sửa text
element.textContent = 'Hello World';

// Sửa HTML
element.innerHTML = '<p>New content</p>';

// Sửa thuộc tính
element.setAttribute('data-value', '123');
element.style.color = 'red';
```

### Event Handling

```javascript
const button = document.getElementById('myButton');

button.addEventListener('click', function() {
    console.log('Button clicked!');
});

// Hoặc với arrow function
button.addEventListener('click', () => {
    console.log('Button clicked!');
});
```

DOM Manipulation là nền tảng của web development với vanilla JavaScript.
