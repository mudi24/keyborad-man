## Day25

## vscode

### 显示侧边代码控制面板

* `ctrl` + `shift` + `g`
* `空格` + `g` + `g`

```json
"vim.normalModeKeyBindingsNonRecursive":[
  {
    "before":["<Space>","g","g"],
    "commands":["workbench.view.scm"]
  }, 
] 
```

### git 添加到缓存区（git add .）

* `空格` + `g` + `s`

```json
{
  "before":["<Space>","g","s"],
  "commands":["git.stageChange"]
}, 
```


### git 提交（git commit）

* `空格` + `g` + `c`

```json
{
  "before":["<Space>","g","c"],
  "commands":["git.commit"]
}, 
```


### git 查看差异（git diff）

* `空格` + `g` + `d` + `f`

```json
{
  "before":["<Space>","g","d","f"],
  "commands":["git.openChange"]
}, 
```


### git 取消add

* `空格` + `g` + `u`

```json
{
  "before":["<Space>","g","u"],
  "commands":["git.openChange"]
}, 
```


### git 取消对文件的修改

* `空格` + `g` + `c` + `l`

```json
{
  "before":["<Space>","g","c","l"],
  "commands":["git.clean"]
}, 
```