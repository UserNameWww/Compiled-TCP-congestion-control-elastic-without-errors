# Compiled-TCP-congestion-control-elastic-without-errors
Ready binary file Tcp Congestion Control Compiled without errors

I have compiled "without errors" on Debian 11 TCP Control PCC that operates on the basis of losses. The source code is taken from. https://github.com/cxxtao/tcp-elastic
Maybe someone will come in handy.

Installation. Download tcp_elastic.ko or archive with it. Unpack. sudo cp tcp_elastic.ko /lib/modules/$(uname -r)/kernel/net/ipv4 sudo depmod -a

You can without rebooting, immediately activate. sudo gedit /etc/sysctl.conf At the very end, add to the new line. net.ipv4.tcp_congestion_control = elastic Apply. sudo sysctl -p Verify. sudo sysctl -a | grep elastic
