<!-- markdownlint-disable MD033 MD041 -->
<p align="center">
  <img alt="LOGO" src="imags/logo.png" width="256" height="256" />
</p>

<div align="center" style="font-size: 30px;font-weight: bold;">Maa-WJDR</div>

## 现有功能

银行存储、英雄招募、仓库补给、仓库体力、联盟捐献、探险奖励、生命之树、晨曦回礼、训练士兵、联盟互助、任务奖励领取、联盟宝箱、邮件领取、游荡商人、统帅奖励、储值中心、宠物寻宝、宠物技能、采集资源、领主指令、灯塔情报、炼晶实验室、游历补给、雪原商路、体力补给、逐光之旅、角色切换、打开集结、竞技场。


## 使用环境

<h4>推荐使用<font color=#c00000>MuMu模拟器</font></h4>

修改模拟器分辨率为**手机**分辨率，**720*1280**、**1080*1920**均可。

> 其他模拟器可能存在部分任务无法执行，如：联盟捐献。
>
> 请自行测试。

## 安装与更新

### 安装使用

#### 启动软件

解压下载好的压缩包，运行`Maa-WJDR.exe`即可。

> 建议将解压后的`Maa-WJDR`目录移动至不包含中文字符的目录下，如：`D:\Program Files\Maa-WJDR`。

[<font color=#c00000>！！！启动报错！！！看这里</font>](#启动助手报错)


#### 连接模拟器

运行软件后，仔细阅读公告后，关闭公告弹窗。点击左上角`连接模拟器`按钮，在连接设备弹窗中点击`一键连接设备`按钮。

> 注意：在连接前，请先启动模拟器，启动游戏，并确定进入首页！！！

[<font color=#c00000>！！！连接设备失败！！！看这里</font>](#连接设备失败)
### 版本更新

更新软件时，删除助手目录下的`_internal`、`assets`和`Maa-WJDR.exe `文件目录，将压缩包中的对应的三个文件目录复制到助手目录下，最后运行`Maa-WJDR.exe`。

```text
MAA-WJDR
├─ _internal // 更新时需要替换的目录
├─ assets    // 更新时需要替换的目录
├─ config    // 助手配置文件目录，更新时保留（启动助手助手后产生）
├─ log       // 日志文件目录（启动助手后产生）
├─ user_data // 用户配置文件目录（启动助手后产生）
│  └─ 888888888.json // 用户ID为888888888的配置文件（连接模拟器成后产生）
└─ Maa-WJDR.exe      // 助手启动程序
```

### 任务配置

**修改任务配置的正确步骤：**

1. **关闭助手**：确保已经连接模拟器并成功识别到用户账号ID后，关闭助手；
2. **修改配置**：在助手所在目录中`user_data`文件夹下，在里找要该配置的账号，用文本编辑器软件（如记事本）打开以账号ID命名的`.json`文件。`true`为开，`false`为关，**修改后保存文件！**
3. **启动助手**：保存修改后的配置文件，并启动助手。

#### 配置信息

****

```python
# 游荡商人任务是否启用
wanderingMerchantEnable = true
# 游荡商人任务折扣商品列表（可删除内容，删除成对大括号{}即可，如删除整个：{"id": "ExpeditionSkillBook", "name": "史诗远征技能书", "discount_ge_buy": "-25%", }。）
wanderingMerchantDiscountGoodsList = [
    {"id": "ExpeditionSkillBook", "name": "史诗远征技能书", "discount_ge_buy": "-25%", },
    {"id": "CommanderExperience", "name": "统帅经验", "discount_ge_buy": "-25%", }
]

# 灯塔情报任务是否启用
lighthouseIntelligenceEnable = true

# 雪原商路任务是否启用
snowfieldTradeRouteEnable = true
# 雪原商路分享列表（可自由增减）
snowfieldTradeRouteShareList = [
    # 0<=战力<90,000,000并且货物品质>=5的目标会被分享至“低战专用”的群聊
    {"targetName": "低战专用", "powerMinNum": "0", "powerMaxNum": "90,000,000", "goodsQuality": 5},
    {"targetName": "雪原商路", "powerMinNum": "90,000,000", "powerMaxNum": "250,000,000", "goodsQuality": 0},
    {"targetName": "联盟", "powerMinNum": "250,000,000", "powerMaxNum": "350,000,000", "goodsQuality": 0},
]
# 当前用户是否校验货物品质，大于0时进行校验
snowfieldTradeRouteGoodsQuality = 5

# 采集资源任务是否启用
collectResourcesEnable = true
# 采集资源是否启用联盟资源矿
collectResourcesUnionMineEnable = true
# 采集资源设置等级是否启用
collectResourcesSetLevelEnable = true
# 采集资源等级（为空时默认为最大等级采集，若需指定等级，改为对应数字即可，如：[6,7,7,7]）
collectResourcesLevel = [null, null, null, null]
# 联盟总动员任务是否启用（尚未写完的任务，开启无用！！！）
unionMobilizationEnable = false
# 领主指令任务是否启用
lordCommandEnable = true
# 炼晶实验室任务是否启用
crystalRefiningLaboratoryEnable = true
# 仓库体力任务是否启用
warehousePhysicalStrengthEnable = true
# 仓库体力领取时间（提前多久领取，单位分钟，最小值为1）
warehousePhysicalStrengthCollectionTime = 60
# 游历补给任务是否启用
travelSupplyEnable = true
# 角色切换任务是否启用【使用说明详见“角色切换”】
roleSwitchEnable = false
# 角色切换间隔，单位分钟
roleSwitchInterval = 60
# 角色切换用户名列表
roleSwitchNameList = null
# 逐光之旅任务是否启用
journeyToTheLightEnable = true
# 训练士兵是否启用（依次为盾矛射）
trainSoldiersEnable = [true, true, true]
# 训练士兵是否优先晋升
barracksPriorityPromotion = true
# 打开集结是否启用
openAssembleEnable = true
# 竞技场是否启用
arenaEnable = true
# 竞技场执行时间
arenaExecuteTime = "23:05"
# 竞技场挑战战力倍数（优先挑战低于阈值战力的目标）
arenaChallengeMultiple = 0.85
# 战争学院是否解锁（true时为5爪野兽，false时为4爪野兽）【临时配置，后续版本将会删除】
warCollegeUnlocked = true
```

#### 角色切换

角色切换**默认为关闭状态**。

角色切换使用推荐步骤：

1. 开启角色切换任务，然后启动`Maa-WJDR助手`；[<font>修改方式详见任务配置</font>](#任务配置)
2. 让助手自动执行角色切换任务，此时助手会根据识别到的角色列表生成`roleSwitchNameList`配置，根据自己需要进行增减即可。

> **同一手机号下的角色**配置，只需修改**当前登录的角色**即可。

## 常见问题

### 启动助手报错：

若启动助手出现以下报错信息，则为缺少[Visual C++ Redistributable](https://learn.microsoft.com/zh-cn/cpp/windows/latest-supported-vc-redist?view=msvc-170#visual-c-redistributable-v14)运行环境，根据电脑cpu架构选择版本下载安装即可。

fileNotfoundError：`Maa-WJDR\\_internal\\maa\\bin\\MaaToolkit.dll`
![fileNotfoundError](imags/fileNotfoundError-MaaToolkit.dll.jpg)

### 连接设备失败
若连接模拟器出现以下报错信息，请尝试**重启助手**或**重启电脑**后重试。

`连接设备失败: Device connection failed`

> 若连接地址不是`127.0.0.1:xxxx`，则需要将模拟器的网络桥接模式关闭后再次尝试连接。

![连接设备失败 Device connection failed.png](imags/%E8%BF%9E%E6%8E%A5%E8%AE%BE%E5%A4%87%E5%A4%B1%E8%B4%A5%20Device%20connection%20failed.png)
### 运行任务时出现乱点情况

请确认模拟器分辨率为**手机**分辨率，**720*1280**、**1080*1920**均可。

### 新区30级后灯塔情报无法识别到野兽情报

这是因为区服的`战争学院`没有解锁，助手前期默认30级以后野兽情报为`5爪野兽`，及解锁`战争学院`后的野兽，为了避免老用户大量修改配置，目前继续沿用默认已解锁的状态。

解决办法：按照修改配置的方式，将`warCollegeUnlocked`改为`false`即可。

