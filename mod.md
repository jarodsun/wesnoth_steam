# 修改说明

对应版本：

Steam，1.14.16

# 文件夹

`/data/core/macros`:技能相关

`/data/core/units`:兵种相关

`/data/campaigns`:战役配置文件

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

## 3. 战役地图调整

### 3.1 Two_Brothers

中文名：兄弟传说

`scenarios`文件夹下`01_Rooting_Out_a_Mage.cfg`文件中

```
recruit=Horseman,BowmanX,Spearman,Footpad
把Bowman改为BowmanX，加强后的弓箭手，使用的是Loyalist_Bowman_X.cfg中的`id`
```

### 3.2 The_South_Guard

中文名：南疆卫队

```
data\campaigns\The_South_Guard\scenarios\01_Born_to_the_Banner.cfg
把Bowman改为BowmanX
```

### 3.3 An_Orcish_Incursion

中文名：兽人入侵

```
data\campaigns\An_Orcish_Incursion\scenarios\01_Defend_the_Forest.cfg
加入Elvish ArcherX
```

### 3.4 The_Rise_Of_Wesnoth

中文名：韦诺崛起

```
data\campaigns\The_Rise_Of_Wesnoth\scenarios\01_A_Summer_of_Storms.cfg
加入BowmanX
```
