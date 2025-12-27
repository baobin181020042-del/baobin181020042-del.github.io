---
title: "React - Thư viện Frontend hiện đại"
date: 2024-12-13
draft: false
tags: ["JavaScript", "React", "Frontend"]
categories: ["JavaScript"]
featured_image: "/images/anh9.jpg"
---

## React - Xây dựng UI với Components

React là thư viện JavaScript giúp xây dựng giao diện người dùng tương tác dễ dàng.

### Component cơ bản

```javascript
// Functional Component
function Welcome(props) {
    return <h1>Hello {props.name}</h1>;
}

// Hoặc với arrow function
const Welcome = (props) => {
    return <h1>Hello {props.name}</h1>;
};

// JSX
const element = <Welcome name="Bảo" />;
```

### Hooks

```javascript
import React, { useState, useEffect } from 'react';

function Counter() {
    const [count, setCount] = useState(0);
    
    useEffect(() => {
        console.log('Component mounted or count changed');
    }, [count]);
    
    return (
        <div>
            <p>Count: {count}</p>
            <button onClick={() => setCount(count + 1)}>
                Increment
            </button>
        </div>
    );
}
```

### Virtual DOM

React sử dụng Virtual DOM để tối ưu hóa rendering, chỉ update những phần thay đổi.

React đã trở thành framework JavaScript phổ biến nhất trong vài năm qua.
