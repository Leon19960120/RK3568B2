```shell
 evtest /dev/input/event0
```

读取上下键

```shell
[root@RK356X:/etc]#  evtest /dev/input/event0
Input driver version is 1.0.1
Input device ID: bus 0x19 vendor 0x1 product 0x1 version 0x100
Input device name: "gpio_keys_polled"
Supported events:
  Event type 0 (EV_SYN)
  Event type 1 (EV_KEY)
    Event code 103 (KEY_UP)
    Event code 108 (KEY_DOWN)
Key repeat handling:
  Repeat type 20 (EV_REP)
    Repeat code 0 (REP_DELAY)
      Value    250
    Repeat code 1 (REP_PERIOD)
      Value     33
Properties:
Testing ... (interrupt to exit)
Event: time 1777824128.145877, type 1 (EV_KEY), code 108 (KEY_DOWN), value 1
Event: time 1777824128.145877, -------------- SYN_REPORT ------------
Event: time 1777824128.355647, type 1 (EV_KEY), code 108 (KEY_DOWN), value 0
Event: time 1777824128.355647, -------------- SYN_REPORT ------------
Event: time 1777824129.699208, type 1 (EV_KEY), code 103 (KEY_UP), value 1
Event: time 1777824129.699208, -------------- SYN_REPORT ------------
Event: time 1777824129.905605, type 1 (EV_KEY), code 103 (KEY_UP), value 0
Event: time 1777824129.905605, -------------- SYN_REPORT ------------

```

```shell
evtest /dev/input/event1
```

```shell
evtest /dev/input/event2
```

```shell
[root@RK356X:/etc]# evtest /dev/input/event3
Input driver version is 1.0.1
Input device ID: bus 0x19 vendor 0x1 product 0x1 version 0x100
Input device name: "adc-keys"
Supported events:
  Event type 0 (EV_SYN)
  Event type 1 (EV_KEY)
    Event code 114 (KEY_VOLUMEDOWN)
    Event code 115 (KEY_VOLUMEUP)
Properties:
Testing ... (interrupt to exit)
Event: time 1777824352.272731, type 1 (EV_KEY), code 114 (KEY_VOLUMEDOWN), value 1
Event: time 1777824352.272731, -------------- SYN_REPORT ------------
Event: time 1777824352.375676, type 1 (EV_KEY), code 114 (KEY_VOLUMEDOWN), value 0
Event: time 1777824352.375676, -------------- SYN_REPORT ------------
Event: time 1777824353.202639, type 1 (EV_KEY), code 115 (KEY_VOLUMEUP), value 1
Event: time 1777824353.202639, -------------- SYN_REPORT ------------
Event: time 1777824353.408999, type 1 (EV_KEY), code 115 (KEY_VOLUMEUP), value 0
Event: time 1777824353.408999, -------------- SYN_REPORT ------------

```



