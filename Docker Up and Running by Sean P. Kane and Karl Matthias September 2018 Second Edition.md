
parent: [[Книги]]

стр. 21 Container Networking

To understand bridge mode, it’s easiest to think of each of your Docker containers as behaving
like a host on a private network. The Docker server acts as a virtual bridge and the containers
are clients behind it. A bridge is just a network device that repeats traffic from one side to
another. So you can think of it like a mini–virtual network with each container acting like a host
attached to that network.

Чтобы понять режим моста, проще всего представить, что каждый из ваших контейнеров Docker ведет себя как хост в частной сети. Сервер Docker действует как виртуальный мост, а контейнеры являются клиентами, стоящими за ним. Мост - это просто сетевое устройство, которое повторяет трафик с одной стороны на другую. Таким образом, вы можете думать об этом как о мини–виртуальной сети, где каждый контейнер действует как хост, подключенный к этой сети.

The actual implementation, as shown in Figure 24, is that each container has its own virtual
Ethernet interface connected to the Docker bridge and its own IP address allocated to the virtual
interface. Docker lets you bind and expose individual or groups of ports on the host to the
container so that the outside world can reach your container on those ports. That traffic passes
over a proxy that is also part of the Docker daemon before getting to the container.

Фактическая реализация, как показано на рисунке 24, заключается в том, что каждый контейнер имеет свой собственный виртуальный Интерфейс Ethernet, подключенный к Docker bridge, и свой собственный IP-адрес, выделенный виртуальному интерфейсу. Docker позволяет привязывать и предоставлять доступ к контейнеру отдельным портам или группам портов на хосте, чтобы внешний мир мог получать доступ к вашему контейнеру через эти порты. Этот трафик проходит через прокси, который также является частью демона Docker, прежде чем попасть в контейнер.

![[Pasted image 20240313090743.png]]