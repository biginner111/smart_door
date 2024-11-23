	在软件设计上，我采用了FreeRTOS作为操作系统，利用其时间片调度、软件定时器、消息队列及事件机制，确保了系统的高效运行与任务的灵活调度。
	存储方面，考虑到系统数据量小，我选择了1K容量的EEPROM来存储密码，通过IIC（I²C）协议与MCU通信，这种简单可靠的通信方式非常适合小数据量应用。
	显示层面，我采用了IIC驱动的OLED显示屏，其显示清晰、功耗低，非常适合作为小型设备的显示界面，用于反馈用户按键输入操作信息
	输入设计上，我设计了4x4矩阵按键，通过逐行逐列扫描法捕捉按键输入，实现密码输入功能。同时，引入了RFID无线感应技术和指纹模块，RFID通过串口与MCU通信读取身份卡片内容，实现无密码开锁；指纹模块则通过SPI与MCU通信，检测指纹信息实现指纹解锁，丰富了设备的解锁方式。
	通讯方面，我使用了ESP8266模块实现设备与终端的无线通信，ESP8266接收数据后通过UART与MCU通信，实现数据的无线传输和交互，满足了设备与外界进行数据交换的需求。
	终端方面，我利用QT框架设计了直观的人机交互界面，作为TCP客户端与ESP8266服务器建立连接，实现远程操作和控制MCU的功能。这样的设计不仅提升了用户操作的便捷性，还确保了设备与终端之间的高效通信。整个系统集成了多种技术，实现了高效、便捷的设备控制与管理。
