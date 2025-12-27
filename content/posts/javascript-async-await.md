---
title: "JavaScript Async/Await - Xử lý bất đồng bộ"
date: 2024-12-16
draft: false
tags: ["JavaScript", "Async", "Promise"]
categories: ["JavaScript"]
featured_image: "/images/anh6.jpg"
---

## Async/Await trong JavaScript

Async/Await là cách hiện đại để xử lý bất đồng bộ trong JavaScript, làm cho code dễ đọc hơn.

### So sánh Callback, Promise, và Async/Await

#### Callback Hell
```javascript
fetchUser(id, function(user) {
    fetchPosts(user.id, function(posts) {
        fetchComments(posts[0].id, function(comments) {
            console.log(comments);
        });
    });
});
```

#### Promise Chain
```javascript
fetchUser(id)
    .then(user => fetchPosts(user.id))
    .then(posts => fetchComments(posts[0].id))
    .then(comments => console.log(comments))
    .catch(error => console.error(error));
```

#### Async/Await
```javascript
async function getComments(id) {
    try {
        const user = await fetchUser(id);
        const posts = await fetchPosts(user.id);
        const comments = await fetchComments(posts[0].id);
        console.log(comments);
    } catch (error) {
        console.error(error);
    }
}
```

Async/Await làm code trông giống như synchronous nhưng thực tế là bất đồng bộ.
