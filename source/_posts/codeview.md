---
title: Sample Views of Code Highlight
date: 2020-03-29
---

Bash:
<!-- --> 
```bash
$ for i in {0..9}; do
$    echo "hello world"
$ done
```
<!-- --> 

C++:
<!-- --> 
```cpp
int main() {
    for (int i = 0; i < 10; ++i) {
        std::cout << "hello world" << std::endl;
    }
    return 0;
}
```

Python3:
```py
for i in range(10):
    print("hello world")
```

Rust:
```rs
for x in 0..10 {
    println!("hello world");
}
```

diff (seems unsupported):
```diff
- before
+ after
```