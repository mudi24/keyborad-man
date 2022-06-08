## vim08

### vim 滚动

- `control` + `f` 向下滚动一屏
- `control` + `b` 向上滚动一屏
- `control` + `d` 向下滚动半屏
- `control` + `u` 向上滚动半屏
- `control` + `e` 向下滚动一行（光标不会移动）
- `control` + `y` 向上滚动一行（光标不会移动）

#### vim 快速移动 5 行

在 setting.json 里面添加以下配置：

- 可视化模式

```json
"vim.visualModeKeyBindings": [
    {"before": ["J"], "after": ["5","j"]},
    {"before": ["K"], "after": ["5","k"]},
]
```

- 正常模式

```json
"vim.normalModeKeyBindings":[
    {"before": ["J"], "after": ["5","j"]},
    {"before": ["K"], "after": ["5","k"]},
]
```


### vim 移动光标 

* `z` + `z` 将当前行置于屏幕中央
* `z` + `t` 将当前行置于屏幕顶部
* `z` + `b` 将当前行置于屏幕底部
* `g` + `g` 调到文件首部
* `G` 调到文件尾部
* `行数` + `g` + `g` 调到指定行
* `行数` + `G` 调到指定行


