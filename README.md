# 🚀 Reliability-app

[![License](https://img.shields.io/badge/license-MIT-green.svg?style=flat)](LICENSE)

Este repositório contém uma aplicação web simples (uma API) em Flask que expõe duas rotas e faz controle básico de requisições, esta API está instrumentada com práticas DevOps e  SRE (Site Reliability Engineering).
<br>
<br>
**Esta é a estrutura do projeto, seus recursos e funções:**
<br>
<br>
![estrutura-diretorios](https://github.com/user-attachments/assets/01f066d9-5e4b-483d-923c-1e02b255bc26)
<br>
README.md e DEPLOY.md fornecem instruções claras sobre uso e implantação
<br>
Aplicação:<br>
Código isolado no diretório app/ seguindo boas práticas de organização
Dockerfile permite deployment consistente em qualquer ambiente
<br>
Automação DevOps:<br>
deploy.sh - automatiza o processo de implantação
monitor.sh - verifica saúde e métricas da aplicação
rollback.sh - garante recuperação rápida em caso de problemas
<br>
Qualidade:<br>
Testes isolados no diretório tests/ com suas próprias dependências
Separação entre dependências de produção e desenvolvimento
<br>
Esta estrutura reflete princípios de separação de responsabilidades, automação e confiabilidade essenciais em práticas DevOps/SRE.
<br>
<br>
**A aplicação contém os seguintes endpoints:**

🏠 Endpoint raiz (/) → retorna versão e contador de requisições

❤️ /health → health check

📊 /metrics → métricas internas (uptime, taxa de sucesso, contadores)

⚠️ Captura de erros e atualização de métricas
<br>
<br>
<br>
<br>
**🔧 Nesta aplicação temos:**

🐳 Containerização com Docker

🧪 Testes automatizados com Pytest

🤖 Pipeline CI com GitHub Actions

📈 Métricas internas da aplicação

🩺 Monitoramento via script shell

🚀 Processo completo de Deploy automatizado

🔄 Processo seguro de Rollback
<br>
<br>
<br>
<br>
**🛠️ Tecnologias Utilizadas:** 

🐧 Linux Ubuntu

🐳 Docker

🤖 Github Actions

🐍 Python Flask

--------
--------

# 🚀 Reliability-app

This repository contains a simple web application (an API) built with Flask that exposes two routes and performs basic request tracking, this API is instrumented with SRE (Site Reliability Engineering) and DevOps practices. 
<br>
<br>
**The application contains the following endpoints:**

🏠 Root endpoint (/) → returns version and request counter

❤️ /health → health check

📊 /metrics → internal metrics (uptime, success rate, counters)

⚠️ Error capturing and metrics updating 
<br>
<br>
<br>
<br>
**🔧 In this application have:**

🐳 Containerization with Docker

🧪 Automated tests with Pytest

🤖 CI pipeline with GitHub Actions

📈 Internal application metrics

🩺 Monitoring via shell script

🚀 Fully automated deployment process

🔄 Safe rollback process 
<br>
<br>
<br>
<br>
**🛠️ Technologies Used:**

🐧 Linux Ubuntu

🐳 Docker

🤖 GitHub Actions

🐍 Python Flask

