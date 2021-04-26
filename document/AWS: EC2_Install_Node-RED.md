|[Back - Chapter 7](https://github.com/xuan103/MQTT/blob/main/document/AWS:%20EC2_MQTTlens_MQTT.md)|[Contents](https://github.com/xuan103/MQTT/blob/main/README.md)| [Next - Chapter 9](https://github.com/xuan103/MQTT/blob/main/document/AWS:%20EC2_Node-RED_MQTT.md)
---| ---| ---|

---

# Chapter 8: EC2: Install Node-RED

- 前置準備作業
    - 一台可上網的電腦
        - Ubuntu / macOS / Windows 皆可
- [AWS: EC2 Install Ubuntu](https://github.com/xuan103/MQTT/blob/main/document/AWS:%20EC2_Install_Ubuntu.md) 安裝完成
- [EC2: Install Mosquitto MQTT Broker](https://github.com/xuan103/MQTT/blob/main/document/AWS:%20EC2_Install_MQTT.md) 安裝完成

---
### Step 1. 登入到 AWS EC2

- AWS: EC2 登入
    - [EC2: For Ubuntu]((https://github.com/xuan103/MQTT/blob/main/document/AWS:%20EC2_For_Ubuntu_SSH.md))

### Step 2. 安裝 Node-RED

- 在終端機執行以下指令：安裝 `Node-RED`

>$ `curl -sL https://deb.nodesource.com/setup_8.x | sudo -E bash`

>$ sudo apt-get install -y nodejs build-essential

>$ sudo npm install -g --unsafe-perm node-red --allow-root

### Step 3. 啟動 Node-RED

- 在終端機執行以下指令：啟動 `Node-RED`

>$ node-red

![nr1_node_red_ok](https://github.com/xuan103/MQTT/blob/main/document/png/nr1_node_red_ok.png)

（以上畫面為 Node-RED 啟動成功。）

---

### Step 4. 查看 AWS EC2 IP 位置

![mq3-2_ipv4](https://github.com/xuan103/MQTT/blob/main/document/png/mq3-2_ipv4.png)

---

- 開啟 Chrome 瀏覽器
    - 在網址列輸入上一步驟的 IP ，最後在加上 `:1880`。
        - 例如：[IP]:1880

![nr2_web](https://github.com/xuan103/MQTT/blob/main/document/png/nr2_web.png)

---

|[Back - Chapter 7](https://github.com/xuan103/MQTT/blob/main/document/AWS:%20EC2_MQTTlens_MQTT.md)|[Contents](https://github.com/xuan103/MQTT/blob/main/README.md)| [Next - Chapter 9](https://github.com/xuan103/MQTT/blob/main/document/AWS:%20EC2_Node-RED_MQTT.md)
---| ---| ---|

