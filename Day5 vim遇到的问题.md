## Day5 vim05

### vim 切换大写

- `v` + `e` 选中单词，`shift` + `~` 把单词每个字母都变成大写
- `g` + `U` + `i`+`w` 把当前光标所在的单词变成全部大写

### vim 中`control`+`c`会直接由 insert 模式进入 normal 模式

还是在 setting.json 文件中添加以下配置：

```json
"vim.handleKeys": {
    "<C-c>":false
}
```

### vim 中的insert模式下与系统快捷键配合操作

* insert模式下使用上下左右键进行移动
* `control` + `w` 删除光标前的单词内容
