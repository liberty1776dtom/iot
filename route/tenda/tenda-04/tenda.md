vendor:Tenda

product:AC9/AC10 

version:V15.03.05.19(6318)_CN(AC9),  V15.03.06.23_CN(AC10) and earlier

type:Remote Code Execution

author:Shaojie Zhang

institution:NISL@Tsinghua University

Vulnerability description
-------------------------
We find a RCE vulnerability in Tenda's router after connecting to it. Details are as follows:
While the router's web server--httpd processing the `mac` parameter for a post request, the value is directly passed to doSystemCmd function, causing a arbitrary command execution.The details are shown below:
![image](https://github.com/zsjevilhex/iot/blob/master/route/tenda/tenda-04/image4.jpg)

PoC
-------------------------
![image](https://github.com/zsjevilhex/iot/blob/master/route/tenda/tenda-04/image5.jpg)
This PoC can open telnet service.
