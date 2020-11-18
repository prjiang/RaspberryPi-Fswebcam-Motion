# RaspberryPi-Fswebcam-Motion

## fswebcam
安裝fswebcam，只能拍照存檔成jpeg檔
```
sudo apt-get install fswebcam
```
拍照儲存為 test.jpg
```
fswebcam test.jpg
```

<br>

## motion

檢查是否驅動
```
sudo lsusb
```

安裝motion前，先更新系統套件資訊
```
sudo apt-get update
```

安裝motion 可拍攝影片，作為監視器使用
```
sudo apt-get install motion
```

開機自動啟動
```
sudo nano /etc/default/motion
```
* start_motion_daemon=yes

修改設定檔
```
sudo nano /etc/motion/motion.conf
```
* daemon on
* stream_localhost off
* webcontrol_localhost off

啟動
```
sudo service motion start
``` 

連線
```
http://IP:8081
```
