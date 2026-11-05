## Conclusão

Durante o desenvolvimento do projeto TechLab Networks, aprendi como implementar sub-redes IPv4 e utilizar VLANs para organizar logicamente os quatro setores de uma empresa, permitindo uma melhor distribuição dos endereços IP e a segmentação da infraestrutura de rede.

A configuração do roteamento inter-VLAN foi imprescindível para o nosso projeto, pois, por meio dele, conseguimos interligar as diferentes sub-redes da infraestrutura, permitindo que os dispositivos de departamentos distintos pudessem se comunicar e compartilhar recursos, como os serviços disponibilizados pelo servidor.

A implementação do DHCP foi importante porque permitiu fornecer automaticamente endereços IPv4, máscaras de sub-rede, gateways e servidores DNS aos dispositivos conectados à infraestrutura, facilitando a configuração e a administração das redes.

Também aprendemos a importância dos serviços DNS e HTTP. O DNS permite traduzir nomes de domínio em endereços IP, enquanto o HTTP possibilita que os usuários acessem o conteúdo das páginas web disponibilizadas pelo servidor. No nosso projeto, utilizamos esses serviços para permitir o acesso ao endereço `www.techlab.local`.

Decidimos utilizar o protocolo SSH para administrar nosso roteador remotamente por oferecer maior segurança. Diferentemente do Telnet, o SSH utiliza criptografia para proteger as informações transmitidas, dificultando a leitura do conteúdo da comunicação por terceiros.

A implementação da rede wireless foi muito importante para o nosso projeto, pois possibilitou que dispositivos móveis pudessem se conectar à infraestrutura sem a necessidade de utilizar cabos de rede. Dessa forma, os usuários passaram a ter maior mobilidade, podendo acessar os recursos da rede em diferentes ambientes da empresa, desde que estivessem dentro da área de cobertura do Access Point.

Também configuramos a segurança da rede wireless utilizando WPA2-PSK com criptografia AES, para proteger a comunicação entre os dispositivos e restringir o acesso à infraestrutura.

Durante o projeto, aprendemos a utilizar o Wireshark para capturar e analisar o tráfego de pacotes na rede. Essa ferramenta nos permitiu observar o funcionamento de protocolos como DNS, ICMP, TCP e TLS, além de identificar possíveis problemas de comunicação por meio da análise dos pacotes enviados e recebidos.

Aprendemos que, durante o troubleshooting, é importante investigar a causa de uma falha antes de realizar alterações nas configurações da rede. Para isso, utilizamos ferramentas como o `ping`, que permite testar a conectividade por meio de mensagens ICMP, além de verificar configurações como gateway, máscara de sub-rede, VLANs e rotas. Dessa forma, conseguimos identificar os problemas, aplicar as correções necessárias e validar o funcionamento da infraestrutura.

### Fluxo completo da comunicação

Outro aprendizado importante foi compreender como os dados percorrem as camadas da rede. Quando um computador acessa `www.techlab.local`, o DNS permite descobrir o endereço IP do servidor. Para acessar a página HTTP, o cliente estabelece uma conexão TCP, que utiliza o Three-Way Handshake.

Durante o encapsulamento, os dados passam pelas camadas de aplicação, transporte, rede, enlace e física. O TCP utiliza portas para identificar a comunicação, o IPv4 identifica os endereços de origem e destino, e o Ethernet utiliza endereços MAC para encaminhar os quadros no enlace local.

Quando o destino pertence a outra sub-rede, o computador envia o tráfego ao gateway. O roteador consulta sua tabela de roteamento, identifica a rede de destino e encaminha o pacote por meio de um novo quadro Ethernet. Ao chegar ao servidor, ocorre o desencapsulamento, permitindo que os dados sejam entregues à aplicação correspondente.

Com a realização desse projeto, conseguimos relacionar os conhecimentos teóricos de redes com situações práticas, desde o planejamento do endereçamento até a configuração dos serviços, a análise dos protocolos e a resolução de falhas de comunicação.
