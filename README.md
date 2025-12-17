此为Fork版本，添加了橙狐适配
# TWRP 小米平板6 Pro（liuqin）
基于[红米K60橙狐设备树](https://github.com/ymdzq/OFRP-device_xiaomi_mondrian)修改的TWRP设备树  
参考了sk佬[小米12S twrp设备树](https://github.com/sekaiacg/TWRP_android_device_xiaomi_mayfly)
# 目前进度
liuqin基本功能可用，解密安卓15澎湃OS2.0的data分区正常，触摸控制正常，并且可以正常刷入HyperOS完整包  
# 如何使用
进入[Release](https://github.com/xccxxcys/device_xiaomi_liuqin-TWRP-OF/releases)中，下载 liuqin 对应的 recovery.img  
已root平板可以通过爱玩机工具箱、搞机助手等app直接写入recovery分区  
也可以平板连接电脑线刷，请自备[fastboot工具](https://developer.android.google.cn/studio/releases/platform-tools?hl=zh-cn)，手动重启平板至bootloader模式（橙色fastboot字样）  
使用fastboot工具把rec镜像刷入ab两槽的rec分区，重启进入rec，命令：  
```bash
fastboot flash recovery_a recovery.img
fastboot flash recovery_b recovery.img
fastboot reboot recovery
