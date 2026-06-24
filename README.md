# Rede-corporativa-simples
Projeto desenvolvido no Cisco Packet Tracer com foco na implementação de conceitos fundamentais de redes corporativas.

# Objetivo
Elaborar uma pequena rede corporativa, utilizando conceitos fundamentais de redes, como VLANs para segmentação de domínio e organização de departamentos, router-on-a-stick para comunicação entre VLANs, Trunk, 802.1q, STP, VLSM, static route, configuração DHCP e DNS.

# Topologia
<img width="1899" height="679" alt="Captura de tela 2026-06-23 194442" src="https://github.com/user-attachments/assets/f37c8feb-2faa-492d-8273-ca46ee490235" />

# Ambiente
Software: Cisco Packet Tracer

Dispositivos:
- 2 roteadores
- 3 switches
- PCs clientes
- Servidor DNS
- Servidor Web


# Tecnologias implementadas
- VLANs
- Router-on-a-stick
- Trunk 802.1q
- Spanning Tree Protocol (STP)
- VLSM
- Static route
- DHCP
- DNS


### Endereçamento
|VLAN|Departamento|Endereço de rede|
|--- |:----:      |:----:          |
|VLAN 10|Financeira|192.168.1.0/29|
|VLAN 20|Administrativa|192.168.1.8/29|
|VLAN 30|TI|192.168.1.16/29|
|VLAN 40|Gerenciamento|192.168.1.24/29|


# Funcionalidades
- Comunicação entre VLANs na camada de rede.
- Comunicação entre redes.
- Redundância entre switches.
- Atribuição de endereço IP e DNS via DHCP.
- Organização de departamentos.
- Roteamento estático entre redes.
- Economia de IPs com VLSM.

# Testes realizados
### Conectividade inter VLAN
Foram realizados testes de conexão ICMP em todos dispositivos de todas as VLANs para diagnóstico de conectividade entre elas.

<img width="465" height="614" alt="Captura de tela 2026-06-23 204417" src="https://github.com/user-attachments/assets/39c89720-9a9f-4bdb-a626-6a2bd2a5c083" />
<img width="465" height="614" alt="Captura de tela 2026-06-23 204343" src="https://github.com/user-attachments/assets/4206b6c3-4863-4cc5-975b-827a90d097dd" />


### Conectividade entre redes
Foi realizado um teste de conexão ICMP para um endereço fora da rede para diagnóstico de conectividade.

<img width="459" height="197" alt="Captura de tela 2026-06-23 204701" src="https://github.com/user-attachments/assets/62ef3abc-ce1d-4e1d-bfec-8192bc40fc74" />


### Teste de redundância STP
Foi simulado a falha de um enlace para o switch root bridge, com objetivo de testar o funcionamento do protocolo STP.

- Link normal:

<img width="848" height="601" alt="Captura de tela 2026-06-23 204835" src="https://github.com/user-attachments/assets/90d27c76-ab11-4b00-ab38-c5bba0982394" />

- Link sem conexão:

<img width="854" height="603" alt="Captura de tela 2026-06-23 204909" src="https://github.com/user-attachments/assets/84e4abb9-28da-469f-a6d8-99a60b3d2baa" />

Conclusão: A porta em estado de bloqueada foi ativada, permitindo a continuidade de comunicação.


### Resolução DNS
Foi configurado um servidor DNS e um site Web para testar a resolução DNS.

<img width="1065" height="1026" alt="Captura de tela 2026-06-23 205206" src="https://github.com/user-attachments/assets/b26ac80b-2402-48fb-8b41-5b77406542bb" />


# Habilidades demonstradas
- Segmentação de domínio utilizando VLANs.
- Organização de departamentos.
- Criação de subinterfaces e utilização do protocolo 802.1q.
- Utilização de VLSM.
- Diagnóstico de conexão utilizando ICMP.
- Redundância entre switches utilizando o protocolo Spanning Tree (STP).
- Configuração DHCP e resolução de nomes DNS.
- Configuração de rotas estáticas.
