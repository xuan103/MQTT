# MQTT: AWS IoT Core

>AWS IoT 支援的 MQTT 以 MQTT v3.1.1 規格為基礎，但有一些差異。如需有關 AWS IoT 與 MQTT v3.1.1 規格差異的資訊，請參閱 [AWS IoT 與 MQTT 3.1.1 版規格](https://docs.aws.amazon.com/zh_tw/iot/latest/developerguide/mqtt.html) 的差異或下方表格（部份顯示）。

---

## MQTT 服務品質 (QoS) 選項

AWS IoT 和 AWS IoT 裝置軟體開發套件支援 MQTT 服務品質 (QoS) 層級 0 和 1。MQTT 通訊協定定義 QoS 的第三個層級，層級 2，但 AWS IoT 不支援。只有 MQTT 通訊協定支援 QoS 功能。HTTPS 不支援 QoS。

此表格說明各個 QoS 層級如何影響訊息發佈至中介裝置的方式，以及訊息中介裝置發佈訊息的方式。

![a1_QoS](https://github.com/xuan103/MQTT/blob/main/document/png/a1_Q0S.png)

>---

部分與規格差異：（部份顯示，詳細參考 AWS 官網。）

- 請求 QoS 2 時，訊息中介裝置不會傳送 PUBACK 或 SUBACK。
- 在 AWS IoT 中，訂閱 QoS 層級 0 的主題表示訊息會發送零次或多次。
- 一則訊息可能會傳送超過一次。
- 傳送超過一次的訊息在發送時可能會使用不同的封包 ID。
- 在這些情況下，DUP 旗標就不會設置。
- MQTT 規範提供了一項規定，讓發佈者可以請求中介裝置保留發送至主題的最新訊息，並將此訊息傳送給未來所有的主題訂閱者。
- AWS IoT 不支援保留的訊息。如果請求保留訊息，連線就會中斷。
