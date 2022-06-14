## Day13

## vim 处理包裹字符的符号（vim-surround)

- `c` + `s` + `<existing>` + `<desired>` 使用新符号替换现在字符两端的符号，例如`cs"\``
- `y` + `s` + `<existing>` + `<desired>` 在字符两端添加符号，例如：`ysiw"`
  > `ysiwt` + 标签名 可以使用标签包裹单词
- `d` + `s` + `<existing>` 删除字符两端的符号
- `S` + `<desired>` 给选中字符的两端添加符号（可视化模式下使用）
