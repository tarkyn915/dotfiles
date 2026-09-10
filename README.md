# my_config

个人 Linux 配置文件（dotfiles），用 GNU stow 结构管理。

## 包含

| 包 | 内容 |
|---|---|
| niri | config.kdl + my 模块 |
| kitty | kitty.conf |

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
