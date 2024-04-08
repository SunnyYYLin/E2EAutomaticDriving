# E2EAutomaticDriving
The first competition for me, by CVPR.

## Transfuser
### 问题1
按照 [[https://github.com/autonomousvision/transfuser]] 的步骤，第三步：
```shell
UserName@Ubuntu-22.04:~/transfuser$ ./setup_carla.sh
mkdir: cannot create directory ‘carla’: File exists
--2024-04-08 20:36:20--  https://carla-releases.s3.eu-west-3.amazonaws.com/Linux/CARLA_0.9.10.1.tar.gz
Connecting to 127.0.0.1:7890... connected.
Proxy request sent, awaiting response... 404 Not Found
2024-04-08 20:36:22 ERROR 404: Not Found.
--2024-04-08 20:36:22--  https://carla-releases.s3.eu-west-3.amazonaws.com/Linux/AdditionalMaps_0.9.10.1.tar.gz
Connecting to 127.0.0.1:7890... connected.
Proxy request sent, awaiting response... 404 Not Found
2024-04-08 20:36:23 ERROR 404: Not Found.
```
查看setup_carla.sh中：
```shell
wget https://carla-releases.s3.eu-west-3.amazonaws.com/Linux/CARLA_0.9.10.1.tar.gz
wget https://carla-releases.s3.eu-west-3.amazonaws.com/Linux/AdditionalMaps_0.9.10.1.tar.gz
```
链接（欧洲西区3）似乎失效了。
到carla项目地址:[[https://github.com/carla-simulator/carla/releases]] 找到相同的0.9.10.1版本，替换链接为：
```shell
wget https://carla-releases.s3.us-east-005.backblazeb2.com/Linux/CARLA_0.9.10.1.tar.gz
wget https://carla-releases.s3.us-east-005.backblazeb2.com/Linux/AdditionalMaps_0.9.10.1.tar.gz
```
即可正常运行脚本。
