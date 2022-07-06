## Day30

## vscode 终端

### 打开终端

- `ctrl` + ``` 打开终端并自动切换到命令行
- `command` + `j` 打开终端

### 清除终端命令历史

- `ctrl` + `k` windows 自行配置

### 在终端右边打开命令行窗口

- `ctrl` + `shift` + `5` windows
- `command` + `\` mac

### 在左右两个终端窗口进行切换

- `alt` + `方向键` windows

### 关闭当前命令行窗口

- `shift` + `alt` + `q` 自行配置

### 打开新的终端

- `ctrl` + `shift` + ```

### 切换终端组

- `ctrl` + `shift` + `方向键`

### 打开外部终端

- `ctrl` + `shift` + `c` 打开系统自带的终端
- 自己配置打开指定的终端，在 settings.json 中添加以下配置：

```json
"terminal.external.osxExec": "iTerm.app"
```

### 一键打开终端，并进入lazygit模式的插件
* 下载 quick open lazygit 插件
* `npm install ttab -g`
* 如果在 iTerm2 中使用，则要在 settings.json中添加：`quickOpenLazygit.useITerm = true`

* `command` + `g` + `o` 一键打开lazygit 
> 插件仓库：https://github.com/cuixiaorui/quickOpenLazygit.git