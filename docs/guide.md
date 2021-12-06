# 指南

## 提示块

??? example "举个栗子"
    ```
    !!! note
    note
    ```

    !!! note
        note

### 更改标题

??? example "举个栗子"
    ```
    !!! note "小提示"
    note
    ```

    !!! note "小提示"
        note

### 删除标题

??? example "举个栗子"
    ```
    !!! note ""
    note
    ```

    !!! note ""
        note

### 可折叠块

??? example "举个栗子"
    ```
    ??? note
    note
    ```

    ??? note
        note

在 `???` 后面添加一个 `+`，提示块默认为打开状态。

??? example "举个栗子"
    ```
    ???+ note
    note
    ```

    ???+ note
        note

### 支持的类型

??? example "举个栗子"

    !!! note "note"
        注意
    
    !!! summary "summary"
        概括
    
    !!! info "info todo"
        信息
    
    !!! tip "tip important"
        提示，重要
    
    !!! success "success check done"
        成功 检查 完成
    
    !!! question "question help"
        问题 帮助
    
    !!! warning "warning"
        警告
    
    !!! failure "failure fail missing"
        失败 丢失
    
    !!! danger "danger error"
        危险 错误
    
    !!! bug "bug"
        bug
    
    !!! example "example"
        举例
    
    !!! quote "quote"
        引用

## 代码块

### 添加标题

??? example "举个栗子"
    ```` markdown
    ``` py title="bubble_sort.py"
    def bubble_sort(items):
    for i in range(len(items)):
    ```
    ````

    ``` py title="bubble_sort.py"
    def bubble_sort(items):
        for i in range(len(items)):
    ```

### 添加注释

??? example "举个栗子"
    ````markdown
    ``` yaml
    theme:
    features:
    - content.code.annotate # (1)
    ```

    1. :man_raising_hand: I'm a code annotation!
    ````

    ``` yaml
    theme:
      features:
        - content.code.annotate # (1)
    ```

    1. I'm a code annotation!

### 添加行号

??? example "举个栗子"
    ````
    ``` py linenums="23"
    def bubble_sort(items):
    for i in range(len(items)):
    for j in range(len(items) - 1 - i):
    if items[j] > items[j + 1]:
    items[j], items[j + 1] = items[j + 1], items[j]
    ```
    ````

    ``` py linenums="23"
    def bubble_sort(items):
    for i in range(len(items)):
    for j in range(len(items) - 1 - i):
    if items[j] > items[j + 1]:
    items[j], items[j + 1] = items[j + 1], items[j]
    ```

### 高亮行号

??? example "举个栗子"
    ````markdown
    ``` py hl_lines="2 3"
    def bubble_sort(items):
    for i in range(len(items)):
    for j in range(len(items) - 1 - i):
    if items[j] > items[j + 1]:
    items[j], items[j + 1] = items[j + 1], items[j]
    ```
    ````

    ``` py hl_lines="2 3"
    def bubble_sort(items):
        for i in range(len(items)):
            for j in range(len(items) - 1 - i):
                if items[j] > items[j + 1]:
                    items[j], items[j + 1] = items[j + 1], items[j]
    ```

### 内联代码块

??? example "举个栗子"
    ```markdown
    The `#!python range()` function is used to generate a sequence of numbers.
    ```

    The `#!python range()` function is used to generate a sequence of numbers.

## 内容选项卡

### 代码分组

??? example "举个栗子"
    ````markdown
    === "C"
    
        ``` c
        #include <stdio.h>
    
        int main(void) {
          printf("Hello world!\n");
          return 0;
        }
        ```
    
    === "C++"
    
        ``` c++
        #include <iostream>
    
        int main(void) {
          std::cout << "Hello world!" << std::endl;
          return 0;
        }
        ```
    ````
    
    === "C"
    
        ``` c
        #include <stdio.h>
    
        int main(void) {
          printf("Hello world!\n");
          return 0;
        }
        ```
    
    === "C++"
    
        ``` c++
        #include <iostream>
    
        int main(void) {
          std::cout << "Hello world!" << std::endl;
          return 0;
        }
        ```

### 其他分组

??? example "举个栗子"
    ```markdown
    === "Unordered list"
    
        * Sed sagittis eleifend rutrum
        * Donec vitae suscipit est
        * Nulla tempor lobortis orci
    
    === "Ordered list"
    
        1. Sed sagittis eleifend rutrum
        2. Donec vitae suscipit est
        3. Nulla tempor lobortis orci
    ```
    
    === "Unordered list"
    
        * Sed sagittis eleifend rutrum
        * Donec vitae suscipit est
        * Nulla tempor lobortis orci
    
    === "Ordered list"
    
        1. Sed sagittis eleifend rutrum
        2. Donec vitae suscipit est
        3. Nulla tempor lobortis orci

## 格式化

### 突出标签

??? example "举个栗子"
    ``` markdown
    Text can be {--deleted--} and replacement text {++added++}. This can also be
    combined into {~~one~>a single~~} operation. {==Highlighting==} is also
    possible {>>and comments can be added inline<<}.
    ```
    
    Text can be {--deleted--} and replacement text {++added++}. This can also be
    combined into {~~one~>a single~~} operation. {==Highlighting==} is also
    possible {>>and comments can be added inline<<}.

### 突出文本

??? example "举个栗子"
    ```markdown
    - ==This was marked==
    - ^^This was inserted^^
    - ~~This was deleted~~
    ```

    - ==This was marked==
    - ^^This was inserted^^
    - ~~This was deleted~~

### 上标和下标

??? example "举个栗子"
    ```markdown
    - H~2~0
    - A^T^A
    ```

    - H~2~0
    - A^T^A

### 键盘按键

??? example "举个栗子"
    ```markdown
    ++ctrl+alt+del++
    ```

    ++ctrl+alt+del++

## 参考

1. [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/)