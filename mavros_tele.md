MAVROS and telemetry

Operation(test):

1  connect tele to pixhawk and computer

2  open terminal

    cd USART/c_uart_interface_example/
    ./mavlink_control -d /dev/ttyUSB0
then confirm the output.(open and then close QGC **may** help establish the connection)

3 run mavros

    roscore
    rosrun mavros mavros_node _fcu_url:=/dev/ttyUSB0:57600 _gcs_url:=udp://@172.16.254.1
   
 to be tested afterwards
 
    rosrun offb_py linefollowing.py
    
Reference:

 1. [github:mavros](https://github.com/mavlink/mavros/blob/master/mavros/README.md)
 
 2. [CSDN:使用无线数传 radio telemetry 连接pixhawk进入offboard模式进行mavlink协议通讯的尝试](https://blog.csdn.net/qq_31310793/article/details/78472676)
 
 3. [mavlink-tele-example](https://github.com/mavlink/c_uart_interface_example)

 
