# elsint

elsint app composed of distributed components
a. rest_server 
b. tcp-to-udp
c. udp-to-tcp
d. worker

example of run command with file a.txt that has content 
2
23

$rest_server a.txt
2
3

rest_server reads input file and sends its content via b,c components to  worker component
worker component returns the length of each line via path c,b.
rest server prints the lengths as in the example

b convert incoming tcp on 8021 port to outgoing udp 8022 port  , incoming udp 8022 port to tcp outgoing 8021 port 
c convert incoming udp 8022 port to outcoming tcp 8023 port , incoming tcp  8023 port to outcoming udp 8022 port  
d listens on tcp 8023 port  and returns line lengths 




