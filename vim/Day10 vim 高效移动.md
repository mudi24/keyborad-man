## Day10

## vim 高效移动

### vim-easymotion

在 vim 中使用 easymotion 需要先开启，在 setting.json 中添加配置：

```json
"vim.easymotion": true,
```

在 vim 中修改`<leader>`对应的键位，下面会用到

```json
"vim.leader": "<Space>",
```

#### 基于单词的移动

- `<leader>` + `<leader>` + `w` 快速移动到单词的头部（向光标下面进行移动）
- `<leader>` + `<leader>` + `b` 快速移动到单词的尾部（向光标上面进行移动）
- `<leader>` + `<leader>` + `e` 快速移动到字符的尾部（向光标下面进行移动）
- `<leader>` + `<leader>` + `g` + `e` 快速移动到字符的尾部（向光标上面进行移动）

#### 基于行的移动

- `<leader>` + `<leader>` + `j` 快速移动到某行（向光标下面进行移动）
- **`<leader>` + `<leader>` + `k` 快速移动到某行（向光标上面进行移动） **
- `<leader>` + `<leader>` + `h` 快速移动到某行开头、结尾、大小写、`_`、`,`和`#`（向光标上面进行移动）
- `<leader>` + `<leader>` + `l` 快速移动到某行开头、结尾、大小写、`_`、`,`和`#`（向光标下面进行移动）

- `<leader>` + `<leader>` + `<leader>` + `j` 快速移动到某行（向光标上下任意进行移动）

### vim-sneak

在 setting.json 中添加以下配置，开启使用 sneak:

```json
"vim.sneak": true,
```

#### 基于全局进行跳转（基于两个字符进行跳转）

- `s` + 两个字符 全局查找（和`f`查找类似，向下查找）
- `S` + 两个字符 全局查找（向上查找）

* `;` 重复上次的字符查找命令（跳转到下一个字符的位置）
* `,` 反转方向查找上次的字符查找命令（跳转到上一个字符的位置）

#### 改键避免冲突

在 setting.json 中添加以下配置：

```json
"vim.normalModeKeyBindingsNonRecursive":[ // 非递归
    {
        "before": ["f"],
        "after": ["s"]
    },
    {
        "before": ["F"],
        "after": ["S"]
    },
    {
        "before": ["s"],
        "after": ["c" , "l"]
    },
    {
        "before": ["S"],
        "after": ["^" , "C"]
    },
]
```

还要在可视化模式下也添加映射

```json
"vim.visualModeKeyBindingsNonRecursive":[ // 非递归
    {
        "before": ["f"],
        "after": ["s"]
    },
    // 可视化模式下不支持 S
    // {
    //     "before": ["F"],
    //     "after": ["S"]
    // },
]
```

在使用修饰符的同时也添加`f`键进行高效移动

```json
"vim.operatorPendingModeKeyBindingsNonRecursive":[ // 非递归
    {
        "before": ["f"],
        "after": ["z"]
    },
    {
        "before": ["F"],
        "after": ["Z"]
    },
]
```

- `f` 替换 `s`
- `F` 替换 `S`

  > 这样`F` ,`f`可以同时搜索一个字符和两个字符

- `s` 删除当前字符
- `C` 删除从当前光标到行尾的字符
- `S` 删除本行字符并进入 Insert 模式
