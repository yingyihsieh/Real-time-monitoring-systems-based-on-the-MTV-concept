# Real-time-monitoring-systems-based-on-the-MTV-concept
read me
1. Introduction
Develop data analysis platform with Python,Mysql, sockjs-tornado,Psutil,pyecharts,and pyecharts-snapshot to set up the real-time monitoring systems based on the MTV concept to obtain information from hardware, and by query data tables and visual charts implemented
2. Implementation
There are further information and operaation below,
A.Analysis project directory:

| ---- manage.py #Entry startup file, responsible for startup file
| ---- app #Application package, store MTV
| -------- __init__.py #Init module, custom application, custom service
| -------- configs.py #Configuration information (site, database)
| -------- urls.py #Route view mapping configuration file (configure routing rules)
| -------- views #view package (storage view module)
| -------- models #model package (stores model modules)
| -------- templates #Template directory (stores HTML templates)
| -------- static #static file directory (CSS, js, pictures)
| -------- tools #Toolkit (chart, get hardware information, connect to database)
B.ORM model design- save raw data to database
- design memory,swap, cpu modules
-generate a data table
(import database connection driver,create a connection engine,the model is mapped into the table
C.Get hardware information
-get cpu information(cpu average usage rate,each cpu usage rate,or cpu logical core number)
-get memory information(Bytes to GB)
(include:total (GB),usage (GB),remaining amount (GB),usage rate (%))
-get swap information(Bytes to GB)
(include:total (GB),usage (GB),remaining amount (GB),usage rate (%))
-get disk information
(include:device name,mount point,file system type,operation options,total
 ,usage,remaining amount,usage rate)
-get network card information
(include:network card name,send byte,number of packets sent,Protocol                                                          address family,IP address,subnet mask,broadcast address
-get last boot time
-get recent user login information
(include:account,terminal,host,time,process)
D.System monitoring
-create websocket server
(establish a connection,send a message and actively push the message to all clients connected to the server,close the connection
3. Environment setting up
Python 3.6
sqlalchemy
Mysql 8.0.18
tornado
mysql-connector-python
sqlalchemy
sockjs-tornado
psutil
pyechart,pyecharts-snapshot

4. Further work
- create websocket client
-visual for memory,cpu,and swap
-real-time update of CPU,memory,swap information
