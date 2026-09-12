# my_config

个人 Linux 配置文件（dotfiles），用 GNU stow 结构管理。

## 包含

| 包 | 内容 |
|---|---|
| niri | config.kdl + my 模块 |
| kitty | kitty.conf |
| ghostty | config.ghostty（独立于 kitty,与 kitty 配置并存） |

## 新机器恢复

```bash
# 1. 装依赖
sudo pacman -S stow

# 2. clone 并部署
git clone https://github.com/username/my_config.git ~/my_config
cd ~/my_config
stow niri kitty
```

## 备注

- 改完配置 niri 自动热重载；语法不确定时跑 `niri validate`
- kitty只用 `kitty.conf`

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

