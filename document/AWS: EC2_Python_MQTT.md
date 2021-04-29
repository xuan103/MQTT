|[Back - Chapter 10](https://github.com/xuan103/MQTT/blob/main/document/AWS:%20EC2_Node-RED_MQTT.md)|[Contents](https://github.com/xuan103/MQTT/blob/main/README.md)| 
---| ---|

---

# Chapter 11: EC2: Python & MQTT

- 一台已連上網路的電腦
    - Ubuntu / macOS / Windows 皆可
- [Mosquitto MQTT Broker](https://github.com/xuan103/MQTT/blob/main/document/AWS:%20EC2_Install_MQTT.md) 安裝完成
- [Node-RED](https://github.com/xuan103/MQTT/blob/main/document/AWS:%20EC2_Install_Node-RED.md) 安裝完成

- 設定完成 [Node-RED 串接 Mosquitto MQTT Broker](https://github.com/xuan103/MQTT/blob/main/document/AWS:%20EC2_Node-RED_MQTT.md)

- 設定完成 [Node-RED 設定 Dashboard](https://github.com/xuan103/MQTT/blob/main/document/AWS:%20EC2_Node-RED_Dashboard.md)

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
## Step 4. 撰寫 Python3 串接程式

- 程式中的 MQTT_SERVER，請自行更改為 Mosquitto MQTT Broker 所在位置。
    - AWS EC2 Ubuntu Server 所在的 IP 位置。
- 將下方程式存檔為 " 檔名.py "（Python3 程式的副檔名為 " py " ）。
    - 檔名的部份請自行命名，範例命名為 " mqtt.py "。
```python=
import paho.mqtt.client as mqtt 
import time
import json
import random

# *********************************************************************
# MQTT Config

dataChnId1 = "Temperature"
MQTT_SERVER = "54.191.103.222"
MQTT_PORT = 1883
MQTT_ALIVE = 60
MQTT_TOPIC1 = "Try/" + dataChnId1 + "/MQTT"
# Try/22/MQTT

# *********************************************************************

mqtt_client = mqtt.Client()
mqtt_client.connect(MQTT_SERVER, MQTT_PORT, MQTT_ALIVE)    

while True:  
  t0 = random.randint(0,30)
  payload = {"dataChnId":dataChnId1,"value":t0}
  print(dataChnId1 + " : " + str(t0))
  mqtt_client.publish(MQTT_TOPIC1, json.dumps(payload), qos=1)
  time.sleep(10)
```

---
## Step 5. 安裝 Python3 的 paho-mqtt 套件

- 在 TERMINAL 處輸入下方指令進行安裝套件。

>$ pip3 install paho-mqtt

代表使用 Python3 的套件管理工作 pip3 來安裝 paho-mqtt 套件。

---
## tep 6. 執行 Python3 Code

- 在 TERMINAL 處輸入下方指令執行程式
    - `python3 檔名.py`

代表使用 python3 編譯器來執行 `檔名.py` 的程式

- 範例程式命名為 mqtt.py，故此處執行方式為 `python3 mqtt.py`
>$ `python3 mqtt.py`

---
## Step 7. TERMINAL 執行畫面

![nrp1_TERMINAL](https://github.com/xuan103/MQTT/blob/main/document/png/nrp1_TERMINAL.png)

---
## Step 8. 開啟 Node-RED 編輯頁面

![nrp2-1_dashboard](https://github.com/xuan103/MQTT/blob/main/document/png/nrp2-1_dashboard.png)

---

![nrp2-2_dashboard_open](https://github.com/xuan103/MQTT/blob/main/document/png/nrp2-2_dashboard_open.png)

---

![nrp2-3_dashboard_ok](https://github.com/xuan103/MQTT/blob/main/document/png/nrp2-3_dashboard_ok.png)

---
|[Back - Chapter 10](https://github.com/xuan103/MQTT/blob/main/document/AWS:%20EC2_Node-RED_MQTT.md)|[Contents](https://github.com/xuan103/MQTT/blob/main/README.md)| 
---| ---|


