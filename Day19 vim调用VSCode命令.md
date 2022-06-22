## Day19

## vim 调用 VS Code 的命令

### 格式化文档

`shift` + `alt` + `f`

在 setting.json 中添加以下配置：

```json
"vim.normalModeKeyBindingsNonRecursive":[
  // format document
  {
    "before":["<Leader>","f","d"],
    "commands":["editor.action.formatDocument"]
  },
  {
    "before":["<Leader>","r","n"],
    "commands":["editor.action.rename"]
  }
],
```

> windows 需要把 `<Leader>` 替换成 `<Space>`

### 重命名

`f2`

```json
"vim.normalModeKeyBindingsNonRecursive":[
  {
    "before":["<Leader>","r","n"],
    "commands":["editor.action.rename"]
  }
],
```

### 折叠代码

Mac: `alt` + `command` + `[`
windows: `ctrl` + `shift` + `[`

### 展示代码

Mac: `alt` + `command` + `]`
windows: `ctrl` + `shift` + `]`

```json
"vim.normalModeKeyBindingsNonRecursive":[
  {
    "before":["<Space>","["],
    "commands":[
      {
        "command":"editor.fold"
      },
      {"command": "vim.remap",
        "args":{
          "after": ["$", "%"]
        }
      }
    ]
  },
  {
    "before":["<Space>","]"],
    "commands":[{
      "command":"editor.unfold"
    }]
  }
],
```
