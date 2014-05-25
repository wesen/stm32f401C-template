STM32f401C-template
===================

Template for starting out with STM32F401C-Disco

---

This is just a quick template for getting started aimed at working more or less out of the box. This is far from complete though but it was quite annoying for me to set up so hopefully this helps somebody else.. :)

---

Prerequisites:

* Download and install GNU toolkit for ARM from [https://launchpad.net/gcc-arm-embedded]
* Make sure the toolkit is available on your PATH (e.g., sudo -s 'echo "_(location of tookit)_/bin" > /etc/paths.d/arm-toolkit')
* Use openocd in conjunction with arm-none-eabi-gdb to debug / upload

```
openocd -f board/stm32f4discovery.cfg
```
