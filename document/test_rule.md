|[Back - Chapter 2](https://github.com/xuan103/MQTT/blob/main/document/mqtt_aws_iot_core.md)|[Contents](https://github.com/xuan103/MQTT/blob/main/README.md)| [Next - Chapter 4](https://github.com/xuan103/MQTT/blob/main/document/AWS:%20EC2_Install_Ubuntu.md)
---| ---| ---|

---

# Chapter 3-2: Test Rule

## 使用 MQTT 使用者端測試您的規則

1. 在 主控台的 AWS IoT MQTT 中，訂用輸入主題，在本例中是 `device/+/data`。

    a. 在 MQTT client（MQTT 使用者）的 Subscriptions（方案）下，
       選擇 Subscribe to a topic.

    b. 在 Subscription topic（預設主題）中，
       輸入輸入主題篩選條件 `device/+/data`。

    c. 將其他欄位保留為其預設設定。

    d. 選擇 Subscribe to topic.
       在 Subscriptions （方案） 欄中，
       在 Publish to a `topicdevice/+/data` ，出現 。

![tr1_test_rule_data](https://github.com/xuan103/MQTT/blob/main/document/png/tr1_test_rule_data.png)

---

2. 向您的規則將發行的 主題描述 `device/data/temp`：。

    a. 在 Subscriptions（方案 下，選擇 Subscribe to a topic 」，
       並在 Subscription topic （方案主題） 中，
       輸入已重新發布訊息的 主題 `device/data/temp`。

    b. 將其他欄位保留為其預設設定。

    c. 選擇 Subscribe to topic.
       在 Subscriptions （方案） 欄中，
       在 `device/+/datadevice/data/temp`，出現 。

![tr2_test_rule_temp](https://github.com/xuan103/MQTT/blob/main/document/png/tr2_test_rule_temp.png)

---

3. 發行訊息至具有特定 裝置 ID 的輸入主題 device/22/data。 
   您無法發布到包含萬用字元的 MQTT 主題。

    a. 在 MQTT client（MQTT 使用者）的 Subscriptions（方案）下，
       選擇 Publish to topic.

    b. 在 Publish 欄位中，輸入主題名稱 `device/22/data`。 

    c. 複製此處顯示的範例資料，
       並在主題名稱下方的編輯方塊中貼上範例資料。

    d. 若要傳送 MQTT 訊息，請選擇 Publish to topic.
    
```
{
  "temperature": 28,
  "humidity": 80,
  "barometer": 1013,
  "wind": {
    "velocity": 22,
    "bearing": 255
  }
}
```

![tr3-1_test_rule_22](https://github.com/xuan103/MQTT/blob/main/document/png/tr3-1_test_rule_22.png)

>---

![tr3-2_test_rule_22_push](https://github.com/xuan103/MQTT/blob/main/document/png/tr3-2_test_rule_22_push.png)

---

4. 檢查傳送的訊息。

    a. 在 MQTT client （MQTT 使用者）的 Subscriptions（方案）下，
       會在您稍早訂購的兩個主題旁邊有一個 gining 點。

    b. green points（等色點）表示自上次查看後已接收到一則或多則新訊息。

    c. 在 Subscriptions （方案） 下，
       選擇 `device/+/data` 來檢查訊息承載是否符合您剛發布的項目，
       看起來像這樣：

```
{
  "temperature": 28,
  "humidity": 80,
  "barometer": 1013,
  "wind": {
    "velocity": 22,
    "bearing": 255
  }
}
```

![tr4-1_test_rule_ck](https://github.com/xuan103/MQTT/blob/main/document/png/tr4-1_test_rule_ck.png)

在 Subscriptions （方案） 下，選擇 `device/data/temp`，以檢查重新發布的訊息承載是否如下所示：

```
{
  "device_id": "22",
  "temperature": 28
}
```

![tr4-2_test_rule_ck_22](https://github.com/xuan103/MQTT/blob/main/document/png/tr4-2_test_rule_ck_22.png)

請注意，device_id 值是引號字串，而 temperature 值是數字。這是因為 topic() 函數從輸入訊息的主題名稱擷取字串，而 temperature 值則使用輸入訊息承載的數值。

如果您想要將 device_id 值設為數值，將規則查詢陳述式 topic(2) 中的 取代為：

```
cast(topic(2) AS DECIMAL)
```

請注意，將 topic(2) 值轉換為數值只有在主題的該部分只包含數字字元時才會運作。

---

5. 如果您看到正確的訊息已發布至 `device/data/temp` 主題，則您的規則有效。在下一節中，了解 Republish 規則動作的更多資訊。

如果您未看到正確的訊息已發布至 `device/+/` 資料或 `device/data/temp` 主題，請檢查疑難排解秘訣。

---

小小補充：

![tr99](https://github.com/xuan103/MQTT/blob/main/document/png/tr99.png)

---
|[Back - Chapter 2](https://github.com/xuan103/MQTT/blob/main/document/mqtt_aws_iot_core.md)|[Contents](https://github.com/xuan103/MQTT/blob/main/README.md)| [Next - Chapter 4](https://github.com/xuan103/MQTT/blob/main/document/AWS:%20EC2_Install_Ubuntu.md)
---| ---| ---|
