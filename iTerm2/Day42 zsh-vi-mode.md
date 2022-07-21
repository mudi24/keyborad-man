## Day42

## zsh-vi-mode 

### 安装
* `brew install zsh-vim-mode`
* 添加配置到.zshrc文件中


### 退回normal模式配置
* `esc`
* `ctrl` + `[`
* 如何配置jj?jk?
  * 通过环境变量来控制，把如下配置添加到.zshrc文件中：
    * `ZVM_VI_INSERT_ESCAPE_BINDKEY=jk`
    * `ZVM_VI_VISUAL_ESCAPE_BINDKEY=jk`
    * `ZVM_VI_OPPEND_ESCAPE_BINDKEY=jk`

### 移动
* `b` 和 `e`  
* `b` + `d` + `i` + `w` 删除当前单词
* 操作与在vim几乎相同

### history
#### 查看历史
* normal 模式
  * `ctrl` + `p` 
  * `ctrl` + `n`
* insert 模式
  * `j` `k`

#### 搜索
* insert 模式
  * `ctrl` + `r`
* normal 模式
  * `/`
  * `n`  `N` 前后切换

#### 使用原生的vim `vv`