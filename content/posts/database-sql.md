---
title: "SQL - Ngôn ngữ truy vấn cơ sở dữ liệu"
date: 2024-12-12
draft: false
featured_image: "/images/anh11.jpg"
tags: ["SQL", "Database", "CRUD", "Backend"]
categories: ["Backend"]
---

## Giới thiệu

Trong bất kỳ hệ thống phần mềm nào, **Dữ liệu (Data)** luôn là tài sản quý giá nhất. SQL (Structured Query Language) là ngôn ngữ tiêu chuẩn được sử dụng để quản lý và thao tác dữ liệu trong các cơ sở dữ liệu quan hệ (Relational Database). Bằng cách sử dụng SQL, chúng ta có thể thực hiện các thao tác như truy vấn, thêm, sửa, xóa và quản lý cấu trúc của cơ sở dữ liệu.

SQL giúp người lập trình viên có thể tương tác với cơ sở dữ liệu, khai thác và xử lý các khối lượng dữ liệu lớn một cách hiệu quả. Hãy cùng tìm hiểu các lệnh cơ bản nhất trong SQL để thao tác với dữ liệu trong bài viết này.

## 1. Các lệnh thao tác dữ liệu cơ bản (CRUD)

CRUD là viết tắt của 4 thao tác cơ bản nhất trong SQL: **C**reate, **R**ead, **U**pdate, **D**elete.

### CREATE (Tạo mới)
Lệnh `CREATE` dùng để tạo mới các đối tượng trong cơ sở dữ liệu như bảng (table), chỉ mục (index), hoặc cơ sở dữ liệu.

#### **Tạo bảng mới**:

```sql
CREATE TABLE users (
    id INT PRIMARY KEY,
    name VARCHAR(100),
    email VARCHAR(100),
    age INT
);
