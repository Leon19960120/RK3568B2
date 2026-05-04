*以 gpio111 为例**

打开蜂鸣器
**手动导出**

```shell
echo 111 > /sys/class/gpio/export
```

# 

```

echo out > /sys/class/gpio/gpio111/direction
# 蜂鸣器常响（假设高电平有效）
echo 1 > /sys/class/gpio/gpio120/value
sleep 1
# 蜂鸣器不响（假设高电平有效）
echo 0 > /sys/class/gpio/gpio120/value
```

LED

```shell
echo 120 > /sys/class/gpio/export
echo 121 > /sys/class/gpio/export
echo 123 > /sys/class/gpio/export
echo 124 > /sys/class/gpio/export
```

```shell
# 以 gpio120 为例
echo out > /sys/class/gpio/gpio120/direction
# 点亮（假设高电平有效）
echo 1 > /sys/class/gpio/gpio120/value
sleep 1
echo 0 > /sys/class/gpio/gpio120/value
```



```shell
[root@RK356X:/sys/class/gpio]# cat /sys/kernel/debug/gpio
gpiochip0: GPIOs 0-31, parent: platform/fdd60000.gpio, gpio0:
 gpio-6   (                    |vcc5v0_otg          ) out lo
 gpio-23  (                    |vcc3v3_lcd0_n       ) out hi
 gpio-29  (                    |vcc3v3_vga          ) out hi

gpiochip1: GPIOs 32-63, parent: platform/fe740000.gpio, gpio1:
 gpio-40  (                    |GPIO Key UP         ) in  hi
 gpio-42  (                    |GPIO Key DOWN       ) in  hi

gpiochip2: GPIOs 64-95, parent: platform/fe750000.gpio, gpio2:
 gpio-73  (                    |bt_default_rts      ) in  hi
 gpio-79  (                    |bt_default_reset    ) out lo
 gpio-80  (                    |bt_default_wake_host) in  hi
 gpio-82  (                    |bt_default_wake     ) in  lo
 gpio-84  (                    |reset               ) out hi
 gpio-94  (                    |reset               ) out lo

gpiochip3: GPIOs 96-127, parent: platform/fe760000.gpio, gpio3:
 gpio-98  (                    |spk-ctl             ) out lo
 gpio-100 (                    |vcc3v3_pcie         ) out hi
 gpio-103 (                    |reset               ) out hi
 gpio-109 (                    |mdio-reset          ) out hi
 gpio-111 (                    |sysfs               ) out lo
 gpio-114 (                    |Headphone detection ) in  lo

gpiochip4: GPIOs 128-159, parent: platform/fe770000.gpio, gpio4:
```



## 🖥️ 背光设备（屏幕/指示灯）

你之前还看到 `/sys/class/backlight/backlight/brightness`，它可以控制屏幕背光或某个可调光 LED：

```bash
# 查看最大亮度
cat /sys/class/backlight/backlight/max_brightness
# 设置亮度（例如 255）
echo 255 > /sys/class/backlight/backlight/brightness
# 熄灭
echo 0 > /sys/class/backlight/backlight/brightness
```

观察板子上是否有变化（可能是 LCD 背光或独立的指示灯）。
