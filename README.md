# Rede-corporativa-simples
Um laboratório de uma pequena rede corporativa, com objetivo de implementar as tecnologias que aprendi.

# Objetivo
Elaborar uma rede corporativa organizada, utilizando VLANs para segmentação, router-on-a-stick para roteamento inter VLAN, Trunk, STP, VLSM, static route, configuração DHCP e DNS.

# Topologia
<img width="1899" height="679" alt="Captura de tela 2026-06-23 194442" src="https://github.com/user-attachments/assets/f37c8feb-2faa-492d-8273-ca46ee490235" />

# Técnologias implementadas
### VLANs
VLAN é uma rede local virtual, utilizada para segmentar um domíni criando subredes, melhorando a segurança, o desempenho e a organização da rede.

<img width="642" height="271" alt="Captura de tela 2026-06-23 195425" src="https://github.com/user-attachments/assets/c71c1fd1-1f64-4ebb-ae51-6ca4d74fb276" />

### Trunk
O trunk permite que múltiplas VLANs trafeguem no enlace.

<img width="546" height="269" alt="Captura de tela 2026-06-23 200050" src="https://github.com/user-attachments/assets/eceacb92-a43a-4fe9-a933-b39205932a68" />

### STP
O protocolo Spanning Tree bloqueia loops em um domínio redundante. Ele desativa o link com o maior custo até o switch Root Bridge, e se por ventura um enlace falhar, esse link é ativado para a rede continuar funcionando.

<img width="688" height="640" alt="Captura de tela 2026-06-23 201316" src="https://github.com/user-attachments/assets/76e61012-47d3-4af4-b229-ac2aa2f21587" />

### Router-on-a-stick e 802.1q
A técnica router-on-a-stick permite o roteamento inter VLAN na camada de rede. Para ela funcionar, é necessário criar subinterfaces na interface do roteador, e implementar o encapsulamento 802.1q para o roteador ler a tag da VLAN que o quadro Ethernet carrega.

<img width="647" height="164" alt="Captura de tela 2026-06-23 201913" src="https://github.com/user-attachments/assets/6a45ac64-373e-4729-a8b8-f52e8c3cb2f1" />

### VLSM
O VLSM (Variable length subnetting mask) é o método de utilizar tamanho de máscaras variados, acabando com o desperdício do antigo modelo de classes IP(A, B, e C).
Neste projeto a máscara usada para as VLANs foi de /29 (255.255.255.248), permitindo 6 host válidos.

<img width="491" height="62" alt="Captura de tela 2026-06-23 202927" src="https://github.com/user-attachments/assets/cdf1a9f7-822d-4d12-b4d6-e8c55f9ac2c5" />

### Static route
Foi adicionado uma rota estática manualmente, para permitir comunicação com outras redes.
Neste projeto, foi feito uma rede externa para simular o roteamento entre redes.

<img width="599" height="358" alt="Captura de tela 2026-06-23 203923" src="https://github.com/user-attachments/assets/4d469537-cbb6-4f5f-80ab-b3b05989f9af" />

### DHCP
O DHCP é o protocolo usado para atribuír endereçamento IP aos clientes dinamicamente, além do endereço IP, ele atribui endereço de Gateway e servidor DNS.
Neste projeto, cada subinterface recebeu um pool de IPs para ser atribuído.

<img width="644" height="732" alt="Captura de tela 2026-06-23 203609" src="https://github.com/user-attachments/assets/943ab1c6-a40a-43b4-b9bd-185b7ce14b7f" />

# Funcionalidades
- Comunicação entre VLANs na camada de rede.
- Comunicação entre redes.
- Redundância entre switches.
- Atribuição de endereço IP e DNS via DHCP.
- Organização de departamentos.
- Roteamento estático entre redes.
- Economia de IPs com VSLM.

# Testes realizados
### Conectividade inter VLAN
Foi realizado ping em todos dispositivos de todas as VLANs para verificar a conectividade entre elas.

<img width="465" height="614" alt="Captura de tela 2026-06-23 204417" src="https://github.com/user-attachments/assets/39c89720-9a9f-4bdb-a626-6a2bd2a5c083" />
<img width="465" height="614" alt="Captura de tela 2026-06-23 204343" src="https://github.com/user-attachments/assets/4206b6c3-4863-4cc5-975b-827a90d097dd" />


### Conectividade entre redes
Foi realizado um ping para um endereço fora da rede para diagnóstico de conectividade.

<img width="459" height="197" alt="Captura de tela 2026-06-23 204701" src="https://github.com/user-attachments/assets/62ef3abc-ce1d-4e1d-bfec-8192bc40fc74" />


### STP over
Foi simulado a falha de um link para o switch root bridge, com objetivo de testar o funcionamento do protocolo STP.

- Link normal:

<img width="848" height="601" alt="Captura de tela 2026-06-23 204835" src="https://github.com/user-attachments/assets/90d27c76-ab11-4b00-ab38-c5bba0982394" />

- Link sem conexão:

<img width="854" height="603" alt="Captura de tela 2026-06-23 204909" src="https://github.com/user-attachments/assets/84e4abb9-28da-469f-a6d8-99a60b3d2baa" />

Conclusão: A blocking port foi ativada para manter a rede funcionando.


### Resolução DNS
Foi configurado um servidor DNS e um site Web para testar a resolução DNS.

<img width="1065" height="1026" alt="Captura de tela 2026-06-23 205206" src="https://github.com/user-attachments/assets/b26ac80b-2402-48fb-8b41-5b77406542bb" />


# Aprendizados
- Segmentação de domínio utilizando VLANs.
- Organização de departamentos.
- Criação de subinterfaces e utilização do protocolo 802.1q.
- Utilização de VSLM.
- Diagnóstico de conexão utilizando o comando ping.
- Redundância entre switches utilizando o protocolo Spanning Tree.
- Configuração do pool DHCP.
- Configuração de rotas estáticas.
