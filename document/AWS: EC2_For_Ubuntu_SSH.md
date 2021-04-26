|[Back - Chapter 4](https://github.com/xuan103/MQTT/blob/main/document/AWS:%20EC2_Install_Ubuntu.md)|[Contents](https://github.com/xuan103/MQTT/blob/main/README.md)| [Next - Chapter 6](https://github.com/xuan103/MQTT/blob/main/document/AWS:%20EC2_Install_MQTT.md)
---| ---| ---|

---

# Chapter 5-1: EC2: For Ubuntu SSH

- 前置準備作業
    - 一台已連上網路的 Ubuntu / macOS 電腦
    - 已設定完成 AWS EC2 環境

---

### Client 端：Ubuntu / macOS 

#### Step 1. 開啟終端機 `Ctrl + Alt + T`（範例為: ubuntu 20.04）

![us1_terminal](https://github.com/xuan103/MQTT/blob/main/document/png/us1_terminal.png)

---

#### Step 2. 切換路徑到 AWS EC2 憑證所在位置

- 指令為 cd 憑證所在目錄

![us2_cd](https://github.com/xuan103/MQTT/blob/main/document/png/us2_cd.png)

- 設定憑證權限
    - 指令為 chmod 400 憑證名稱

![us3_chmod](https://github.com/xuan103/MQTT/blob/main/document/png/us3_chmod.png)

---

#### Step 3. 取得 AWS EC2 登入資訊

- 登入到【 AWS 】，網址如下：https://aws.amazon.com/tw/

![ec1-aws](https://github.com/xuan103/MQTT/blob/main/document/png/ec1-aws.png)

>---

- 找到 "所有服務" ➙ 點選 "EC2"。

![ec2-1_ec2](https://github.com/xuan103/MQTT/blob/main/document/png/ec2-1_ec2.png)

>---

- 點選 " 執行個體 (Instances) "。

![us4_instances](https://github.com/xuan103/MQTT/blob/main/document/png/us4_instances.png)

>---

- 點選所啟用的執行個體 Instance ，再點選 " 連線 Connect "。

![us5_connect](https://github.com/xuan103/MQTT/blob/main/document/png/us5_connect.png)

---

- 複製紅色框框中的資訊到終端機中

![us6_ssh_cp](https://github.com/xuan103/MQTT/blob/main/document/png/us6_ssh_cp.png)

---
![us7_ssh_ok](https://github.com/xuan103/MQTT/blob/main/document/png/us7_ssh_ok.png)

---
|[Back - Chapter 4](https://github.com/xuan103/MQTT/blob/main/document/AWS:%20EC2_Install_Ubuntu.md)|[Contents](https://github.com/xuan103/MQTT/blob/main/README.md)| [Next - Chapter 6](https://github.com/xuan103/MQTT/blob/main/document/AWS:%20EC2_Install_MQTT.md)
---| ---| ---|




