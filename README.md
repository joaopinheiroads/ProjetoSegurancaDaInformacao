Repositório de Projetos Práticos de Segurança da Informação
Introdução
Este repositório contém dois projetos práticos realizados durante o curso de Segurança da Informação. Cada projeto aborda diferentes aspectos de segurança cibernética, explorando tanto a implementação de medidas de segurança em redes quanto a análise de vulnerabilidades em aplicações web.

Projetos
1º Projeto - Implementação de Redes Seguras
Objetivo:
Configurar e implementar uma solução de segurança de rede utilizando firewall (pfSense), WAF e SIEM para monitoramento e resposta a incidentes.

Etapas do Projeto:

Preparação do Ambiente:

Criação de uma máquina virtual com Graylog (Debian 11, MongoDB 4.2.21, Graylog 4.3) para receber logs via Syslog.
Configuração do pfSense como firewall, roteador e servidor de Syslog.
Configuração do NAT:

Implementação de NAT no pfSense para traduzir endereços IP entre a rede interna e externa.
Implementação do Graylog:

Configuração do Graylog para receber e analisar logs de diferentes dispositivos de rede.
Testes e Validação:

Teste de regras de firewall e análise de logs para verificar a segurança da rede.
Ferramentas Utilizadas:

pfSense, Graylog, VirtualBox, Debian 11, MongoDB.
2º Projeto - Testando Vulnerabilidades na Aplicação OWASP Juice Shop
Objetivo:
Utilizar a aplicação OWASP Juice Shop para identificar e explorar vulnerabilidades comuns em aplicações web.

Etapas do Projeto:

Preparação do Ambiente:

Download e execução da imagem Docker da aplicação OWASP Juice Shop em um sistema Kali Linux.
Exploração e Testes:

Coleta de informações e reconhecimento utilizando ferramentas como Nmap, dirb e gobuster.
Testes de entrada de dados para identificar vulnerabilidades de XSS (Cross-Site Scripting) e SQL Injection.
Testes de autenticação e autorização utilizando ataques de força bruta com Hydra e Burp Suite.
Identificação de Vulnerabilidades:

Exposição de diretórios confidenciais.
Execução de scripts maliciosos (XSS).
Injeções SQL.
Proteção contra força bruta.
Soluções Propostas:

Configurações de segurança recomendadas para mitigar as vulnerabilidades encontradas.
Ferramentas Utilizadas:

Docker, OWASP Juice Shop, Kali Linux, Nmap, dirb, gobuster, Burp Suite, Hydra, SQLmap.
Conclusão
Os projetos apresentados neste repositório ilustram o uso de ferramentas e técnicas para fortalecer a segurança de redes e aplicações web. A Implementação de Redes Seguras demonstrou a importância de uma configuração adequada de firewall e monitoramento de eventos, enquanto o teste de vulnerabilidades na aplicação OWASP Juice Shop destacou as ameaças comuns em ambientes web e as melhores práticas para mitigá-las.
