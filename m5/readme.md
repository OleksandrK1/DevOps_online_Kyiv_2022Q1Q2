### EPAM University Programs DevOps external course
## Module � Linux Networking
# Task 5
��������� ������� ������ Linux Networking ��������� ��������� �������� Virtual Box �����, �� ��������� �� ������� 1
������� 1
Host � �� ��������, �� ����� ��������� Virtual Box;
Server_1 � ³�������� ������, �� ��� ���������� �� Linux. Int1 ���� ������ � ����� ���������� ��� ���������� �� ����� Net1, ����� ����������� � ��������� ������� �������� �����. IP-������ Int1 �������������� �������� �������� �� ��������� ��������, ��������� 192.168.1.200/24. ���������� Int2 �� Int3 �������� ��������� � ����� ��������� ������ �� ����� Net2 �� Net3.
Client_1 �� Client_2 � ³������� ������, �� ���� ���������� �� Linux (������ ��� ������������, ��������� Ubuntu �� CentOS). ���������� �������� � ����� ��������� ������ �� ����� Net2, Net3 �� Net4 �� �������� �� ������� 1.
������ ����� Net2 � 10.Y.D.0/24, �� Y � �� ������ ����� � ������ ���� ����������, D � ���� ����������.
������ ����� Net3 � 10.M.Y.0/24, �� M � ����� ����� ����������.
������ ����� Net4 � 172.16.D.0/24.
�����! ����, �������� ������ Net2, Net3 ��� Net4 ������������ � �������� ��������� Net1 � �������� ������ ����� ������ �� ������� ������.
1. �� Server_1 ����������� ������� ������ �� ��� �����������.
[![N|Solid](https://github.com/OleksandrK1/DevOps_online_Kyiv_2022Q1Q2/raw/main/m2/task5/5_1.jpg)]
2. �� Server_1 ����������� DHCP �����, ���� ���� ������������� ������ Int1 Client_1 �� Client_2
[![N|Solid](https://github.com/OleksandrK1/DevOps_online_Kyiv_2022Q1Q2/raw/main/m2/task5/5_2.jpg)]
3. �� ��������� ������ ping �� traceroute ��������� ��'���� �� ����������� ��������. ��������� ��������.
[![N|Solid](https://github.com/OleksandrK1/DevOps_online_Kyiv_2022Q1Q2/raw/main/m2/task5/images/5_3_1.jpg)] __ping from Server1 to Client1__
[![N|Solid](https://github.com/OleksandrK1/DevOps_online_Kyiv_2022Q1Q2/raw/main/m2/task5/images/5_3_2.jpg)] __ping from Client1 to Server1__
[![N|Solid](https://github.com/OleksandrK1/DevOps_online_Kyiv_2022Q1Q2/raw/main/m2/task5/images/5_3_3.jpg)] __traceroute from Server1 to Client1__
[![N|Solid](https://github.com/OleksandrK1/DevOps_online_Kyiv_2022Q1Q2/raw/main/m2/task5/images/5_3_4.jpg)] __traceroute from Client1 to Server1__
[![N|Solid](https://github.com/OleksandrK1/DevOps_online_Kyiv_2022Q1Q2/raw/main/m2/task5/images/5_3_5.jpg)] __ping from Server1 to Client2__
[![N|Solid](https://github.com/OleksandrK1/DevOps_online_Kyiv_2022Q1Q2/raw/main/m2/task5/images/5_3_6.jpg)] __ping from Client2 to Server1__
[![N|Solid](https://github.com/OleksandrK1/DevOps_online_Kyiv_2022Q1Q2/raw/main/m2/task5/images/5_3_7.jpg)] __traceroute from Server1 to Client2__
[![N|Solid](https://github.com/OleksandrK1/DevOps_online_Kyiv_2022Q1Q2/raw/main/m2/task5/images/5_3_8.jpg)] __traceroute from Client2 to Server1__
�����! ��� ����, ��� � Client_1 �� Client_2 ��������� ������ � ������ Internet (������ ��� ����������� � Internet �� Client_1 �� Client_2) �� Wi-Fi Router ��������� ����������� ������� �������� ��� ����� Net2 �� Net3
[![N|Solid](https://github.com/OleksandrK1/DevOps_online_Kyiv_2022Q1Q2/raw/main/m2/task5/images/5_3_9.jpg)] __Wi-Fi Router Static routing for Net2 and Net3__
4. �� ����������� ���������� lo Client_1 ���������� �� �� ������ �� ����� ��������: 172.17.D+10.1/24 �� 172.17.D+20.1/24. ����������� ������������� ����� �����, ��� ������ � Client_2 �� 172.17.D+10.1 �������� ����� Server_1, � �� 172.17.D+20.1 ����� Net4. ��� �������� ����������� traceroute.
[![N|Solid](https://github.com/OleksandrK1/DevOps_online_Kyiv_2022Q1Q2/raw/main/m2/task5/images/5_4_1.jpg)] __ip a Client1__
[![N|Solid](https://github.com/OleksandrK1/DevOps_online_Kyiv_2022Q1Q2/raw/main/m2/task5/images/5_4_2.jpg)] __ip route Client2__
[![N|Solid](https://github.com/OleksandrK1/DevOps_online_Kyiv_2022Q1Q2/raw/main/m2/task5/images/5_4_3.jpg)] __traceroute from Client2 to Client1 on 172.17.D+10.1/24 via Server1__
[![N|Solid](https://github.com/OleksandrK1/DevOps_online_Kyiv_2022Q1Q2/raw/main/m2/task5/images/5_4_4.jpg)] __traceroute from Client2 to Client1 on 172.17.D+20.1/24 via Net4__
5. ����������� ������ ������ �� ����� (summarizing) ����� 172.17.D+10.1 �� 172.17.D+20.1, ��� ���� ����� �� ���� ����������� ��������. �������� ��������, ���������� �� ������������ ����� �� ������� �� �ᒺ������ ���������, ��� �� ��������� ����� Server_1.
__172.17.32.0/20__
[![N|Solid](https://github.com/OleksandrK1/DevOps_online_Kyiv_2022Q1Q2/raw/main/m2/task5/images/5_5_1.jpg)] __route -n Server1__
[![N|Solid](https://github.com/OleksandrK1/DevOps_online_Kyiv_2022Q1Q2/raw/main/m2/task5/images/5_5_2.jpg)] __ip route Client2__
[![N|Solid](https://github.com/OleksandrK1/DevOps_online_Kyiv_2022Q1Q2/raw/main/m2/task5/images/5_5_3.jpg)] __traceroute from Client2 to Client1 on 172.17.D+10.1/24 via Server1__
[![N|Solid](https://github.com/OleksandrK1/DevOps_online_Kyiv_2022Q1Q2/raw/main/m2/task5/images/5_5_4.jpg)] __traceroute from Client2 to Client1 on 172.17.D+20.1/24 via Server1__
6. ����������� SSH ����� ����� �����, ��� Client_1 �� Client_2 ����� ����������� �� Server_1 �� ���� �� ������.
 __sudo apt-get install openssh-server__
7. ���������� �� Server_1 firewall ����� �����:
� ��������� ����������� ����� SSH � Client_1 �� ���������� � Client_2
[![N|Solid](https://github.com/OleksandrK1/DevOps_online_Kyiv_2022Q1Q2/raw/main/m2/task5/images/7_1.jpg)] __ufw status Server1__
� � Client_1 �� 172.17.D+10.1 ping ��������, � �� 172.17.D+20.1 �� ��������

8. ���� � �.3 ���� ����������� ������������� ��� ������� Client_1 �� Client_2 �� ����� �������� � �������� ������� ������. �� Server_1 ����������� NAT ����� ����� �����, ��� � Client_1 �� Client_2 �������� ping � ������ ��������

