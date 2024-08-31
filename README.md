# 2° Projeto Prático - Segurança da Informação

Projeto desenvolvido durante o programa Desenvolve Boticário, em parceria com a Alura.

## Autor

- João Lucas Gomes Pinheiro

## Descrição

Este projeto visa desenvolver e implementar uma solução de segurança de rede, incluindo componentes principais como Firewall, WAF com Nginx e um SIEM. A configuração garante uma rede segura, protegendo contra ataques e ameaças.

## Ferramentas e Tecnologias Utilizadas

- **VirtualBox**: Utilizado para a criação de máquinas virtuais.
- **PfSense**: Implementado como firewall para proteger a rede.
- **Debian**: Sistema operacional utilizado para servidores.
- **Graylog**: Utilizado como SIEM (Security Information and Event Management) para coleta e análise de logs.
- **Nginx ModSecurity**: Utilizado como Web Application Firewall (WAF).
- **Snort**: Sistema de detecção e prevenção de intrusões (IDS/IPS).
- **Netfilter (iptables)**: Utilizado para manipulação de pacotes no Linux.

## Planejamento de Segurança

### Requisitos de Segurança

- **Firewall**: Uso do pfSense para proteger a rede.
- **Zonas Militarizadas e Desmilitarizadas**: Configuração de zonas DMZ para separação de serviços internos e externos.
- **WAF**: Configuração do Nginx ModSecurity para prevenção de ataques como SQL Injection e XSS.

### Políticas de Segurança

1. **Política de Senhas**:
   - Complexidade: Senhas devem ter um mínimo de caracteres e incluir letras maiúsculas, minúsculas, números e caracteres especiais.
   - Expiração: Troca de senhas periodicamente (a cada 90 dias).
   - Reutilização: Proibição da reutilização das últimas senhas.

2. **Política de Acesso à Rede**:
   - Implementar regras de firewall para limitar o acesso a serviços críticos.

3. **Política de Monitoramento de Segurança**:
   - Uso de ferramentas para monitoramento de logs e prevenção de ataques de força bruta.

### Objetivo de Segurança

- Desenvolver e manter uma rede segura, garantindo que todos os componentes estejam configurados e mantidos de acordo com as melhores práticas de segurança.

## Implementação

### Configuração do Ambiente

- Utilização do VirtualBox para criar máquinas virtuais e instalação dos sistemas:
  - **Internet**: IPv4 DHCP (modo Bridge)
  - **Server_Web**: IPv4 estático: 172.16.10.10/24
  - **Graylog**: IPv4 estático: 172.16.10.12/24
  - **WAF**: IPv4 estático: 172.16.20.12/24

### Configuração do Firewall

1. **Acesso ao pfSense**:
   - Acesse o firewall via navegador em: `http://192.168.56.2`
   - Usuário padrão: `admin`, Senha: `pfsense`

2. **Criação de Regras**:
   - Bloquear todo o tráfego por padrão e adicionar regras específicas para tráfegos autorizados.

3. **Configuração de Aliases**:
   - Criar aliases para IPs e portas para facilitar a criação de regras de firewall.

### Configuração de NAT e IPs Virtuais

- Configuração de NAT para traduzir endereços IP internos para IPs externos reconhecidos.
- Criação de IPs virtuais no pfSense para garantir o acesso adequado às interfaces de rede.

### Configuração do IDS/IPS

- Instalação e configuração do **Snort** no pfSense para monitoramento e prevenção de intrusões.

## Passos para Reproduzir o Projeto

1. Instale o VirtualBox e crie máquinas virtuais conforme as especificações.
2. Instale o pfSense e configure as regras de firewall e NAT conforme detalhado.
3. Instale e configure o Graylog e o Nginx ModSecurity para gerenciamento de logs e proteção da aplicação.
4. Configure o **Snort** no pfSense para monitoramento de rede.
5. Siga as instruções para definir políticas de segurança de senha, acesso e monitoramento.

## Conclusão

Este projeto demonstra a implementação de uma segurança robusta de rede utilizando diversas ferramentas e tecnologias, focando na prevenção e mitigação de ataques cibernéticos. A configuração apresentada é um guia prático para a criação de uma rede segura em ambientes de estudo e testes.

## Licença

Este projeto é distribuído sob a licença MIT. Consulte o arquivo [LICENSE](LICENSE) para mais informações.

## Contato

Para mais informações, entre em contato comigo em: https://www.linkedin.com/in/jo%C3%A3o-lucas-gomes-pinheiro-11914829a/
