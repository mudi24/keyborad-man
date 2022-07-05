## Day28

## VSpaceCode（whichkey)

- VSpaceCode 面向 vim 用户
- whichkey 面向普通用户

### 打开命令面板

- `空格` + `;`
- 在 settings.json 里添加以下配置：

```json
"vim.normalModeKeyBindingsNonRecursive":[
  {
    "before":["<Space>",";"],
    "commands":["vspacecode.space"]
  },
]
```

### 在keybindings中添加按键绑定


> VSpaceCode 官方文档：https://vspacecode.github.io/docs/
