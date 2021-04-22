# Create Rrules

1. 開放 [主控台的 AWS IoTRules hub](https://us-west-2.console.aws.amazon.com/iot/home?region=us-west-2#/rulehub) （規則中樞）。

---

2. 在 Rules （規則） 中，選擇 Create 並開始建立新規則。

![mp1_rules_create](https://github.com/xuan103/MQTT/blob/main/document/png/mp1_rules_create.png)

---

3. 在 Create a rule （建立規則） 的頂端部分：

    a. 在 Name （名稱） 中，輸入規則的名稱。
    b. 在 Description （描述） 中描述規則。

* 請記住，規則名稱在您的帳號和區域中必須是唯一的，並且不能有任何空格。我們在此名稱中使用基礎核心字元來分隔規則名稱中的兩個字。

![mp2_rule_reate_name](https://github.com/xuan103/MQTT/blob/main/document/png/mp2_rule_reate_name.png)

---

4. 在 Create a rule （建立規則） 的規則陳述式中：

    a. 在 Using SQL version（使用 SQL 版本） 中，選取 2016-03-23。
    b. 在 Rule query statement （規則查詢陳述式）編輯方塊中，輸入 陳述式：

> SELECT topic(2) as device_id, temperature FROM 'device/+/data'

![mp3_rule_create_version](https://github.com/xuan103/MQTT/blob/main/document/png/mp3_rule_create_version.png)

此陳述式：
- 使用符合device/+/data主題篩選條件的主題，接聽 MQTT 訊息。
- 從主題字串中選取第二個元素，並將其指派給 device_id 欄位。
- 從訊息承載選取值temperature欄位，並將其指派給 temperature 欄位。

---

5. 在 Set one or more actions （設定一或多個動作） 中：

    a. 若要開放此規則的規則動作清單，請選擇 Add action.

    b. 在 Select an action （選取動作） 中，選擇 Republish a message to an AWS IoT topic (重新發布訊息至 AWS 主題)。

    c. 在動作清單的底部，選擇 Configure action 打開所選動作的組態頁面。

![mp4-1_set_actions](https://github.com/xuan103/MQTT/blob/main/document/png/mp4-1_set_actions.png)

---

6. 在 Configure action （設定動作） 中：

![mp4-2_configure_action](https://github.com/xuan103/MQTT/blob/main/document/png/mp4-2_configure_action.png)

>---

![mp4-3_configure_action_new](https://github.com/xuan103/MQTT/blob/main/document/png/mp4-3_configure_action_new.png)

>---

![mp4-4_add_action](https://github.com/xuan103/MQTT/blob/main/document/png/mp4-4_add_action.png)

---

![mp5_rules_create_ck](https://github.com/xuan103/MQTT/blob/main/document/png/mp5_rules_create_ck.png)

>在新動作的圖磚中，可以在 Republish a message to an AWS IoT topic （重新發布訊息至 AWS 主題） 下方，看到修訂動作將發布的主題。

---

8. 在 Create a rule （建立規則） 中，向下捲動至底部並選擇 Create rule 建立規則並完成此步驟。

![mp6_rules_create_ok](https://github.com/xuan103/MQTT/blob/main/document/png/mp6_rules_create_ok.png)

