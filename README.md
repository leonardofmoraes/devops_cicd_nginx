# CI/CD com GitHub Actions, Docker e Nginx

Este projeto demonstra um fluxo simples de CI/CD usando GitHub Actions para construir uma imagem Docker e realizar o deploy de uma aplicação HTML com Nginx.

## 🔧 Tecnologias Utilizadas
- **GitHub Actions**: para automação da pipeline CI/CD
- **Docker**: para containerização da aplicação
- **Nginx**: servidor web leve para servir arquivos HTML
- **Docker Hub**: como repositório de imagens

## 🚀 Como Funciona

1. Push na branch `main` inicia o workflow do GitHub Actions
2. O GitHub Actions:
   - Faz build do container com o HTML e Nginx
   - Faz push da imagem para o Docker Hub

## 🗂 Estrutura do Projeto

```
.
├── Dockerfile
├── index.html
├── nginx.conf
└── .github
    └── workflows
        └── deploy.yml
```

## ⚙️ Como Usar

### Pré-requisitos
- Conta no [Docker Hub](https://hub.docker.com)
- Repositório no GitHub
- Secrets configurados no GitHub:
  - `DOCKER_USERNAME`
  - `DOCKER_PASSWORD`

### Publicar no GitHub

1. Crie um novo repositório no GitHub
2. Suba os arquivos do projeto
3. Configure os secrets `DOCKER_USERNAME` e `DOCKER_PASSWORD`
4. Faça push na branch `main`

A pipeline irá construir a imagem e fazer o push para o Docker Hub.

---

Desenvolvido por Leonardo Moraes.