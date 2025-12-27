---
title: "Java Collections Framework"
date: 2024-12-19
draft: false
tags: ["Java", "Collections", "API"]
categories: ["Java"]
featured_image: "/images/anh2.jpg"
---

## Java Collections Framework

Java Collections Framework cung cấp các lớp và interface để làm việc với các tập hợp dữ liệu.

### Các loại Collections chính

#### List
- ArrayList
- LinkedList
- Vector

#### Set
- HashSet
- TreeSet
- LinkedHashSet

#### Map
- HashMap
- TreeMap
- LinkedHashMap

### Ví dụ sử dụng

```java
import java.util.*;

public class CollectionExample {
    public static void main(String[] args) {
        // ArrayList
        List<String> names = new ArrayList<>();
        names.add("Java");
        names.add("Python");
        
        // HashSet
        Set<Integer> numbers = new HashSet<>();
        numbers.add(1);
        numbers.add(2);
        
        // HashMap
        Map<String, Integer> ages = new HashMap<>();
        ages.put("Alice", 25);
        ages.put("Bob", 30);
    }
}
```

Hiểu rõ Collections Framework là kỹ năng cần thiết cho mọi lập trình viên Java.
