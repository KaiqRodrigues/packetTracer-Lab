LAN 1 - AREA 1(ospf):
VLAN + VLSM + DHCP
Dividi a rede 192.168.1.0 em 3 subredes utilizando VLSM e atribui cada um em uma VLAN e atribui os ips com pools de DHCP.
<img width="576" height="592" alt="Captura de tela 2026-11-08 115900" src="https://github.com/user-attachments/assets/acb46091-8c4f-4dc3-90ec-10942ca630de" />

VLAN 10 - 100 Dispositivos
192.168.1.0 - 192.168.1.127 

VLAN 30 - 50 Dispositivos
192.168.1.128 - 192.168.1.191 

VLAN 20 - 20 Dispositivos
192.168.1.192 - 192.168.1.223

LAN 2 - AREA 2(ospf):
WIRELESS + DHCP-SERVER:
Laptops conectados em um AP e um Servidor DHCP fazendo a atribuição de ips.
<img width="437" height="418" alt="Captura de tela 2026-11-08 115909" src="https://github.com/user-attachments/assets/f4d27b18-802d-45b9-93ec-372ad3b8f399" />


BACKBONE - AREA 0(ospf):
Dois rt ABR intermediados por um Switch de camada 2. 
<img width="320" height="590" alt="Captura de tela 2026-11-08 115925" src="https://github.com/user-attachments/assets/73fc24f1-84f1-42bd-9c28-93beacf4ac7b" />
Obs:
Apenas suas portas internas viradas para o SW estão na Area 0 do OSPF.
Anunciado por todos os RT, a comunicação ocorre sem problemas.
Durante os testes de conectividade entre as LANs, identifiquei um comportamente do tempo de convergência do OSPF no Packet Tracer: Ao pingar um pc da rede lan 1 por um pc da lan 2, recebi o "host nao acessivel". 
Procurei no running-config de cada dispositivo mas não encontrei. Depois passei o tempo da simulação, a tabela de roteamento de cada um foi atualizada e a conectividade ponta a ponta ocorreu sem problemas.
