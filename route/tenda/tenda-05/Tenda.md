vendor:Tenda


product:AC9 AC7 AC10 and so on

version:V15.03.05.19(6318)_CN(AC9), V15.03.06.44_CN(AC7), V15.03.06.23_CN(AC10) and earlier

type:buffer overflow

author:Zhang Shao Jie

institution:NISL@Tsinghua University


Vulnerability description
-------------------------
I found a buffer overflow vulnerability in the router's web server--httpd. When processing the page parameters for a post request, the value is directly sprintf to a local variable placed on the stack, which overrides the return address of the function, causing buffer overflow.
The details are shown below:

![image](https://github.com/zsjevilhex/iot/blob/master/route/tenda/tenda-03/image.png)


POC
-------------------------

![image](https://github.com/zsjevilhex/iot/blob/master/route/tenda/tenda-03/poc.jpeg)

This PoC can result in a Dos. 


p.s.Given the vendor's security, we only provide parts of the URL.
