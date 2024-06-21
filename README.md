Configuração das Interfaces dos Servidores 
enable 
    show ip interface brief 
    ping 192.168.10.252
    ping 192.168.10.251(erro)
    ping 192.168.10.250(erro)
    configure terminal
        interface range GigabitEthernet 1/0/10 - 12
            description interfaces de servidores
            switchport mode access 
            switchport nonegotiate  
            switchport access VLAN 20
            exit 
        interface GigabitEthernet 1/0/23 
            description interfaces de Wireless
            switchport mode access 
            switchport nonegotiate  
            switchport access VLAN 30 
        end
write 


