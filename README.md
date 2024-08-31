Repositório de Projetos Práticos de Segurança da Informação

Introdução

Este repositório contém dois projetos práticos realizados durante o curso de Segurança da Informação. Cada projeto aborda diferentes aspectos de segurança cibernética, explorando tanto a implementação de medidas de segurança em redes quanto a análise de vulnerabilidades em aplicações web.

1º Projeto - Implementação de Redes Seguras
Objetivo:
Configurar e implementar uma solução de segurança de rede utilizando firewall (pfSense), WAF e SIEM para monitoramento e resposta a incidentes.

Etapas do Projeto:

1.	Preparação do Ambiente:
o	1.1 Criar uma máquina virtual com Graylog (Debian 11, MongoDB 4.2.21, Graylog 4.3) para receber logs via Syslog.
o	1.2 Configurar o pfSense como firewall, roteador e servidor de Syslog.
2.	Configuração do NAT:
o	2.1 Implementar NAT no pfSense para traduzir endereços IP entre a rede interna e externa.
3.	Implementação do Graylog:
o	3.1 Configurar o Graylog para receber e analisar logs de diferentes dispositivos de rede.
4.	Testes e Validação:
o	4.1 Testar as regras de firewall e analisar os logs para verificar a segurança da rede.
Ferramentas Utilizadas:
•	pfSense, Graylog, VirtualBox, Debian 11, MongoDB.

________________________________________

2 Projeto - Testando Vulnerabilidades na Aplicação OWASP Juice Shop
Objetivo:
Utilizar a aplicação OWASP Juice Shop para identificar e explorar vulnerabilidades comuns em aplicações web.


Etapas do Projeto:

1.	Preparação do Ambiente:
o	1.1 Baixar a imagem Docker da aplicação OWASP Juice Shop no sistema Kali Linux.
o	1.2 Executar a aplicação com o comando:
sudo docker run -d -p 3000:3000 bkimminich/juice-shop.

3.	Exploração e Testes:
	2.1 Coletar informações e reconhecimento utilizando ferramentas como Nmap, dirb e gobuster.
	Comandos utilizados:
	nmap -p 3000 <IP da aplicação>
	gobuster dir -u http://<IP>:3000 -w /usr/share/wordlists/dirb/common.txt
	dirb http://<IP>:3000 /usr/share/wordlists/dirb/common.txt
o	2.2 Testar entradas de dados para vulnerabilidades de XSS (Cross-Site Scripting):
	Injetar scripts maliciosos como:
	<script>alert('XSS Test');</script>
	<iframe src="javascript:alert('xss')">
o	2.3 Realizar testes de SQL Injection:
	Utilizar a sintaxe ' OR true-- para tentativa de acesso não autorizado.
o	2.4 Executar testes de força bruta com Hydra e Burp Suite:
	Interceptar requisição de login com Burp Suite.
	Utilizar o comando:
sudo hydra -L ~/Downloads/email-top-100-domains.txt -P ~/Downloads/rockyou.txt <IP> -s 3000 http-get /rest/user/login

4.	Identificação de Vulnerabilidades:
o	3.1 Identificar diretórios expostos.
o	3.2 Detectar vulnerabilidades de XSS.
o	3.3 Encontrar falhas de SQL Injection.
o	3.4 Avaliar proteções contra ataques de força bruta.

5.	Soluções Propostas:
o	4.1 Configurar permissões adequadas para evitar exposição de diretórios.
o	4.2 Implementar validação e sanitização de entradas para prevenir XSS.
o	4.3 Validar e sanitizar entradas de dados para mitigar SQL Injection.
o	4.4 Melhorar a proteção contra ataques de força bruta com medidas como CAPTCHA e bloqueio de IP.



Ferramentas Utilizadas:
•	Docker, OWASP Juice Shop, Kali Linux, Nmap, dirb, gobuster, Burp Suite, Hydra, SQLmap.


Conclusão

Os projetos apresentados neste repositório ilustram o uso de ferramentas e técnicas para fortalecer a segurança de redes e aplicações web. A Implementação de Redes Seguras demonstrou a importância de uma configuração adequada de firewall e monitoramento de eventos, enquanto o teste de vulnerabilidades na aplicação OWASP Juice Shop destacou as ameaças comuns em ambientes web e as melhores práticas para mitigá-las.
