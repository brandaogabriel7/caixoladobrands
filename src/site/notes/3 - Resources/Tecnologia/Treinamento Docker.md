---
{"dg-publish":true,"dg-path":"Tecnologia/Treinamento Docker.md","permalink":"/tecnologia/treinamento-docker/","tags":["excalidraw"],"created":"2025-04-10T17:21:56.013-03:00","updated":"2026-01-23T14:26:31.804-03:00"}
---

## Outline
- Treinamento de Docker e Docker Compose
- Virtualização vs Containers
    - Formas de criar ambientes isolados
    - Virtualização
        - Cada instância tem seu próprio SO abaixo das libs e dos apps
        - Hypervisor é o programa que ajuda a gerenciar essas diferentes máquinas
    - Container
        - O SO é compartilhado
        - A Container Engine usa técnicas para abstrair o uso dos recursos pelo container e isolar os processos
        - Mais leve e previsível
- O que é o Docker?
    - Programa que ajuda a gerenciar o clico dos containers
- O que é o Docker compose?
- Dockerfile, imagem e container
    - Exemplo de Dockerfile
    - Explicação das camadas
    - Ambiente previsível
- Exemplos de Dockerfile e docker compose
    - [GitHub - brandaogabriel7/full-cycle-arquitetura-hexagonal](https://github.com/brandaogabriel7/full-cycle-arquitetura-hexagonal)
    - [GitHub - brandaogabriel7/docker-laravel: A challenge to create a Laravel project with docker-compose.](https://github.com/brandaogabriel7/docker-laravel)
- CI/CD
- Prática Docker e Docker Compose
    - Aplicação de usuários
        - [GitHub - brandaogabriel7/simple-lab-mern-test](https://github.com/brandaogabriel7/simple-lab-mern-test)
    - Divisão em times
    - Alguns vão ficar com a variação de backend
        - [simple-lab-mern-test/instrucoes-pratica-backend.md at backend-dockerfile-pratica · brandaogabriel7/simple-lab-mern-test · GitHub](https://github.com/brandaogabriel7/simple-lab-mern-test/blob/backend-dockerfile-pratica/instrucoes-pratica-backend.md)
        - Outros vão ficar com a variação de frontend
            - [simple-lab-mern-test/instrucoes-pratica-frontend.md at frontend-dockerfile-pratica · brandaogabriel7/simple-lab-mern-test · GitHub](https://github.com/brandaogabriel7/simple-lab-mern-test/blob/frontend-dockerfile-pratica/instrucoes-pratica-frontend.md)
    - Podem usar a branch principal de cola mas digitem tudo, é pouca coisa

# Excalidraw Data

## Text Elements
Friday Upgrade
{ #mtfAGnSz}


Conteúdo
{ #kuq7C4IC}


- VMs vs Containers
- Docker e Docker compose
- Dockerfile, imagem e container
- Exemplos
- Prática Docker e Docker compose
{ #FVHLyxVm}


Máquina virtual
vs
Container
{ #EHC4MnM1}


https://www.netapp.com/blog/containers-vs-vms/
{ #zgItbXRF}


- Criar imagens
- Rodar containers
- Interagir com containers
{ #cY5zqUPY}


Imagem
{ #7gIv6Vae}


Dockerfile
{ #fW3AyAjr}


- Captura do estado de um container
- Binários, libs, arquivos e pastas
- O que ele faz?
- Qual porta ele exporta?
{ #MAd4x7a3}


- Arquivo especial que especifica como
montar uma imagem de container
- Define todas as camadas da imagem
{ #usffM7kn}


E o Docker compose?
{ #Mk0jdUFi}


Prática Docker
{ #mEU4930Z}


## Embedded Files
ddadbd1554e59e4fac6776c4a77c3eaca6055abe: [[Pasted Image 20250410173702_737.png]]

da71fd642b87b6643cb47832f47d74369288113c: [[Pasted Image 20250410181310_665.png]]

