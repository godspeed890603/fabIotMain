## 目的說明
在2019年，Stocker自動量測使用的電力電無法知道剩餘的電量，導致移動量測系統異常，因此採用電壓回傳，當電壓低於設定電壓，系統將會CALL BACK移動量測設備，</br></br>
待充電再度完成，系統將會自動依據排程，將自動量測安排出發，執行任務。</br></br>
下圖為製作時間</br>
https://www.facebook.com/photo.php?fbid=10211965113081679&set=pb.1788131020.-2207520000&type=3</br></br>
## 架構說明
1.採用ESP8266與廠內無線網路。</br></br>
2.採用光耦合器取代繼電器，待系統完全初始化結束，觸發光耦合器讓動力電壓進入系統
3.因為是移動式設備，當使Wifi強度無法使系統正常傳遞資料，將會斷線重新連線，維持正常資料收集</br></br>
4.電壓收集部分有當輔導高中多元學習的資料，有針對ADC讀取做資料，利用EXCEL趨勢線作校正</br></br>
https://hackmd.io/@PIahL8k2RMKl1pUj4lRpCA/BksLYWwys</br></br>
5.透過https://github.com/godspeed890603/fabIotMain/blob/master/data/f.txt設定，可以支援設定檔中的感應器</br></br>
Dht(1 Wwire)、Noise(BZY)、Gyro(mpu6050/i2c)，Volt(adc)、Pms(pms5003/uart)、SHTXX(Sht31/i2c)
## 成果
https://github.com/godspeed890603/fabIotMain/tree/master/result
