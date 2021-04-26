|[Back - Chapter 3-2](https://github.com/xuan103/MQTT/blob/main/document/test_rule.md)|[Contents](https://github.com/xuan103/MQTT/blob/main/README.md)| [Next - Chapter 5](https://github.com/xuan103/MQTT/blob/main/document/AWS:%20EC2_For_Ubuntu_SSH.md)
---| ---| ---|

---

# Chapter 4: AWS: EC2 Install Ubuntu

## 前置準備作業

- 有 AWS 帳號
- 一台有網路電腦 
    - Ubuntu 
    - Mac 
    - Windows

---

## 使用工具的 Port

- Mosquitto
    - 1883 Port
- Node-RED
    - 1880 Port
- InfluxDB
    - 8086 Port
- Grafana
    - 3000 Port

![ec99](https://github.com/xuan103/MQTT/blob/main/document/png/ec99.png)

---

### Step 1. 登入到 AWS
- 登入網址：https://aws.amazon.com/tw/

![ec1-aws](https://github.com/xuan103/MQTT/blob/main/document/png/ec1-aws.png)

---

### Step 2. 啟用與設定 EC2
- 找到 "所有服務" ➙ 點選 "EC2"。

![ec2-1_ec2](https://github.com/xuan103/MQTT/blob/main/document/png/ec2-1_ec2.png)

>---

- 點選 " 啟動執行個體（Launch Instance）"。

![ec2-2_launch_instance](https://github.com/xuan103/MQTT/blob/main/document/png/ec2-2_launch_instance.png)

>---

- 點選 "Ubuntu Server 18.04 LTS (HVM), SSD Volume Type " 旁邊的 " Select "。

![ec2-3_ubuntu](https://github.com/xuan103/MQTT/blob/main/document/png/ec2-3_ubuntu.png)

>---

- 點選 " t2.micro " 的 Instance Type

![ec2-4_t2.micro](https://github.com/xuan103/MQTT/blob/main/document/png/ec2-4_t2.micro.png)

>---

- 來到 " strp 6.Configure Security Group "
    - 在 " Type " 欄位中選擇 " Custom TCP " 
    - 在 " Port Range " 欄位中輸入 " 1883 "
    - 在 " Source " 欄位中輸入 " 0.0.0.0/0 "

重複以上動作，將所需 port 添加完畢，點選 " Review and Lanuch " 按鈕。

![ec2-5-1_add_rule](https://github.com/xuan103/MQTT/blob/main/document/png/ec2-5-1_add_rule.png)

>---

![ec2-5-2_add_rule_port](https://github.com/xuan103/MQTT/blob/main/document/png/ec2-5-2_add_rule_port.png)

>---

- 來到 " strp 7.Review Instance Lanuch " ，
  點選 " Lanuch " 按鈕。

![ec2-6-1_lanuch](https://github.com/xuan103/MQTT/blob/main/document/png/ec2-6-1_lanuch.png)

>---

![ec2-6-2_key](https://github.com/xuan103/MQTT/blob/main/document/png/ec2-6-2_key.png)

>---

![ec2-6-3_ok](https://github.com/xuan103/MQTT/blob/main/document/png/ec2-6-3_ok.png)

---

3. 建立完成畫面

![ec3_ck](https://github.com/xuan103/MQTT/blob/main/document/png/ec3_ck.png)

---
|[Back - Chapter 3-2](https://github.com/xuan103/MQTT/blob/main/document/test_rule.md)|[Contents](https://github.com/xuan103/MQTT/blob/main/README.md)| [Next - Chapter 5](https://github.com/xuan103/MQTT/blob/main/document/AWS:%20EC2_For_Ubuntu_SSH.md)
---| ---| ---|




