|[Back - Chapter 9](https://github.com/xuan103/MQTT/blob/main/document/AWS:%20EC2_Node-RED_MQTT.md)|[Contents](https://github.com/xuan103/MQTT/blob/main/README.md)| [Next - Chapter 11](https://github.com/xuan103/MQTT/blob/main/document/AWS:%20EC2_Python_MQTT.md)
---| ---| ---|

---

# 10_AWS: EC2_Node-RED_Dashboard

## 前置準備作業


- 一台已連上網路的電腦
    - Ubuntu / macOS / Windows 皆可
- [Mosquitto MQTT Broker](https://github.com/xuan103/MQTT/blob/main/document/AWS:%20EC2_Install_MQTT.md) 安裝完成
- [Node-RED](https://github.com/xuan103/MQTT/blob/main/document/AWS:%20EC2_Install_Node-RED.md) 安裝完成

- 設定完成 [Node-RED 串接 Mosquitto MQTT Broker](https://github.com/xuan103/MQTT/blob/main/document/AWS:%20EC2_Node-RED_MQTT.md)

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
## Step 4. 新增 node-red-dashboard 節點

![nrd1-1_add_new](https://github.com/xuan103/MQTT/blob/main/document/png/nrd1-1_add_new.png)

---

![nrd1-2_add_install](https://github.com/xuan103/MQTT/blob/main/document/png/nrd1-2_add_install.png)

>---

![nrd1-3_add_install_dashboard](https://github.com/xuan103/MQTT/blob/main/document/png/nrd1-3_add_install_dashboard.png)

>---

![nrd1-4_add_install_dashboard_y](https://github.com/xuan103/MQTT/blob/main/document/png/nrd1-4_add_install_dashboard_y.png)

>---

![nrd1-5_add_install_dashboard_ok](https://github.com/xuan103/MQTT/blob/main/document/png/nrd1-5_add_install_dashboard_ok.png)

---
## Step 5. 建立 Node-RED 處理程式 

![nrd2-1_add_function](https://github.com/xuan103/MQTT/blob/main/document/png/nrd2-1_add_function.png)

>---

![nrd2-2_add_function_line](https://github.com/xuan103/MQTT/blob/main/document/png/nrd2-2_add_function_line.png)

>--

![nrd2-3_add_function_done](https://github.com/xuan103/MQTT/blob/main/document/png/nrd2-3_add_function_done.png)

---

## Step 6. 建立 Node-RED 串接 Dashboard 程式

![nrd3-1_add_gauge](https://github.com/xuan103/MQTT/blob/main/document/png/nrd2-1_add_gauge.png)

>---

![nrd3-1_add_gauge_line](https://github.com/xuan103/MQTT/blob/main/document/png/nrd3-1_add_gauge_line.png)

>---

![nrd3-2_add_gauge_tab](https://github.com/xuan103/MQTT/blob/main/document/png/nrd3-2_add_gauge_tab.png)

>---

![nrd3-3_add_gauge_tab_group](https://github.com/xuan103/MQTT/blob/main/document/png/nrd3-3_add_gauge_tab_group.png)

>---

![nrd3-4_add_gauge_tab_group_update](https://github.com/xuan103/MQTT/blob/main/document/png/nrd3-4_add_gauge_tab_group_update.png)

>---

![nrd3-5_add_gauge_tab_group_edit](https://github.com/xuan103/MQTT/blob/main/document/png/nrd3-5_add_gauge_tab_group_edit.png)

>---

![nrd3-6_add_chart](https://github.com/xuan103/MQTT/blob/main/document/png/nrd3-6_add_chart.png)

>---

![nrd3-7_add_chart_line](https://github.com/xuan103/MQTT/blob/main/document/png/nrd3-7_add_chart_line.png)

>---

![nrd3-8_add_chart_edit](https://github.com/xuan103/MQTT/blob/main/document/png/nrd3-8_add_chart_edit.png)

>---

![nrd3-9_deploy](https://github.com/xuan103/MQTT/blob/main/document/png/nrd3-9_deploy.png)

>---

![nrd3-a_deploy_ok](https://github.com/xuan103/MQTT/blob/main/document/png/nrd3-a_deploy_ok.png)

---
|[Back - Chapter 9](https://github.com/xuan103/MQTT/blob/main/document/AWS:%20EC2_Node-RED_MQTT.md)|[Contents](https://github.com/xuan103/MQTT/blob/main/README.md)| [Next - Chapter 11](https://github.com/xuan103/MQTT/blob/main/document/AWS:%20EC2_Python_MQTT.md)
---| ---| ---|





