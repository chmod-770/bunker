# Lab: Network Namespaces + veth

## Objetivo
Entender isolamento de rede no kernel Linux

## RESUMO 
1. criei dois namespaces & duas veths
2. Settei o ip 172.26.255.1 na veth1 via 'ip netns exec ns1...' e o ip '.2' na veth2
3. rodei 'ip netns exec ns1 ping -c 172.16.255.1' num terminal, e em outro rodei um 'ip netns exec ns2 tcpdump'
    deu pra ver os pacotes passando, muito massa kkk. rodei um ip neighbor tabem, ip route.. mostrou direitinho
4. ia subir uma regra, porem nao sei nftables ainda, ficaria meio avulso
5. bom, no geral, usando o prefixo "ip netns exec $name", o restante 'e basicamente igual, 
    seria algo como "podman exec" s'o q em contexto diferente - resumo: 'e muito 'e massa - nota 10 XD


## ANOTACAO
- veth sao cabos virtuais, e a funcao e ligar dois links, entao nao inventa moda
- um uso legal seria, sobe 2 bridges, setta um par de veths nelas e veja as duas conversarem
    * dhcp relay deve funcionar ( eu acho )
