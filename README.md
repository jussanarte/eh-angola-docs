# EH.Angola — Economia com História Angola

> Uma plataforma educativa digital que contextualiza o ensino da 
> economia na realidade histórica e cultural angolana, através de 
> conteúdo, quizzes interativos e comunidade académica.

---

## Sobre o Projeto

A educação económica em Angola enfrenta um paradoxo: apesar de o país 
ter uma história económica rica e complexa — marcada pela exploração 
colonial, pela transição pós-independência, pelas reformas monetárias 
e pela dependência petrolífera — os estudantes universitários 
dispunham de poucas plataformas digitais que ligassem esse percurso 
histórico aos conceitos económicos ensinados em sala de aula.

O **EH.Angola** nasceu para responder a essa lacuna: uma plataforma 
que combina conteúdo editorial (artigos, vídeos, podcasts), avaliação 
formativa através de quizzes gerados com apoio de Inteligência 
Artificial, um fórum de discussão académica moderado, e um sistema de 
gamificação (Jindungo) — tudo ancorado na realidade angolana.

O projeto foi desenvolvido no âmbito da Unidade Curricular de 
**Engenharia de Software II**, do curso de Engenharia Informática do 
**ISPTEC** (Instituto Superior Politécnico de Tecnologias e Ciências), 
sob orientação do professor **Judson Paiva**.

---

## Arquitetura

O sistema é composto por três repositórios independentes, todos a 
consumir a mesma API pública:

| Componente | Descrição | Repositório |
|---|---|---|
| 🔧 **Backend (API)** | Laravel 12 · MySQL · Autenticação (Sanctum) · Tempo real (Reverb) · Geração de quizzes por IA | [link do repo do backend] |
| 🌐 **Aplicação Web** | Interface web que consome a API pública | [link do repo web] |
| 📱 **Aplicação Mobile** | Flutter/Dart · consome a mesma API partilhada com a web | [link do repo mobile] |

A escolha de uma API única partilhada entre as duas aplicações cliente 
garante que a lógica de negócio, as regras de autorização e o modelo 
de dados existem numa única fonte de verdade, evitando duplicação de 
comportamento entre plataformas.

---

## Funcionalidades Principais

- 📰 **Feed de Conteúdo** — artigos, vídeos e podcasts, com pesquisa, 
  categorização e comentários.
- 🧠 **Quiz Interativo** — criação manual ou assistida por IA, com 
  feedback pedagógico imediato e ranking global e por quiz.
- 💬 **Fórum de Discussão** — tópicos públicos e privados, com 
  moderação e atualização em tempo real.
- 🏆 **Gamificação (Jindungo)** — sistema de pontuação e ranking por 
  período (semanal, mensal, geral).
- 🔔 **Notificações em Tempo Real** — via WebSocket, para interações, 
  aprovações e novas publicações.
- 👥 **Modelo de Papéis Granular** — Membro, Escritor, Admin e 
  Administrador, com permissões calculadas centralmente pela API.

---

## Stack Tecnológica

- **Backend:** Laravel 12 (PHP 8.4)
- **Base de Dados:** MySQL
- **Autenticação:** Laravel Sanctum, Google OAuth
- **Tempo Real:** Laravel Reverb
- **Armazenamento de Media:** Cloudinary
- **Email Transacional:** Brevo
- **Inteligência Artificial:** Anthropic API (geração de quizzes)
- **Aplicação Móvel:** Flutter / Dart
- **Infraestrutura:** Railway

---

## Equipa

Projeto desenvolvido por estudantes do curso de Engenharia Informática 
do ISPTEC, no âmbito da disciplina de Engenharia de Software II:

| Nome | Nº de Matrícula | Papel no Projeto |
|---|---|---|
| Isabel Marques | 20231238 | Backend & Integração |
| Jussana Paim | 20230132 | UI/UX Design |
| Norberto Cassoma | 20230873 | Desenvolvimento Web |
| Oldmar Filindo | 20231359 | Desenvolvimento Mobile |

**Orientador:** Prof. Judson Paiva

---

## Estado do Projeto

O sistema encontra-se implantado em ambiente de produção, com os 
módulos de Autenticação, Fórum, Quiz e Conteúdo (incluindo artigos, 
vídeos e podcasts) totalmente operacionais nas versões web e mobile. 
Consultar o relatório final do projeto para detalhes completos sobre 
requisitos, arquitetura e trabalhos futuros.

---

## Licença Académica

Este projeto foi desenvolvido para fins académicos, no âmbito da 
avaliação da disciplina de Engenharia de Software II do ISPTEC, e não 
possui licença de uso comercial associada.
