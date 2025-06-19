# Marketplace de Serviços

Este projeto é um formato de marketplace de serviços que estou desenvolvendo com o objetivo de aplicar e consolidar conhecimentos avançados em engenharia de software, arquitetura de microsserviços, mensageria, deploy em nuvem, entre outros tópicos avançados de arquitetura e engenharia.

O objetivo final deste projeto é consolidar habilidades práticas essenciais para atuar em ambientes escaláveis, aproximando o projeto de contextos reais de produção em larga escala e por se tratar de um ambiente de estudos aprofundados e experimentação contínua, o código-fonte está mantido em um repositório privado, no entanto, compartilho aqui os objetivos, a arquitetura e o progresso atual do projeto.

<p align="center">
 <a href="#demonstração">Demonstração</a> •
 <a href="#funcionalidades">Funcionalidades</a> •
 <a href="#tecnologias-utilizadas">Tecnologias Utilizadas</a> •
 <a href="#-próximos-passos">Próximos Passos</a>
</p>

## Demonstração

![gifDemo](https://github.com/Jonas-Emir/conecta-showcase/blob/main/conecta-readme-demo.gif)

📽 Vídeos mais detalhados do projeto publicados no LinkedIn:

<p align="left">
  <a href="https://www.linkedin.com/feed/update/urn:li:activity:7318580236751724544/" target="_blank">
<img src="https://img.shields.io/badge/▶️%20Assistir%20Vídeo%20Parte%201-LinkedIn-%230077B5?style=for-the-badge&logo=linkedin" alt="Assistir Vídeo Completo no LinkedIn Autenticação"/>
  </a>
</p>

<p align="left">
  <a href="https://www.linkedin.com/feed/update/urn:li:activity:7341419503035060225/" target="_blank">
<img src="https://img.shields.io/badge/▶️%20Assistir%20Vídeo%20Parte%202-LinkedIn-%230077B5?style=for-the-badge&logo=linkedin" alt="Assistir Vídeo Completo no LinkedIn Autenticação"/>
  </a>
</p>

## Funcionalidades

- ✅ Sistema de autenticação (login e registro de usuários).
  - Suporte a login tradicional com e-mail e senha.
  - Integração com autenticação via Google (OAuth 2.0).
- ✅ Cadastro e edição de perfil do usuário.
  - O usuário pode gerenciar suas informações pessoais diretamente.
- ✅ Cadastro, exclusão e edição de serviços por usuários.
  - Cada usuário pode gerenciar os serviços que oferece, mantendo controle sobre suas informações.
- ✅ Página principal com listagem dos serviços.
  - Filtros por categoria, preço mínimo/máximo, região e busca por título.
  - Scroll infinito para melhor experiência de navegação.
  - Alternância entre visualização em lista ou cards.

 ## Tecnologias Utilizadas

- **Frontend:** Angular + TypeScript  
- **Backend:** ASP.NET Core com C#  
- **Comunicação entre serviços:** RabbitMQ (mensageria assíncrona)  
- **Containerização:** Docker para padronização e portabilidade dos ambientes  
- **Banco de Dados:** SQL Server 
- **Autenticação:** OAuth 2.0 com login social (Google) + login tradicional  
- **Outras tecnologias planejadas:** Kubernetes (orquestração), Microsserviços, CI/CD


## 🔄 Próximos Passos

Atualmente estou iniciando a estruturação da arquitetura de microsserviços para a próxima funcionalidade que será o sistema de favoritos, dividido em duas responsabilidades:

1.  **Microserviço de Favoritos**
    -   Persistirá os serviços favoritados por usuários.
    -   Publicará eventos no RabbitMQ indicando que um item foi favoritado.

2.  **Microserviço de Notificações**
    -   Escutará os eventos de favoritos no RabbitMQ.
    -   Enviará notificações em tempo real para os usuários.

Essa abordagem permite testar e validar uma arquitetura distribuída, *event-driven*, com comunicação assíncrona entre serviços desacoplados.
