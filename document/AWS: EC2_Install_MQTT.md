|[Back - Chapter 5](https://github.com/xuan103/MQTT/blob/main/document/AWS:%20EC2_For_Ubuntu_SSH.md)|[Contents](https://github.com/xuan103/MQTT/blob/main/README.md)| [Next - Chapter 7](https://github.com/xuan103/MQTT/blob/main/document/AWS:%20EC2_MQTTlens_MQTT.md)
---| ---| ---|

# Chapter 6: EC2: Install Mosquitto MQTT Broker

---

### 前置準備作業

- [AWS: EC2 Install Ubuntu](https://github.com/xuan103/MQTT/blob/main/document/AWS:%20EC2_Install_Ubuntu.md)

---

### AWS EC2 Ubuntu Server 端

#### Step 1. 登入到 AWS EC2

-   AWS: EC2 登入
    -    [EC2: For Ubuntu](https://github.com/xuan103/MQTT/blob/main/document/AWS:%20EC2_For_Ubuntu_SSH.md)

---

#### Step 2. 安裝 Mosquitto MQTT Broker

- 取得遠端更新伺服器的套件檔案清單

>$ sudo apt update

![mq1_system_update](https://github.com/xuan103/MQTT/blob/main/document/png/mq1_system_update.png)

>---

安裝 Mosquitto MQTT Broker

>$ sudo apt install -y mosquitto mosquitto-clients

![mq2_install_mosquitto](https://github.com/xuan103/MQTT/blob/main/document/png/mq2_install_mosquitto.png)

---

Step 3. 測試 Mosquitto MQTT Broker

- 前置準備作業:
    - Publish、Subscribe 測試
    - 查看 [AWS](https://aws.amazon.com/tw/) EC2 IP 位置

- 開啟兩個終端機
    - 一台為 Subscribe
    - 一台為 Publish

>---

![mq3-1_show](https://github.com/xuan103/MQTT/blob/main/document/png/mq3-1_show.png)

>---

查看 [AWS](https://aws.amazon.com/tw/) EC2 IP 位置
IP 位於 " IPv4 Public IP "

![mq3-2_ipv4](https://github.com/xuan103/MQTT/blob/main/document/png/mq3-2_ipv4.png)

>---

#### 建立 Subscriber

 - **終端機 1**
    - 訂閱 Try/MQTT 的主題 (主題名稱不包含空白)
    - mosquitto_sub -h [IP] -t [Topic]
    - IP 請更改為之前所建立的 AWS EC2 之 IP
       
>$ mosquitto_sub -d -t Try/MQTT

>> 要 Publisher 有發消息才有訊息顯示。

OR

>$ mosquitto_sub -h 54.191.103.222 -t Try/MQTT

>>會看到 Topic、Qos等...資訊
`-h : mqtt host to connect to. Defaults to localhost.`

>---

- 建立 Publisher

 - **終端機 2**
    - 訂閱 Try/MQTT 的主題 (主題名稱不包含空白)
    - mosquitto_pub -h [IP] -t [Topic] -m [Message]
    - IP 請更改為之前所建立的 AWS EC2 之 IP

>$ mosquitto_pub -d -t Try/MQTT -m "Try Message"

OR

>$ mosquitto_pub -d -h 54.191.103.222 -t Try/MQTT -m "Try Message"

>---
### 補充

- 功能:
    - mosquitto_sub : 訂閱
    - mosquitto_pub : 發布
    - `-d` : debug 模式 => debug
    - `-t` : 訂閱的主題 => topic
    - `-h` : Broker 的 IP => host
    - `-m` : 發送的內容 => message
    - `-v` : 顯示主題名稱 => verbosely
- 更多指令內容可以查看:
    - mosquitto_sub --help
    - mosquitto_pub --help

---

|[Back - Chapter 5](https://github.com/xuan103/MQTT/blob/main/document/AWS:%20EC2_For_Ubuntu_SSH.md)|[Contents](https://github.com/xuan103/MQTT/blob/main/README.md)| [Next - Chapter 7](https://github.com/xuan103/MQTT/blob/main/document/AWS:%20EC2_MQTTlens_MQTT.md)
---| ---| ---|
