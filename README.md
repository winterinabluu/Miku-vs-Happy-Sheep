# Miku vs Happy Sheep

`Miku vs Happy Sheep` 是一个基于 Python 和 pygame 编写的 2D 射击小游戏。项目整体结构参考了经典的 Alien Invasion 游戏：玩家控制屏幕底部的角色左右移动并发射子弹，击落从屏幕上方横向移动、逐步下降的目标队列。

项目最早创建提交于 2018-07-13 14:13:52 UTC，属于个人学习 pygame 时的小练手作品，轻松看看、随手跑跑就好。

## 游戏玩法

- 点击开始界面的 **Play** 按钮进入游戏。
- 使用左右方向键移动底部角色。
- 按空格键发射子弹。
- 子弹击中目标后会移除对应目标。
- 清空一整波目标后，游戏会生成新的目标队列。
- 如果目标撞到玩家或到达屏幕底部，玩家会损失一次机会。
- 按 `Esc` 可以退出游戏。

## 运行环境

项目代码使用 Python 3 编写，主要依赖：

- Python 3.6 或更高版本
- pygame

仓库中包含一个 Windows 64 位、Python 3.6 对应的 pygame wheel 文件：

```bash
pygame-1.9.3-cp36-cp36m-win_amd64.whl
```

如果你的环境正好是 Windows + Python 3.6，可以使用该 wheel 安装；其他环境建议直接通过 pip 安装 pygame。

## 安装与运行

1. 克隆仓库：

```bash
git clone https://github.com/winterinabluu/Miku-vs-Happy-Sheep.git
cd Miku-vs-Happy-Sheep
```

2. 安装 pygame：

```bash
pip install pygame
```

或者在 Windows + Python 3.6 环境下使用仓库内的 wheel：

```bash
pip install pygame-1.9.3-cp36-cp36m-win_amd64.whl
```

3. 启动游戏：

```bash
python alien_invasion.py
```

## 操作方式

| 按键/操作 | 功能 |
| --- | --- |
| 鼠标点击 Play | 开始游戏 |
| 左方向键 | 向左移动 |
| 右方向键 | 向右移动 |
| 空格键 | 发射子弹 |
| Esc | 退出游戏 |

## 项目结构

```text
.
├── alien_invasion.py      # 游戏入口，初始化 pygame、窗口、对象和主循环
├── settings.py            # 游戏窗口、速度、子弹、目标队列等配置
├── game_functions.py      # 事件处理、碰撞检测、目标队列生成和画面刷新
├── ship.py                # 玩家角色逻辑
├── alien.py               # 目标角色逻辑
├── bullet.py              # 子弹逻辑
├── button.py              # Play 按钮
├── game_stats.py          # 游戏状态与剩余机会
├── images/                # 游戏图片素材
└── pygame-*.whl           # pygame 安装包，适用于特定 Windows/Python 版本
```

## 备注

- 当前仓库还包含 `.idea/` 和 `__pycache__/` 等开发环境或缓存文件，它们不是运行游戏所必需的。
- 代码中的函数名 `chect_keydown_events` 和 `chect_keyup_events` 存在拼写问题，但不影响当前游戏运行。
- 如果 pygame 无法加载图片，请确认运行命令时所在目录是仓库根目录。
