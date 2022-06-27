## 第一天 vim01

### VS Code 下载 vim 扩展

### vim 模式切换

- vim 默认为 normal 模式，
- 进入输入（insert）模式：
  - 点击`i`键，输入位置在当前光标选中的位置的前面
  - 点击`a`键，输入位置在当前光标选中的位置的后面
- 退出 输入（insert）模式，点击`esc`键或者点击`control`+`[`键

### vim 方向移动

- `j`键：向下移动
- `k`键：向上移动
- `h`键：向左移动
- `l`键：向右移动

#### 练习

```js
const a = 1;
const b = 1;
```

```js
const aa = 11;
const bb = 11;
```

### 终端中退出 vim

- `vim test` 有 test 文件则进入 test 文件，没有 test 文件则创建 test 文件
- `:wq` 写入内容并退出
- `cat test.txt` 查看当前 test 文件的内容
- `:q!` 强制退出(不保存当前对文件的修改)

### control 和 caps lock 调换位置

- 设置 => 键盘 => 修饰符

### 在 VS Code 中把 ESC 键映射到`j`+`k`

- 在 VS Code 中按下`command` + `shift` + `p`，选择 setting.json 文件
- 添加以下配置

```json
"vim.insertModeKeyBindings":[
    {"before": ["j","k"], "after": ["<Esc>"]}
]
```

> 或者下载一个软件：https://karabiner-elements.pqrs.org/

![image](./images/Day1.png)

### 在 vim 中快速移动

- 修改 VS Code 中的 vim 配置，点击 https://github.com/VSCodeVim/Vim#mac ，复制下面这几条命令

```shell
defaults write com.microsoft.VSCode ApplePressAndHoldEnabled -bool false              # For VS Code
defaults write com.microsoft.VSCodeInsiders ApplePressAndHoldEnabled -bool false      # For VS Code Insider
defaults write com.visualstudio.code.oss ApplePressAndHoldEnabled -bool false         # For VS Codium
defaults write com.microsoft.VSCodeExploration ApplePressAndHoldEnabled -bool false   # For VS Codium Exploration users
defaults delete -g ApplePressAndHoldEnabled
```

- 调整键盘灵活度，设置 => 键盘 ，按键重复和重复前延迟都跳到最右边
- 在搜狗输入法的 ABC 模式下，就可以实现快速移动（点击`shift`切换搜狗中英文模式）
