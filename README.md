# my_dotfiles

个人 Linux 配置文件（dotfiles），用 GNU stow 结构管理。

## 包含

| 软件包   | 配置文件                      | 默认目录                           |
| -------- | ----------------------------- | ---------------------------------- |
| niri     | config.kdl + my 模块          | ~/.config/niri/config.kdl          |
| kitty    | kitty.conf                    | ~/.config/kitty/kitty.conf         |
| ghostty  | config.ghostty + shaders 模块 | ~/.config/ghostty/config.ghostty   |
| typora   | darkkk.css                    | ~/.config/Typora/themes/darkkk.css |
| starship | starship.toml                 | ~/.config/starship.toml            |



## 新机器恢复

```bash
# 1. 装依赖
sudo pacman -S stow

# 2. clone 并部署
git clone https://github.com/tarkyn915/dotfiles.git ~/dotfiles
cd ~/dotfiles

# 3. 删除原本默认的配置，用stow链接接管配置文件
stow niri
stow ghostty
stow typora
···
```

## 备注

- 配置 niri 自动热重载，语法检测 `niri validate`
- kitty只用 `kitty.conf`
- ghostty 重载配置文件 `ctrl + shift + ,` shaders模块 https://github.com/sahaj-b/ghostty-cursor-shaders
- typora 重新打开窗口在theme中选择 `darkkk.css`
- starship需要在不同shell中添加配置 https://starship.rs/zh-CN/guide/

## Niri 设定快捷键

```
# 这里只列出了常用的快捷键，并不是全部内容
# 应用
Mod+Space	应用启动器  DMS spotlight 
Mod+T	    默认终端    kitty
Mod+E		文件管理器  nautilus

# 系统
Mod+Alt+L          DMS锁屏
Mod+Shift+Slash    速查表
Mod+Shift+Q        电源菜单

# 窗口移动（hjkl也是对应键位） 移动窗口也是同理  Mod+ctrl+xxx
Mod+Left    向左切换窗口
Mod+Right   向右切换窗口
Mod+Up      向上切换窗口
Mod+Down    向下切换窗口
Mod+F       切换窗口大小
Mod+M       最大化窗口
Mod+O       桌面总览
Mod+Q       关闭窗口

# 工作区切换
Mod+page_down 向下切换工作区
Mod+page_up   向上切换工作区
Mod+U   	  向下切换工作区
Mod+I   	  向上切换工作区
Mod+1/2/3     切换1/2/3工作区

```

