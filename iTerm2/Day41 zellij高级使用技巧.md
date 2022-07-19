## Day41

## zellij 高级使用

### session

当前窗口状态

- 创建
  - `ctrl` + `o` `d` 创建随机名称的 session
  - `zj attach -c <session name>` 创建指定名称的 session
- 使用
  - `zj attach <session name>` 简写 `a`
- 查看
  - `zj list-sessions` 简写 `ls`
- 清空
  - `kill-session` 简写 `k`
  - `kill-all-session` 简写 `ka`

### sync

同步到全部窗口，通常用于切换路径

- `ctrl` + `t` `s`

### 滚动

- `ctrl` + `s` 进入滚动状态
- `j/k` 上下滚动
- `u/d` 翻页

### 清理

- `clear`

### 修改配置

- `mkdir ~/.config/zellij`
- `zellij setup --dump-config > ~/.config/zellij/config.yaml`
