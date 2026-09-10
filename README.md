# my_config

个人 Linux 配置文件（dotfiles），用 GNU stow 结构管理。

## 包含

| 包 | 内容 |
|---|---|
| niri | Wayland 合成器配置（config.kdl + my/ 模块化拆分） |
| kitty | 终端配置 |

## 新机器恢复

```bash
# 1. 装依赖
sudo pacman -S stow niri kitty

# 2. clone 并部署
git clone https://github.com/<用户名>/my_config.git ~/my_config
cd ~/my_config
stow niri kitty
```

## 日常修改流程

```bash
# 改配置（路径和以前完全一样，软链接透明）
vim ~/.config/niri/my/layout.kdl

# 存档
cd ~/my_config
git add -A && git commit -m "描述改了啥" && git push
```

## 备注

- `niri/.config/niri/dms/` 由 DankMaterialShell 自动生成，已 gitignore。
- niri include 是位置性的：后面的覆盖前面的。模块按骨架中的顺序加载。
- 改完配置 niri 自动热重载；语法不确定时跑 `niri validate`。
