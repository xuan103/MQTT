[Contents](https://github.com/xuan103/MQTT/blob/main/README.md)| [Next - Chapter 2](https://github.com/xuan103/MQTT/blob/main/document/mqtt_aws_iot_core.md)
---| ---| 

---
# Chapter 1: MQTT 簡介

- MQTT(Message Queuing Telemetry Transport) 訊息序列遙測傳輸。
    - 1999年 IBM 發明。
    - 伺服器與用戶端間的發布與訂閱的訊息傳輸協定 (publish / subscribe )
    - MQTT 正式變成開放的 OASIS 國際標準。
    - 適用於 M2M 和 IoT 環境。

---

## 特點

- MQTT 好處在於它是一種輕量級協議（為了物聯網而設計的協定）。
    - 網路頻寬很低。
    - 硬體資源低。
    - 適合用在低功耗和網絡帶寬有限的 IoT 環境，像是：
    - 智慧家電，醫療裝置等等。 
 
--- 
 
## 訊息傳遞原理

- 使用發佈 (Publish) / 訂閱 (Subscribe) 的機制傳訊。
- 4個主要的元素:
    - 發佈者 (Publisher)。
    - 訂閱者 (Subscriber)。
    - 主題 (Topic)。
    - 轉訊站 (Broker)。

![m1](https://github.com/xuan103/MQTT/blob/main/document/png/m1.png)

> 發佈者 (Publisher)發佈一個主題，傳送給轉訊站 (Broker)，
由轉訊站 (Broker) 轉發給訂閱者 (Subscriber)。

>---

![m2](https://github.com/xuan103/MQTT/blob/main/document/png/m2.png)

---

### MQTT 訊息格式、封包格式

- 訊息格式有三類:
    - Fix Header (固定格式封包)。
    - Variable Header (變動格式封包)。
    - Payload (訊息內文)。
    
![m3_bit](https://github.com/xuan103/MQTT/blob/main/document/png/m3_bit.png)

>DUP flag：標記此訊息為重複 (duplicate) 的訊息，會用在 PUBLISH、PUBREL、SUBSCRIBE、UNSUBSCRIBE 上。 ]

---

### QoS 級別

MQTT 定義了三個層級的品質設定。

- QoS 代表：
    - Publisher 與 Broker。
    - Broker 與 Subscriber 之間傳輸品質。

>---
>
- QoS 0 最多傳送一次（at most once）
    - Publisher 傳訊給 Broker 後直接轉傳給 Subscriber，不會回傳確認封包。
    - QoS 0 就像寄平信，不保證訊息會送達。

![m4_QoS0](https://github.com/xuan103/MQTT/blob/main/document/png/m4_QoS0.png)

>---

- QoS 1 至少傳送一次（at least once）
    - Publisher 傳訊給 Broker 後，Broker 會回應 PUBACK 訊息給
    - Publisher，確認收到訊息。
    - Publisher 沒有收到 PUBACK 回應，就會再次發送 Publish。
- 缺點:
    - Publisher 沒有收到 PUBACK 回應，就會認定訊息沒送到，重傳訊息。
    - 讓訂閱者重複收到相同訊息。
    - 保證訊息會送達，但可能會重複。

![m5_QoS1](https://github.com/xuan103/MQTT/blob/main/document/png/m5_QoS1.png)

>---

- QoS 2 確實傳送一次（exactly once）
    - Publisher 傳訊給 Broker 後，Broker 會回應 PUBREC 訊息給 Publisher，確認收到要發布的訊息。
    - Publisher 收到 PUBREC 回應時，傳送 PUBREL（釋放發布訊息）。
    - Broker 收到 PUBREL，將訊息發布給 Subscriber，並向 Publisher 回報PUBCOMP。

![m6_QoS2](https://github.com/xuan103/MQTT/blob/main/document/png/m6_QoS2.png)

>---

## QoS 總結

- QoS 0
    - 優點 - 佔用頻寬與傳送時間較少
    - 缺點 - 資料可能會遺失

- QoS 1
    - 優點 - 佔用頻寬與傳送時間較少較 Qos 2 少
    - 缺點 - Subscriber可能會收到重複的訊息

- QoS 2
    - 優點 - 不會重覆傳送相同訊息
    - 缺點 - 佔用頻寬與傳送時間較多

---
[Contents](https://github.com/xuan103/MQTT/blob/main/README.md)| [Next - Chapter 2](https://github.com/xuan103/MQTT/blob/main/document/mqtt_aws_iot_core.md)
---| ---| 

