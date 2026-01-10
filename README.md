# 🚀 Reliability-app

[![License](https://img.shields.io/badge/license-MIT-green.svg?style=flat)](LICENSE)

Esta é uma API REST construída em Python utilizando o framework Flask, projetada para demonstrar práticas fundamentais de DevOps e SRE (Site Reliability Engineering) em um ambiente de produção.<br>
<br>
🎯 **Objetivo**: <br>
A aplicação implementa uma API minimalista porém funcional, onde temos na prática:<br>
- Containerização com Docker<br>
- Pipelines de CI/CD<br>
- Testes automatizados<br>
- Monitoramento e observabilidade<br>
- Processos de deploy e rollback<br>

  
**Esta é a estrutura do projeto, seus recursos e funções**:

![estrutura-diretorios](https://github.com/user-attachments/assets/01f066d9-5e4b-483d-923c-1e02b255bc26) 

<br>

Esta estrutura reflete princípios de separação de responsabilidades, automação e confiabilidade essenciais em práticas DevOps/SRE.

<br>

**A API expõe dois endpoints principais:**

Retorna informações sobre a aplicação e métricas básicas de uso


```json
{
  "message": "Aplicação SRE Nível 1",
  "version": "1.0.0",
  "total_requests": 42
}
```

Características:

- Versionamento dinâmico: A versão é configurável via variável de ambiente APP_VERSION
- Contador de requisições: Rastreia o total de acessos ao endpoint (útil para métricas básicas)
- Resposta JSON: Formato padrão para comunicação entre serviços

❤️ /health → health check

Endpoint de monitoramento que indica o status da aplicação:
```
{
  "status": "healthy",
  "timestamp": "2026-01-09T14:30:45.123456"
}
```
<br>
<br>

**- Práticas DevOps/SRE Implementadas:**

<br>
<br>

✅ **Containerização**
- Dockerfile otimizado para produção
- Imagem leve e segura
- Fácil replicação em qualquer ambiente

✅ **Testes Automatizados**
- Suite completa de testes com Pytest
- Validação de endpoints e respostas
- Integração com CI/CD

✅ **CI/CD Pipeline**
- Build automatizado no GitHub Actions
- Execução de testes em cada commit
- Deploy contínuo após aprovação

✅ **Monitoramento**
- Health checks para verificação de disponibilidade
- Scripts de monitoramento automatizado
- Métricas básicas de uso

✅ **Deployment Seguro**
- Script de deploy automatizado
- Processo de rollback em caso de falhas
- Versionamento controlado

<br>

🔄 **Fluxo de Trabalho**
```
Desenvolvimento → Testes → Build → Deploy → Monitoramento
      ↓             ↓         ↓       ↓          ↓
   (local)      (pytest)  (Docker) (scripts)  (health)
                                      ↓
                                  Rollback
                                (se necessário)
````


<br>
<br>

**🛠️ Tecnologias Utilizadas:** 

🐧 Linux Ubuntu - v: 24.04.3 LTS

🐳 Docker - v: 29.0.2

🤖 Github Actions

🐍 Python Flask - v: 2.3.0

<br>
<br>


**- Como executar o projeto:**

1.Clonar o repositório
```
# Clone o projeto
git clone https://github.com/sheila-silva/Reliability-app.git

# Entre no diretório
cd Reliability-app
```
2.Construindo e testando o container 🐳
```
# Construir a imagem
docker build -t sre-app:1.0.0 app/

# Executar o container
docker run -d -p 8080:8080 --name minha-app sre-app:1.0.0

# Testar
curl http://localhost:8080/health

# Ver logs
docker logs minha-app

# Parar e remover
docker stop minha-app
docker rm minha-app
````
3.Teste local antes de fazer o push:
````
cd tests
pip install -r requirements.txt
pytest -v test_app.py
````
5.Torne o script executável e teste:
````
chmod +x monitor.sh

# Inicie a aplicação em um terminal
docker run -d -p 8080:8080 sre-app:1.0.0

# Execute o monitor em outro terminal
./monitor.sh
````
6.Teste do processo completo:
````
# Torne os scripts executáveis
chmod +x deploy.sh rollback.sh

# Faça um deploy
./deploy.sh 1.0.0

# Verifique se está funcionando
./monitor.sh

# Simule um rollback
./rollback.sh

# Verifique se voltou
./monitor.sh
````




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

**🛠️ Technologies Used:**

🐧 Linux Ubuntu

🐳 Docker

🤖 GitHub Actions

🐍 Python Flask

<br>
<br>

-----------
-----------


# Agradecimentos / Referências 

Alura - Cursos On Line de Tecnologia 

<br>


----------
----------


# Autora:

Sheila M. M. L. Silva 

https://www.linkedin.com/in/sheilasheila/


