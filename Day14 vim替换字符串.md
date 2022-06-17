## Day14

## vim 替换字符串

### 替换命令 :substitute

- `:` + `[range]` + `s[ubstitute]` + `/` + `{pattern}` + `/` + `{string}` + `/` + `[flags]`
  - range 范围
  - s[ubstitute] 命令
  - pattern 模式（可以使用正则表达式)
  - string 要替换成的字符串
  - flags
    > 中括号里面的内容可以不写
- 例如： `:s/vnode/haha回车` 把 vnode 替换成 haha

#### range

- `$` 光标到尾部
- `%` 全文
- `number,number` 从某行到某行，例如： 10，12

#### {pattern}

- /d 数字进行替换
- [1,2] 包含 1 和 2 的进行替换

#### flag（可以两个同时用）

- `g` 全局匹配
- `c` 弹出对话框选择替换方式

#### 可视化模式下全局替换

### 多选

*  `gb` 多光标操作替换
* `gbc` + `要替换的字符` 

### 如何查看vim帮助文档

1. `vim`
2. `:help s_flags`
> 终端内的vim可能和VSCode中的vim有所不同
