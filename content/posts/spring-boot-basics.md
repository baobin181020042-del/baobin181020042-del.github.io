---
title: "Spring Boot - Khởi đầu nhanh"
date: 2024-12-14
draft: false
tags: ["Java", "Spring Boot", "Backend"]
categories: ["Java"]
featured_image: "/images/anh10.jpg"
---

## Spring Boot - Lập trình Web Backend dễ dàng

Spring Boot đơn giản hóa việc tạo ứng dụng Spring, giảm boilerplate code.

### Cấu trúc cơ bản

```java
import org.springframework.boot.SpringApplication;
import org.springframework.boot.autoconfigure.SpringBootApplication;
import org.springframework.web.bind.annotation.GetMapping;
import org.springframework.web.bind.annotation.RestController;

@SpringBootApplication
public class Application {
    public static void main(String[] args) {
        SpringApplication.run(Application.class, args);
    }
}

@RestController
public class HelloController {
    @GetMapping("/hello")
    public String hello() {
        return "Hello World!";
    }
}
```

### Các tính năng chính

- Auto-configuration
- Embedded server (Tomcat, Jetty, Undertow)
- Starter dependencies
- Actuator cho monitoring
- Dễ deployment

### Tạo project mới

```bash
mvn archetype:generate -DgroupId=com.example -DartifactId=my-app
# Hoặc dùng Spring Boot CLI
spring boot new --name my-app
```

Spring Boot là lựa chọn hàng đầu cho phát triển web backend với Java.
