# Projeto de Phishing para captura de senhas do Facebook

### Descrição

Este projeto faz parte de um desafio promovido pela plataforma Digital Innovation One, em parceria com o Santander, que visa explorar a criação de um ataque de phishing como estudo sobre cibersegurança. O objetivo é reproduzir a configuração de um phishing utilizando o Social-Engineer Toolkit (SET) no Kali Linux.

### Ferramentas Utilizadas

- Kali Linux
- Social-Engineer Toolkit (SET)

### Configuração do Social-Engineer Toolkit (dentro do Kali Linux)

- Acesse o root: ``` sudo su ```
- Inicie o SET: ``` setoolkit ```
- Selecione o Tipo de ataque: ``` Social-Engineering Attacks ```
- Selecione o Vetor de ataque: ``` Web Site Attack Vectors ```
- Selecione o Método de ataque: ```Credential Harvester Attack Method ```
- Selecione a opção: ``` Site Cloner ```
- Insira o endereço IP da máquina (obtenha com ``` ifconfig ```)
- Insira a URL a ser clonada (neste caso, http://www.facebook.com)

### Resultado Observado

- O SET clonou o site com sucesso e estava acessível na rede local. No entanto, as credenciais capturadas estavam cifradas ou inutilizáveis.

![Captura de tela 2024-12-11 174426](https://github.com/user-attachments/assets/81e5ac92-ce7e-40f7-ae83-b49bb7e54ffe)

### Considerações Finais

Este projeto demonstrou que, apesar de ser uma ferramenta didática, o Social-Engineer Toolkit (SET) apresenta limitações sérias em ambientes modernos, onde HTTPS e criptografia local são amplamente utilizados.
Os navegadores atuais adotam mecanismos avançados para proteger os usuários, como Sanitização de Dados, HSTS e CSP. Além disso, sites como o Facebook utilizam criptografia local em JavaScript e Tokens Dinâmicos, o que explica a presença de campos como _spin_r e _spin_b, visíveis na captura do SET, mas ilegíveis sem descriptografia.

#### Observações Extras/Próximos Passos

Para os engajados, será interessante explorar ferramentas mais modernas, como o Evilginx2, para entender como elas contornam essas limitações.
