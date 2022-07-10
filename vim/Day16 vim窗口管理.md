## Day16

## vim 窗口管理

### 新建窗口

- `ctrl` + `w` `v` 左右
- `ctrl` + `w` `s` 上下

### 窗口切换

- `ctrl` + `w` `h`/`j`/`k`/`l`
- `ctrl` + `w` `w`

### 关闭窗口

- `ctrl` + `w` `c`

### 只保留当前窗口，关闭其他所有的窗口

- `ctrl` + `w` `o`

## VS Code 窗口管理

### 新建窗口

- `command` + `\`
- `command` + `ctrl` + `\` 在上方新建窗口

### 关闭窗口

- `command` + `w`
- `command` + `k` + `w`

### 窗口切换

- `shift` + `方向键`
- `shift` + `ctrl` + `j`/`k`/`h`/`l` 没有改键的话使用
- 在 keybinding.json 中添加配置：
```json
{
  // window move left
 "key": "shift+left",
 "command": "vim.remap",
 "when": "vim.mode == 'Normal",
 "args": {
  "after": ["<c-w", "h"]
 } 
}
{
  // window move right
 "key": "shift+right",
 "command": "vim.remap",
 "when": "vim.mode == 'Normal",
 "args": {
  "after": ["<c-w", "l"]
 } 
}
{
  // window move up
 "key": "shift+up",
 "command": "vim.remap",
 "when": "vim.mode == 'Normal",
 "args": {
  "after": ["<c-w", "k"]
 } 
}
{
  // window move bottom
 "key": "shift+bottom",
 "command": "vim.remap",
 "when": "vim.mode == 'Normal",
 "args": {
  "after": ["<c-w", "j"]
 } 
}
```