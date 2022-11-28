# Compiled-TCP-congestion-control-elastic-without-errors
Ready binary file Tcp Congestion Control Compiled without errors

I have compiled "without errors" on Debian 11 TCP Control elastic. The source code is taken from. https://github.com/cxxtao/tcp-elastic
Maybe someone will come in handy.

Installation.
Only Debian.
If you want to use it on other "Distributions", you will have to compile it yourself.
Download tcp_elastic.ko or archive with it. Unpack. sudo cp tcp_elastic.ko /lib/modules/$(uname -r)/kernel/net/ipv4 sudo depmod -a

You can without rebooting, immediately activate. sudo gedit /etc/sysctl.conf At the very end, add to the new line. net.ipv4.tcp_congestion_control = elastic Apply. sudo sysctl -p Verify. sudo sysctl -a | grep elastic

Скомпилированный мною "Без Ошибок" на Debian 11 TCP congestion control tcp_elastic.ko. Исходный код взят из. https://github.com/cxxtao/tcp-elastic Может кому-то пригодится.

Установка.
Только для Debian.
Если хотите использовать на других "Дистрибутивах", то прийдется компилировать самостоятельно.
Скачать tcp_elastic.ko или архив с ним.
Распаковать.
sudo cp tcp_elastic.ko /lib/modules/$(uname -r)/kernel/net/ipv4
sudo depmod -a

Можно без перезагрузки, сразу активировать. sudo gedit /etc/sysctl.conf в самый конец, в новой строке добавить. net.ipv4.tcp_congestion_control = elastic Применить. sudo sysctl -p Проверить. sudo sysctl -a | grep elastic
