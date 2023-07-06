需要进入pod后执行命令。

# 下载并启动

```shell
curl -O https://arthas.aliyun.com/arthas-boot.jar

java -jar arthas-boot.jar
```

# trace

```shell
trace com.hillstone.cloud.ngcv.security.service.device.image.DeviceImageUpgradeService getDeviceImageUpgradeTasks
```

# watch


```shell
watch com.hillstone.cloud.ngcv.security.service.device.image.DeviceImageUpgradeService getDeviceImageUpgradeTasks -f -x 6 '{returnObj}' 
```