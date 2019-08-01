# StressTest-JMeter 壓力測試-JMeter

以下內容用來測試WebAPI及Websocket
### 下載Apache JMeter
前往https://jmeter.apache.org/download_jmeter.cgi 下載並安裝

### 執行
<pre><code>./bin/jmeter.bat</code></pre>

### 安裝JMeterWebSocket
<p>將JMeterWebSocketSamplers-1.2.2.jar放置apache-jmeter-5.1.1\lib\ext\裡面</p>
<p>放置後重啟JMeter就會看到WebSocket有關的功能</p>

![JMeterWebSocket](https://github.com/ruby1126/StressTest-JMeter/blob/master/JMeter%20Websocket.png)

### 將結果輸出成html
<pre><code>cd ./bin
jmeter -n -t jmx的檔名.jmx -l 輸出檔名.jtl -e -o 輸入位置</code></pre>
<p>(沒設定則預設輸出到bin\report-output)</p>
<pre><code>參數
-n ：以非GUI形式運行Jmeter
-t ：jmeter腳本路徑
-l ：result.jtl 運行結果保存路徑（.jtl）此文件必須不存在。
-e ：在腳本運行結束後生成html報告
-o ：用於存放html報告的目錄，不加該參數默認生成到 bin\report-output
</code></pre>

### Example
#### API
將api_test.jmx load進來
有關設定可以自行查詢
![api_test Example](https://github.com/ruby1126/StressTest-JMeter/blob/master/api_test%E7%A4%BA%E7%AF%84.png)

#### WebSocket
將websocket_test.jmx load進來
有關設定可以自行查詢
![將websocket_test Example](https://github.com/ruby1126/StressTest-JMeter/blob/master/websocket_test.png)
