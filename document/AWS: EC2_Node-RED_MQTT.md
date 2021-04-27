|[Back - Chapter 8](https://github.com/xuan103/MQTT/blob/main/document/AWS:%20EC2_Install_Node-RED.md)|[Contents](https://github.com/xuan103/MQTT/blob/main/README.md)| [Next - Chapter ](https://github.com/xuan103/MQTT/blob/main/document/AWS:%20EC2_Node-RED_Dashboard.md)
---| ---| ---|

---

# Chapter 9: EC2: Node-RED & Mosquitto MQTT Broker

## 前置準備作業

- 一台已連上網路的電腦
    - Ubuntu / macOS / Windows 皆可
- [Mosquitto MQTT Broker](https://github.com/xuan103/MQTT/blob/main/document/AWS:%20EC2_Install_MQTT.md) 安裝完成
- [Node-RED](https://github.com/xuan103/MQTT/blob/main/document/AWS:%20EC2_Install_Node-RED.md) 安裝完成

---
## Step 1. 啟動 Node-RED

- 在終端機執行以下指令：啟動 Node-RED

>$ node-red

![nr1_node_red_ok](https://github.com/xuan103/MQTT/blob/main/document/png/nr1_node_red_ok.png)

（以上畫面為 Node-RED 啟動成功。）

---

## Step 2. 查看 AWS EC2 IP 位置

![mq3-2_ipv4](https://github.com/xuan103/MQTT/blob/main/document/png/mq3-2_ipv4.png)

---

## Step 3. 開啟 Node-RED 編輯頁面

- 開啟 Chrome 瀏覽器
    - 在網址列輸入上一步驟的 IP ，最後在加上 :1880。
        - 例如：[IP]:1880

![nr2_web](https://github.com/xuan103/MQTT/blob/main/document/png/nr2_web.png)

---

## Step 4. 建立 Node-RED 串接 Mosquitto MQTT Broker 程式

![nrm1_mqtt_in](https://github.com/xuan103/MQTT/blob/main/document/png/nrm1_mqtt_in.png)

---

![nrm2-1_mqtt_set](https://github.com/xuan103/MQTT/blob/main/document/png/nrm2-1_mqtt_set.png)

>---

![nrm2-2_mqtt_set_ip](https://github.com/xuan103/MQTT/blob/main/document/png/nrm2-2_mqtt_set_ip.png)

>---

![nrm2-3_mqtt_set_ok](https://github.com/xuan103/MQTT/blob/main/document/png/nrm2-3_mqtt_set_ok.png)

>---

![nrm3_mqtt_debug](https://github.com/xuan103/MQTT/blob/main/document/png/nrm3_mqtt_debug.png)

---

![nrm4-1_line](https://github.com/xuan103/MQTT/blob/main/document/png/nrm4-1_line.png)

>---

![nrm4-2_line_ok](https://github.com/xuan103/MQTT/blob/main/document/png/nrm4-2_line_ok.png)

>---

![nrm5_bug](https://github.com/xuan103/MQTT/blob/main/document/png/nrm5_bug.png)

---

![nrm6_node-red_mqttlen_ok](https://github.com/xuan103/MQTT/blob/main/document/png/nrm6_node-red_mqttlen_ok.png)

---
|[Back - Chapter 8](https://github.com/xuan103/MQTT/blob/main/document/AWS:%20EC2_Install_Node-RED.md)|[Contents](https://github.com/xuan103/MQTT/blob/main/README.md)| [Next - Chapter ](https://github.com/xuan103/MQTT/blob/main/document/AWS:%20EC2_Node-RED_Dashboard.md)
---| ---| ---|
