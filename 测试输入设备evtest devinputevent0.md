```shell
 evtest /dev/input/event0
```

//读取ADC按键

```shell
[root@RK356X:/sys/class/gpio]#  evtest /dev/input/event0
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
Event: time 1777906431.204591, type 1 (EV_KEY), code 108 (KEY_DOWN), value 1
Event: time 1777906431.204591, -------------- SYN_REPORT ------------
Event: time 1777906431.411026, type 1 (EV_KEY), code 108 (KEY_DOWN), value 0
Event: time 1777906431.411026, -------------- SYN_REPORT ------------
Event: time 1777906432.341233, type 1 (EV_KEY), code 103 (KEY_UP), value 1
Event: time 1777906432.341233, -------------- SYN_REPORT ------------
Event: time 1777906432.547670, type 1 (EV_KEY), code 103 (KEY_UP), value 0
Event: time 1777906432.547670, -------------- SYN_REPORT ------------
```



```
[root@RK356X:/sys/class/gpio]# ls /dev/input
by-path  event0  event1  event2  event3  event4  event5

```

