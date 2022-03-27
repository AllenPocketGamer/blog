+++
title = "|game X chain| Dfinity游戏开发实践(3/3)"
date = 2022-03-17

[extra]
bgcolor = "bg-[#91c483]"
+++

资料整理中...
<!-- more -->

# 一级: 警告面板

---

{% alert(type="info") %}
月光如流水一般，静静地泻在这一片叶子和花上。薄薄的青雾浮起在荷塘里。叶子和花仿佛在牛乳中洗过一样；又像笼着轻纱的梦。虽然是满月，天上却有一层淡淡的云，所以不能朗照；但我以为这恰是到了好处——酣眠固不可少，小睡也别有风味的。月光是隔了树照过来的，高处丛生的灌木，落下参差的斑驳的黑影，峭楞楞如鬼一般；弯弯的杨柳的稀疏的倩影，却又像是画在荷叶上。塘中的月色并不均匀；但光与影有着和谐的旋律，如梵婀玲⑼上奏着的名曲。
{% end %}

{% alert(type="danger") %}
月光如流水一般，静静地泻在这一片叶子和花上。薄薄的青雾浮起在荷塘里。叶子和花仿佛在牛乳中洗过一样；又像笼着轻纱的梦。虽然是满月，天上却有一层淡淡的云，所以不能朗照；但我以为这恰是到了好处——酣眠固不可少，小睡也别有风味的。月光是隔了树照过来的，高处丛生的灌木，落下参差的斑驳的黑影，峭楞楞如鬼一般；弯弯的杨柳的稀疏的倩影，却又像是画在荷叶上。塘中的月色并不均匀；但光与影有着和谐的旋律，如梵婀玲⑼上奏着的名曲。
{% end %}

## 二级: 代码块

---

```rust,linenos,hl_lines=2 7 13
fn hello() {
  let args: Vec<String> = std::env::args().collect();
  if args.get(1) != Some(&"nonlocal".to_string()) {
      // Run tests
      cmd!("cargo test --workspace")
          .run()
          .expect("Please fix failing tests in output above.");

      // Run doc tests: these are ignored by `cargo test`
      cmd!("cargo test --doc --workspace")
          .run()
          .expect("Please fix failing doc-tests in output above.");
}
```

```rust,hl_lines=2
fn hello() {
  let p = 13;
  println!("Hello World");
  println!("Hello World");
}
```

### 三级: 无序列表/有序列表/~~任务链表~~

---

- George Washington

  George Washington月光如流水一般，静静地泻在这一片叶子和花上。薄薄的青雾浮起在荷塘里。叶子和花仿佛在牛乳中洗过一样；又像笼着轻纱的梦。月光如流水一般，静静地泻在这一片叶子和花上。薄薄的青雾浮起在荷塘里。叶子和花仿佛在牛乳中洗过一样；又像笼着轻纱的梦。
- John Adams

  月光如流水一般，静静地泻在这一片叶子和花上。薄薄的青雾浮起在荷塘里。叶子和花仿佛在牛乳中洗过一样；又像笼着轻纱的梦。月光如流水一般，静静地泻在这一片叶子和花上。薄薄的青雾浮起在荷塘里。叶子和花仿佛在牛乳中洗过一样；又像笼着轻纱的梦。
- Thomas Jefferson

1. James Madison

    James Madison月光如流水一般，静静地泻在这一片叶子和花上。薄薄的青雾浮起在荷塘里。叶子和花仿佛在牛乳中洗过一样；又像笼着轻纱的梦。月光如流水一般，静静地泻在这一片叶子和花上。薄薄的青雾浮起在荷塘里。叶子和花仿佛在牛乳中洗过一样；又像笼着轻纱的梦。
2. James Monroe
3. John Quincy Adams

#### 四级: 链接/图片

---

月光如流水一般，[静静地泻在这一片叶子和花上](https://github.com/AllenPocketGamer)。薄薄的青雾浮起在荷塘里。叶子和花仿佛在牛乳中洗过一样；又像笼着轻纱的梦。虽然是满月，天上却有一层淡淡的云，所以不能朗照；但我以为这恰是到了好处——酣眠固不可少，小睡也别有风味的。月光是隔了树照过来的，高处丛生的灌木，落下参差的斑驳的黑影，峭楞楞如鬼一般；弯弯的杨柳的稀疏的倩影，却又像是画在荷叶上。塘中的月色并不均匀；但光与影有着和谐的旋律，如梵婀玲⑼上奏着的名曲。



这是我的[GITHUB](https://github.com/AllenPocketGamer), 请查看.

![This is an image too](../image/sample.png)

![This is an image](../image/place-hold-img.jpg)

##### 五级: 引用文本/引用标题

---

>如果您还不了解 Rust，那么请先阅读 Rust 程序设计语言。 它将会帮您理清思路：Rust 是什么样的语言、如何安装它、以及它的语法概念（syntax and concepts）。 在看完本书后，您将成为一个登堂入室（intermediate）的 Rust 开发人员，并将很好地理解 Rust 背后的基本理念。

`月光如流水一般，静静地泻在这一片叶子和花上`。
薄薄的青雾浮起在荷塘里。叶子和花仿佛在牛乳中洗过一样；又像笼着轻纱的梦。
虽然是满月，天上却有一层淡淡的云，所以不能`朗照`；但我以为这恰是到了好处——酣眠固不可少，小睡也别有风味的。
月光是隔了树照过来的，高处丛生的灌木，`落下参差的斑驳`的黑影，峭楞楞如鬼一般；
弯弯的杨柳的稀疏的倩影，却又像是画在荷叶上。塘中的月`色并`不均匀；但光与影有着和谐的旋律，如梵婀玲⑼上奏着的名曲。
在`Dfinity`中, 使用的是`Rust`语言进行开发!

月光如流水一般，静静地泻在这一片叶子和花上。薄薄的青雾浮起在荷塘里。叶子和花仿佛在牛乳中洗过一样；又像笼着轻纱的梦。虽然是满月，天上却有一层淡淡的云，所以不能朗照；但我以为这恰是到了好处——酣眠固不可少，小睡也别有风味的。月光是隔了树照过来的，高处丛生的灌木，落下参差的斑驳的黑影，峭楞楞如鬼一般；弯弯的杨柳的稀疏的倩影，却又像是画在荷叶上。塘中的月色并不均匀；但光与影有着和谐的旋律，如梵婀玲⑼上奏着的名曲。

> There is no doubt that he is the choosen one!

###### 六级: 粗体/斜体/删除线

---

__月光如流水一般，静静地泻在这一片叶子和花上。薄薄的青雾浮起在荷塘里。__
_叶子和花仿佛在牛乳中洗过一样；又像笼着轻纱的梦。_
~~虽然是满月，天上却有一层淡淡的云，所以不能朗照；但我以为这恰是到了好处——酣眠固不可少，小睡也别有风味的。~~
__月光是隔了树照过来的__，_高处丛生的灌木_，~~落下参差的斑驳的黑影，峭楞楞如鬼一般~~；
***弯弯的杨柳的稀疏的倩影，却又像是画在荷叶上。***
**塘中的月色并不均匀；_但光与影有着和谐的旋律_，如梵婀玲⑼上奏着的名曲**。