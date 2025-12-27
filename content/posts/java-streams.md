---
title: "Java Streams API - Lập trình hàm"
date: 2024-12-18
draft: false
tags: ["Java", "Streams", "Functional Programming"]
categories: ["Java"]
featured_image: "/images/anh5.jpg"
---

## Java Streams API

Streams API được giới thiệu trong Java 8 để hỗ trợ lập trình hàm và xử lý dữ liệu một cách khai báo.

### Các thao tác cơ bản

```java
List<Integer> numbers = Arrays.asList(1, 2, 3, 4, 5);

// Filter
numbers.stream()
    .filter(n -> n > 2)
    .forEach(System.out::println);

// Map
numbers.stream()
    .map(n -> n * 2)
    .collect(Collectors.toList());

// Reduce
int sum = numbers.stream()
    .reduce(0, Integer::sum);
```

### Lợi ích của Streams

- Code ngắn gọn hơn
- Dễ đọc và bảo trì
- Hỗ trợ parallel processing
- Tận dụng lazy evaluation

Streams API đã thay đổi cách chúng ta viết code Java hiện đại.
