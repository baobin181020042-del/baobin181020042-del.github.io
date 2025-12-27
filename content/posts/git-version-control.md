---
title: "Git - Quản lý phiên bản code"
date: 2024-12-11
draft: false
tags: ["Git", "DevOps", "Tools"]
categories: ["Tools"]
featured_image: "/images/anh1.jpg"
---

## Git - Công cụ quản lý version không thể thiếu

Git là hệ thống kiểm soát phiên bản phân tán được sử dụng rộng rãi trong phát triển phần mềm.

### Các lệnh cơ bản

```bash
# Khởi tạo repository
git init

# Clone repository
git clone https://github.com/user/repo.git

# Kiểm tra trạng thái
git status

# Thêm files
git add .

# Commit
git commit -m "Add new feature"

# Push lên remote
git push origin main

# Pull từ remote
git pull origin main
```

### Branching

```bash
# Tạo branch mới
git branch feature/new-feature

# Switch branch
git checkout feature/new-feature

# Hoặc tạo và switch cùng lúc
git checkout -b feature/new-feature

# Merge branch
git merge feature/new-feature
```

### Giải quyết conflict

Khi merge 2 branch có thay đổi trên cùng một file, Git sẽ yêu cầu giải quyết conflict.

Git là công cụ thiết yếu trong mọi dự án phần mềm hiện đại.
