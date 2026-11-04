# Configuração SSH

## Objetivo

Escolhemos o SSH por ser mais seguro, pois criptografa a comunicação entre os dispositivos. Já o Telnet não possui criptografia, permitindo que as informações transmitidas, incluindo senhas, possam ser interceptadas.

## Implementação

Primeiro, criamos o usuário `netadmin`. Em seguida, configuramos o domínio `techlab.local` e geramos chaves RSA de 1024 bits. Depois, habilitamos o SSH versão 2, configuramos a autenticação local nas linhas VTY e permitimos somente conexões SSH.

## Evidências

### Evidência 1 — Configuração SSH no roteador

Configuração do SSH versão 2, criação do usuário administrativo e definição da autenticação local, permitindo somente conexões SSH.

![Configuração SSH no Router0](../evidencias/evidencia-ssh-1.png)

### Evidência 2 — Teste de acesso remoto

Conexão SSH realizada pelo PC0 ao Router0, utilizando o usuário `netadmin`, confirmando o acesso remoto ao equipamento.

![Teste de conexão SSH pelo PC0](../evidencias/evidencia-ssh-2.png)
