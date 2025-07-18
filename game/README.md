# 艾诺迪亚风格RPG游戏 - 完整版

## 游戏概述
这是一个基于Python和Pygame开发的2D RPG游戏，包含完整的RPG游戏要素。

## 核心功能

### 1. 基础RPG系统
- **角色系统**: 血量、魔法值、等级、经验值、金币
- **属性成长**: 升级时自动提升攻击力、血量、魔法值
- **背包系统**: 可收集金币、血瓶、装备等物品
- **技能系统**: 火球术、治疗术、护盾术等魔法技能

### 2. 战斗系统
- **实时战斗**: 玩家与敌人实时碰撞战斗
- **技能释放**: Q键火球术、E键治疗术、R键护盾术
- **投射物系统**: 火球术会发射投射物攻击远程敌人
- **护盾系统**: 护盾术可以减少受到的伤害
- **暴击系统**: 10%概率产生暴击，造成双倍伤害

### 3. 敌人AI系统
- **多种敌人类型**: 基础敌人、精英敌人、Boss敌人
- **智能AI**: 巡逻、追击、攻击三种状态
- **视野系统**: 敌人有视野范围，发现玩家后会追击
- **不同属性**: 不同类型敌人有不同的血量、攻击力、速度

### 4. 装备系统
- **装备类型**: 武器、护甲、饰品
- **装备属性**: 攻击力、防御力、生命值、魔法值加成
- **等级限制**: 装备有等级要求
- **装备收集**: 拾取装备后放入背包，玩家手动选择装备

### 5. 战利品系统
- **随机掉落**: 敌人死亡后随机掉落金币、血瓶、装备
- **掉落概率**: 不同物品有不同的掉落概率
- **等级关联**: 高等级敌人掉落更好的装备

### 6. 波次系统
- **无尽挑战**: 清空敌人后自动生成下一波
- **难度递增**: 每波敌人数量增加，高波次出现精英和Boss
- **敌人类型**: 第3波开始出现精英，第5波开始出现Boss

### 7. 界面系统
- **状态显示**: 血条、魔法条、等级、经验、金币
- **技能UI**: 技能图标、冷却时间、魔法消耗显示
- **战斗信息**: 实时显示战斗消息和系统提示
- **操作提示**: 按键说明和使用提示

### 8. 存档系统
- **保存游戏**: F5键快速保存，菜单保存
- **加载游戏**: 主菜单继续游戏选项
- **数据持久化**: 保存玩家属性、游戏进度、装备状态

### 9. 菜单系统
- **主菜单**: 开始游戏、继续游戏、退出游戏
- **暂停菜单**: ESC键暂停，可继续、保存、返回主菜单
- **键盘操作**: 上下键选择，回车确认

### 10. 输入法兼容
- **中文字体**: 自动检测并使用系统中文字体
- **按键处理**: 事件驱动的按键处理，避免输入法干扰
- **移动方案**: 提供连续按键和事件驱动两种移动方案

## 操作说明

### 基本操作
- **WASD键**: 移动角色
  - W键：向上移动
  - A键：向左移动
  - S键：向下移动
  - D键：向右移动
- **H键**: 使用血瓶
- **Q键**: 释放火球术
- **E键**: 释放治疗术
- **R键**: 释放护盾术
- **F5键**: 快速保存
- **ESC键**: 暂停游戏

### 技能说明
- **火球术**: 消耗20魔法值，向鼠标位置发射火球，造成50点伤害
- **治疗术**: 消耗15魔法值，恢复50点生命值
- **护盾术**: 消耗25魔法值，获得10点防御力，持续10秒

### 装备说明
- **铁剑**: +15攻击力
- **钢剑**: +25攻击力，需要3级
- **皮甲**: +8防御力，+20生命值
- **链甲**: +15防御力，+40生命值，需要4级
- **魔法戒指**: +30魔法值，需要2级
- **力量护符**: +10攻击力，+5防御力，需要5级

## 文件结构
```
game/
├── main.py                # 原始游戏主循环
├── game_enhanced.py       # 增强版游戏主循环（推荐使用）
├── player.py              # 玩家类
├── enemy.py               # 敌人类
├── item.py                # 物品类
├── map.py                 # 地图类
├── hud.py                 # 界面显示
├── battle.py              # 战斗系统
├── game_state.py          # 游戏状态管理
├── skill_system.py        # 技能系统
├── equipment.py           # 装备系统
├── save_system.py         # 存档系统
├── font_manager.py        # 字体管理
├── test_h_key.py          # 按键测试
├── simple_test.py         # 简单测试
└── requirements.txt       # 依赖包
```

## 运行方式
1. 确保安装了Python 3.7+
2. 安装依赖: `pip install pygame`
3. 运行游戏: `python game_enhanced.py`

## 数据结构展示
游戏还包含了有序/无序顺序表查找性能对比的演示程序(`../main.py`)，用于展示数据结构的性能差异。

## 技术特点
- **面向对象设计**: 清晰的类结构和模块化设计
- **事件驱动**: 高效的事件处理系统
- **状态管理**: 完善的游戏状态管理
- **数据持久化**: JSON格式的存档系统
- **跨平台兼容**: 支持Windows、Linux、Mac
- **中文支持**: 完整的中文显示和输入法兼容

## 后续扩展建议
1. **更多技能**: 冰冻术、闪电术、群体攻击等
2. **职业系统**: 战士、法师、弓箭手等职业
3. **多层地图**: 不同场景和关卡
4. **NPC系统**: 商店、任务、对话
5. **成就系统**: 成就奖励和统计
6. **音效**: 背景音乐和音效
7. **多人模式**: 联机对战或合作
8. **图形优化**: 使用精灵图片替代几何图形

这个RPG游戏提供了完整的游戏体验，包含了现代RPG游戏的核心要素，同时保持了代码的清晰性和可扩展性。
