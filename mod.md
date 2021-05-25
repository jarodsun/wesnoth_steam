# 修改说明

对应版本：

Steam，1.14.16

# 文件夹

`/data/core/macros`:技能相关

`/data/core/units`:兵种相关

`/data/campaigns`:任务配置文件

# 修改说明

## 1. 技能

添加了5个超级技能

`/data/core/macros/abilities.cfg`文件内

```
ABILITY_EXTRA_HEAL_X
ABILITY_CURES_X
ABILITY_REGENERATES_X
WEAPON_SPECIAL_MARKSMAN_X
WEAPON_SPECIAL_MAGICAL_X
```

**详细说明，待添加**

## 2. 兵种

### 2.1 人类

人类兵种对应的文件夹：`/data/core/units/humans`

创建加强弓箭手，由于游戏内，采用的是一套配置文件，所以单独创建了一套兵种对应的文件，以防敌人也变强=。=

```
Loyalist_Bowman_X.cfg
Loyalist_Longbowman_X.cfg
Loyalist_Master_Bowman_X.cfg
```

`cost`下添加的技能

```
[abilities]
    {ABILITY_CURES_X}
    {ABILITY_REGENERATES_X}
    {ABILITY_LEADERSHIP_LEVEL_5}
    {ABILITY_SKIRMISHER}
[/abilities]
[resistance]
fire=0
blade=0
pierce=0
impact=0
cold=0
arcane=0
[/resistance]
```

`[attack]`下添加武器技能，两个武器都添加了

```
[specials]
    {WEAPON_SPECIAL_FIRSTSTRIKE}
    {WEAPON_SPECIAL_MARKSMAN_X}
    {WEAPON_SPECIAL_DRAIN}
[/specials]
```

## 3. 兵种配置到任务地图

### 3.1 Two_Brothers

`scenarios`文件夹下`01_Rooting_Out_a_Mage.cfg`文件中

```
recruit=Horseman,BowmanX,Spearman,Footpad
把Bowman改为BowmanX，加强后的弓箭手，使用的是Loyalist_Bowman_X.cfg中的`id`
```
