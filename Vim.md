# Vim

## 安装

```
vi + tap --- 查看vi
sudo apt-get install vim-gtk
sudo vim /etc/vim/vimrc
if has("syntax")
	syntax
endif
set nu                           // 在左侧行号
set tabstop                  //tab 长度设置为 4
set nobackup               //覆盖文件时不备份
set cursorline               //突出显示当前行
set ruler                       //在右下角显示光标位置的状态行
set autoindent             //自动缩进
```

## Bug

#### insert 下esc失灵:	Ctrl + q

## vim插件

```
#vimrc文件添加插件
Plugin 'luochen1990/rainbow' 
#插件更新
PlugUpdate
#插件安装
`PlugInstall
#插件查找
PlugSearch
#插件状态
PlugStatus
#插件管理
Vundle
```

## 快捷键

```
模式切换
Normal 模式（正常模式）：按 Esc 键进入。
Insert 模式（插入模式）：按 i 键进入。
Visual 模式（可视模式）：按 v 键进入。
Command 模式（命令模式）：按 : 进入。
```

- ### 复制黏贴

```
复制 ： (普通模式)yy nyy 
	  （v模式）y 
粘贴 ： (普通模式) p P 
剪切 ：+y
黏贴 ： （普通） +p
```

### Normal 模式快捷键

#### 光标移动

- `h`：向左移动一个字符。
- `j`：向下移动一行。
- `k`：向上移动一行。
- `l`：向右移动一个字符。
- `w`：移动到下一个单词的开头。
- `b`：移动到前一个单词的开头。
- `e`：移动到当前单词的结尾。
- `0`：移动到行首。
- `$`：移动到行尾。
- `gg`：移动到文件开头。
- `G`：移动到文件结尾。
- `H`：移动到屏幕顶部。
- `M`：移动到屏幕中部。
- `L`：移动到屏幕底部。

#### 编辑操作

- `x`：删除当前字符。
- `dd`：删除当前行。
- `dw`：删除到下一个单词的开头。
- `d$`：删除到行尾。
- `D`：删除到行尾（相当于 `d$`）。
- `yy`：复制当前行。
- `yw`：复制到下一个单词的开头。
- `y$`：复制到行尾。
- `p`：在光标后粘贴。
- `u`：撤销上一步操作。
- `Ctrl+r`：重做上一步操作。

#### 查找与替换

- `/text`：查找 `text`。
- `n`：跳到下一个匹配项。
- `N`：跳到上一个匹配项。
- `:%s/old/new/g`：全局替换 `old` 为 `new`。
- `:s/old/new/g`：当前行替换 `old` 为 `new`。

### Insert 模式快捷键

- `i`：在当前光标位置进入插入模式。
- `I`：在当前行首进入插入模式。
- `a`：在当前光标后进入插入模式。
- `A`：在当前行尾进入插入模式。
- `o`：在当前行下方新建一行并进入插入模式。
- `O`：在当前行上方新建一行并进入插入模式。
- `Esc`：退出插入模式，返回正常模式。

### Visual 模式快捷键

- `v`：进入字符可视模式。
- `V`：进入行可视模式。
- `Ctrl+v`：进入块可视模式。
- `y`：复制选中的文本。
- `d`：删除选中的文本。
- `>`：缩进选中的文本。
- `<`：反缩进选中的文本。

### Command 模式快捷键

- `:w`：保存文件。
- `:q`：退出 Vim。
- `:wq`：保存并退出 Vim。
- `:q!`：强制退出，不保存修改。
- `:e filename`：打开文件 `filename`。
- `:vsp filename`：垂直分割窗口并打开文件 `filename`。
- `:sp filename`：水平分割窗口并打开文件 `filename`。

### 窗口管理

- `Ctrl+w s`：水平分割窗口。
- `Ctrl+w v`：垂直分割窗口。
- `Ctrl+w c`：关闭当前窗口。
- `Ctrl+w o`：关闭其他窗口，只保留当前窗口。
- `Ctrl+w w`：切换到下一个窗口。
- `Ctrl+w h`：切换到左边的窗口。
- `Ctrl+w j`：切换到下边的窗口。
- `Ctrl+w k`：切换到上边的窗口。
- `Ctrl+w l`：切换到右边的窗口。

### 缓冲区管理

- `:bnext` 或 `:bn`：切换到下一个缓冲区。
- `:bprev` 或 `:bp`：切换到上一个缓冲区。
- `:bfirst`：切换到第一个缓冲区。
- `:blast`：切换到最后一个缓冲区。
- `:bd`：删除当前缓冲区。

### 标签页管理

- `:tabnew filename`：在新标签页中打开文件 `filename`。
- `:tabnext` 或 `:tabn`：切换到下一个标签页。
- `:tabprev` 或 `:tabp`：切换到上一个标签页。
- `:tabclose` 或 `:tabc`：关闭当前标签页。
- `:tabonly`：关闭其他标签页，只保留当前标签页。
