## Day27

## vscode 重构

### 重构按键

- `ctrl` + `shift` + `r` 只展示重构代码相关操作
- `ctrl` + `.` 展示重构代码和其他选项

### vim选中函数中所有代码

* `v` + `i` + `i`

### 提炼为一个函数

- 选中要提炼的代码
- `ctrl` + `.` 选中提炼成一个函数
- 也可以提炼成一个内联的函数

### 提炼为一个变量

- 和提炼为函数操作基本一致
- 选中变量名，`ctrl` + `.` 提炼为一个变量

## 插件
> 语法报错的话需要先修改语法错误才可以进行重构操作
### Abracadabra

### hocus pocus

- 先使用变量/函数，再创建变量/函数
- 在 settings.json 中配置快捷键

```json
"vim.normalModeKeyBindingsNonRecursive":[
  {
    "before":["<Space>","f","f"],
    "commands":["hocusPocus.createFunction"]
  },
  {
    "before":["<Space>","v","v"],
    "commands":["hocusPocus.createVariable"]
  },
]
```

### javascript booster

* 这个插件与Abracadabra的功能是可以互补的，可以同时使用