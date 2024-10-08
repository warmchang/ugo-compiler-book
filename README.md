# 《µGo语言实现——从头开发一个迷你语言编译器》

- *凹语言(专为 WebAssembly 设计): https://github.com/wa-lang/wa*
- *WaBook(Go语言实现的MD电子书构建工具): https://github.com/wa-lang/wabook*

----

本书尝试以实现 µGo 编译器为线索，以边学习边完善的自举方式实现一个玩具语言。

![](cover.svg)

- 在线阅读(Go版本): https://wa-lang.github.io/ugo-compiler-book/
- 示例代码(Go版本): [https://github.com/wa-lang/ugo](https://github.com/wa-lang/ugo) (和章节对应的分支)
- µGo 输出C语言: https://github.com/3dgen/ugo-c-book
- 社区分享: [Go编译器定制简介](https://wa-lang.org/ugo-compiler-book/go-compiler-intro.html)

---

## Why: 挖坑的起因

- 因为坑就在那里
- 挖坑的工具差不多齐全了
- 为了启动 [凹语言](https://github.com/wa-lang/wa) 的热身项目
- 凹语言项目已过5年, 完成了当初不做玩具车的目标, 是时候向凹语言迁移了
- ？

## What: µGo 例子

µGo 最初是Go语言的子集, 也是凹语言项目的起点. 所以说µGo现在更像是凹语言的子集, 当然µGo是一个玩具语言.

```go
import "libc"
import "libc.math" => m

const Pi = 3.14
const Pi_2 = Pi * 2

type MyInt :int

global x = println(1 + 2*(3+4) + -10 + double(50))

func println() => int

func main => int {}
```

## Output: 输出的目标格式

为了跨平台和方便测试，输出LLVM汇编代码，如果以后可能会增加WASM文件。

## License 版权

学习目的可免费阅读。
