# Repositório de Projetos Práticos de Segurança da Informação



## Introdução



Este repositório contém dois projetos práticos realizados durante o curso de Segurança da Informação. Cada projeto aborda diferentes aspectos de segurança cibernética, explorando tanto a implementação de medidas de segurança em redes quanto a análise de vulnerabilidades em aplicações web.




## 1º Projeto - Implementação de Redes Seguras



Objetivo:
Configurar e implementar uma solução de segurança de rede utilizando firewall (pfSense), WAF e SIEM para monitoramento e resposta a incidentes.



### Etapas do Projeto:

1.	Preparação do Ambiente:
	1.1 Criar uma máquina virtual com Graylog (Debian 11, MongoDB 4.2.21, Graylog 4.3) para receber logs via Syslog.
	1.2 Configurar o pfSense como firewall, roteador e servidor de Syslog.
2.	Configuração do NAT:
	2.1 Implementar NAT no pfSense para traduzir endereços IP entre a rede interna e externa.
3.	Implementação do Graylog:
	3.1 Configurar o Graylog para receber e analisar logs de diferentes dispositivos de rede.
4.	Testes e Validação:
	4.1 Testar as regras de firewall e analisar os logs para verificar a segurança da rede.
Ferramentas Utilizadas:
•	pfSense, Graylog, VirtualBox, Debian 11, MongoDB.




________________________________________




## 2º Projeto - Testando Vulnerabilidades na Aplicação OWASP Juice Shop
Objetivo:
Utilizar a aplicação OWASP Juice Shop para identificar e explorar vulnerabilidades comuns em aplicações web.


Etapas do Projeto:

1.	Preparação do Ambiente.


3.	Exploração e Testes:
	2.1 Coletar informações e reconhecimento utilizando ferramentas como Nmap, dirb e gobuster.
	
	2.2 Testar entradas de dados para vulnerabilidades de XSS (Cross-Site Scripting):
   
	2.3 Realizar testes de SQL Injection:
	Utilizar a sintaxe ' OR true-- para tentativa de acesso não autorizado.

	2.4 Executar testes de força bruta com Hydra e Burp Suite:

	


4.	Identificação de Vulnerabilidades:
	3.1 Identificar diretórios expostos.
	3.2 Detectar vulnerabilidades de XSS.
	3.3 Encontrar falhas de SQL Injection.
	3.4 Avaliar proteções contra ataques de força bruta.

5.	Soluções Propostas:
	4.1 Configurar permissões adequadas para evitar exposição de diretórios.
	4.2 Implementar validação e sanitização de entradas para prevenir XSS.
	4.3 Validar e sanitizar entradas de dados para mitigar SQL Injection.
	4.4 Melhorar a proteção contra ataques de força bruta com medidas como CAPTCHA e bloqueio de IP.



Ferramentas Utilizadas:
•	Docker, OWASP Juice Shop, Kali Linux, Nmap, dirb, gobuster, Burp Suite, Hydra, SQLmap.


## Conclusão

Os projetos apresentados neste repositório ilustram o uso de ferramentas e técnicas para fortalecer a segurança de redes e aplicações web. A Implementação de Redes Seguras demonstrou a importância de uma configuração adequada de firewall e monitoramento de eventos, enquanto o teste de vulnerabilidades na aplicação OWASP Juice Shop destacou as ameaças comuns em ambientes web e as melhores práticas para mitigá-las.
