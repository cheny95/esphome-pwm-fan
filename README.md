# esphome-pwm-fan
8266通过ESPHOME使用PWM控制无级调速风扇

![yaofan](https://user-images.githubusercontent.com/6293952/196037499-17ef6aec-9fe4-4fc2-a4ac-811a12bfb380.jpg)

## 硬件
- 12V电源（5.5mm或线头式的随意，取决于你的降压模块和是否焊接）
- 12V转5V降压模块
- PWM MOS管
- 12V风扇
- 8266模块

## 连接
1. 首先将12V单元焊接到降压模块的正负极输入上，如果你的降压模块带5.5mm插头的也可以直接用电源插入。注意此时电源先不接入220V.
2. 降压板的12V输出接MOS管的正负极输入，MOS管的正负极输出接风扇的正负极。注意风扇的正负极，反接风扇不转。
3. 12V电源的USB输出口，插入Micro USB给8266供电。
4. 8266的D4接口接到MOS管的PWM针脚，G接到MOS管的GND.
5. 8266的5V输出和G接到SHTC3的正负极，D5、D6分别接到SDA和SCL。

## 烧录
1. 8266的USB接入电脑或HA主机，用esphome刷入仓库内的yaml文件。
2. 烧录成功后，12V接上电源，USB接回降压板上。（8266亦可单独供电）
3. 此时通电后，风扇过5秒左右会自动启动。

## 接入
1. 直接在HA的设备里，新增集成。选择esphome
2. 通过路由器找到风扇的IP
3. 集成添加8266的IP即可

## 交流
- QQ群：198841186

- 微信群：(添加该机器人，发送“进群”会自动发送邀请链接）

![xiaomi miot weixin group](https://user-images.githubusercontent.com/4549099/161735971-0540ce1c-eb49-4aff-8cb3-3bdad15e22f7.png)
