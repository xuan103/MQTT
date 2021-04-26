|[Back - Chapter 6](https://github.com/xuan103/MQTT/blob/main/document/AWS:%20EC2_Install_MQTT.md)|[Contents](https://github.com/xuan103/MQTT/blob/main/README.md)| [Next - Chapter 8](https://github.com/xuan103/MQTT/blob/main/document/AWS:%20EC2_Install_Node-RED.md)
---| ---| ---|

# Chapter 7: EC2: MQTTlens on Mosquitto MQTT Broker

---
## 前置準備作業

- 一台可上網的電腦
    - Ubuntu / macOS / Windows 皆可
- 已安裝 Google Chrome 網路瀏覽器
- Mosquitto MQTT Broker - 安裝教學

---
### Step 1. 在 Chrome 安裝 MQTTlens

- 下載網址
    - [MQTTlens](https://chrome.google.com/webstore/detail/mqttlens/hemojaaeigabkbcookmlgmdigohjobjm?utm_source=chrome-ntp-launcher)

```
https://chrome.google.com/webstore/detail/mqttlens/hemojaaeigabkbcookmlgmdigohjobjm?utm_source=chrome-ntp-launcher
```

![chm1_add_tool](https://github.com/xuan103/MQTT/blob/main/document/png/chm1_add_tool.png)

---
### Step 2. 啟動 MQTTlens

- 點選 "MQTTlens"。

![chm2-1_mqttlen](https://github.com/xuan103/MQTT/blob/main/document/png/chm2-1_mqttlen.png)

---

- 若沒有跳轉置上頁畫面，可回到原下網址，點選 "Launch app"。

![chm2-2_launch_app](https://github.com/xuan103/MQTT/blob/main/document/png/chm2-2_launch_app.png)

---
- MQTTlens 開啟畫面

![chm2-3_open_mqttlen](https://github.com/xuan103/MQTT/blob/main/document/png/chm2-3_open_mqttlen.png)

---
### Step 3. 設定 MQTTlens

- 點選 "Connections" 旁的 " + "。

![chm3-1_connections](https://github.com/xuan103/MQTT/blob/main/document/png/chm3-1_connections.png)

---

- 輸入 " Connection name " 、 " Hostname " ，再點選 " CREATE CONNECTION " 。
    - Hostname 請輸入之前所建立的 AWS EC2 之 IP。

![chm3-2_connections_add](https://github.com/xuan103/MQTT/blob/main/document/png/chm3-2_connections_add.png)

---

![chm3-3-1_connections_new](https://github.com/xuan103/MQTT/blob/main/document/png/chm3-3-1_connections_new.png)

---

![chm3-3-2_connections_new](https://github.com/xuan103/MQTT/blob/main/document/png/chm3-3-2_connections_new)

---

![chm3-4_connections_ok](https://github.com/xuan103/MQTT/blob/main/document/png/chm3-4_connections_ok.png)

---

![chm3-5_subscriber](https://github.com/xuan103/MQTT/blob/main/document/png/chm3-5_subscriber.png)

---

![chm3-6_publisher](https://github.com/xuan103/MQTT/blob/main/document/png/chm3-6_publisher.png)

---
|[Back - Chapter 6](https://github.com/xuan103/MQTT/blob/main/document/AWS:%20EC2_Install_MQTT.md)|[Contents](https://github.com/xuan103/MQTT/blob/main/README.md)| [Next - Chapter 8](https://github.com/xuan103/MQTT/blob/main/document/AWS:%20EC2_Install_Node-RED.md)
---| ---| ---|