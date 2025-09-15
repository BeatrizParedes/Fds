# Boas Práticas para Projetos de Software com Metodologias Ágeis (Scrum)

Este projeto apresenta diretrizes detalhadas para desenvolvimento de software em equipe usando **Scrum** e conceitos do livro *Engenharia de Software Moderna*. Destina-se a estudantes da disciplina **[Fundamentos de Desenvolvimento de Software](https://engsoftmoderna.info/)** e aborda organização, colaboração, controle de qualidade e entregas incrementais.

---

## 1️⃣ Planejamento Inicial

**Objetivo:** Garantir clareza de objetivos, responsabilidades definidas e backlog inicial.  

- **Definição do escopo:** Liste funcionalidades e requisitos, categorizando como essenciais, importantes e opcionais.  
- **Papéis da equipe (Scrum):**  
  - **Product Owner (PO):** Define prioridades, gerencia o backlog e garante que o projeto atenda às necessidades do usuário.  
  - **Scrum Master (SM):** Facilita o processo Scrum, remove impedimentos e garante que a equipe siga as práticas ágeis.  
  - **Development Team (Dev Team):** Implementa funcionalidades, realiza testes e mantém a qualidade do código.  
- **Ferramentas:** Kanban/Scrum Boards, reuniões diárias (Daily Standup), backlog atualizado.
  [<img width="1863" height="550" alt="image" src="https://github.com/user-attachments/assets/2994a252-f4e6-412b-8785-882d49308f2e" />
](https://trello.com/b/mhGgpLkc/kanban-quadro-modelo)

---
## Guia de GIT e GITHUB [clique aqui](git_github.md)
---

## 2️⃣ Cartões de Gestão Ágil

### 2.1 Cartão de Tarefa
- **Objetivo:** Registrar e acompanhar funcionalidades e atividades do projeto.  
- **Componentes:**  
  - Título da tarefa  
  - Descrição detalhada  
  - Responsável (membro do Development Team)  
  - Data de início e prazo  
  - Prioridade  
  - Status: *Backlog → Em andamento → Em revisão → Concluída*  
  - **Critérios de aceite:** Condições que a tarefa deve atender para ser considerada pronta (funcionalidade funcionando, testes aprovados, documentação atualizada).  

### 2.2 Cartão de Conversa
- **Objetivo:** Registrar discussões, dúvidas e decisões sobre tarefas específicas.  
- **Uso:**  
  - Comunicação centralizada entre Product Owner, Development Team e Scrum Master.  
  - Mantém histórico e decisões importantes relacionadas à tarefa.  

### 2.3 Cartão de Confirmação
- **Objetivo:** Validar se a tarefa foi concluída de acordo com os critérios de aceite.  
- **Uso:**  
  - QA ou Development Team revisa a tarefa.  
  - Confirma que todos os critérios de aceite foram atendidos.  
  - Move a tarefa para **Concluída**.  

---

## 3️⃣ Divisão de Etapas de Entrega (Sprints)

- **Planejamento da Sprint (Sprint Planning):**  
  - Selecionar tarefas do backlog.  
  - Dividir tarefas grandes em subtarefas.  
  - Definir critérios de aceite para cada tarefa.  

- **Execução da Sprint:**  
  - Desenvolvimento em **pair programming** (Driver e Navigator).  
  - Atualização de cartões de tarefa, conversa e confirmação.  
  - Pull Requests e revisões de código entre pares.  

- **Revisão da Sprint (Sprint Review):**  
  - Demonstração das funcionalidades desenvolvidas.  
  - Coleta de feedback do Product Owner e equipe.  

- **Retrospectiva da Sprint (Sprint Retrospective):**  
  - Identificação do que funcionou bem e do que precisa ser melhorado.  
  - Planejamento de melhorias para a próxima sprint.  

---

## 4️⃣ Issues e Bugs Tracker

- Registro de problemas e melhorias durante o desenvolvimento.  
- Cada issue deve conter: descrição, passos para reproduzir, responsável, prioridade e status.  
- Ferramentas recomendadas: [GitHub Issues](https://github.com/issues/assigned), Jira, Trello.  

---

## 5️⃣ Diagrama de Atividades

**Objetivo:** Visualizar o fluxo completo do projeto, desde planejamento até entrega e demonstração.  

**Elementos básicos:**
- **Estado inicial:** círculo sólido preto → início do processo.  
- **Atividades:** retângulos arredondados → ações ou tarefas.  
- **Decisões:** losangos → pontos de escolha no fluxo.  
- **Fluxo de controle:** setas → sequência das atividades.  
- **Estado final:** círculo com contorno externo → fim do processo.  
- **Swimlanes (opcional):** divisão das atividades por papéis Scrum.  

**Exemplo de fluxo de sprint (texto visual):**
<img width="1700" height="847" alt="image" src="https://github.com/user-attachments/assets/336db231-f6d4-4055-82d6-7958681e1a1d" />


---

## 6️⃣ Programação em Pares (Pair Programming)

- Dois desenvolvedores trabalham juntos:  
  - **Driver:** escreve o código.  
  - **Navigator:** revisa em tempo real e sugere melhorias.  
- Benefícios: menor incidência de bugs, qualidade de código superior e compartilhamento de conhecimento.  

---

## 7️⃣ Testes, Confirmação e Critérios de Aceite

No Scrum, os **critérios de aceite** são condições específicas que uma tarefa (ou **User Story**) deve cumprir para ser considerada concluída. Eles ajudam a equipe a ter clareza sobre o que significa "feito" e garantem que a funcionalidade atenda às expectativas do Product Owner e dos usuários.

### Como definir critérios de aceite

1. **Funcionalidade esperada**
   - Descreve o comportamento que a funcionalidade deve apresentar.
   - Exemplo: “O usuário deve conseguir criar uma conta com e-mail e senha válidos.”

2. **Casos de teste**
   - Listar cenários que comprovem que a funcionalidade funciona corretamente.
   - Exemplo:  
     - Tentar criar conta com e-mail já existente → deve exibir erro.  
     - Tentar criar conta com senha menor que 8 caracteres → deve exibir alerta.

3. **Regras de negócio**
   - Condições obrigatórias que o sistema deve seguir.
   - Exemplo: “A senha deve ter no mínimo 8 caracteres e incluir pelo menos um número.”

4. **Critérios não funcionais**
   - Desempenho, usabilidade, segurança ou compatibilidade.
   - Exemplo: “O tempo de resposta para criar a conta não pode ultrapassar 3 segundos.”

5. **Documentação e testes**
   - Garantir que documentação, testes automatizados ou manuais estejam atualizados.
   - Exemplo: “Manual do usuário atualizado com instruções de criação de conta.”

### Exemplo de Critérios de Aceite para uma User Story

**User Story:** Como usuário, quero me cadastrar no sistema para acessar minhas informações.

**Critérios de Aceite:**
- O usuário consegue criar conta com e-mail válido e senha ≥ 8 caracteres.  
- Mensagens de erro aparecem quando e-mail já existe ou senha é inválida.  
- A senha é armazenada de forma segura (hash).  
- Tempo de resposta ≤ 3 segundos.  
- Documentação atualizada e testes unitários criados.

### No Kanban Scrum

- QA ou **Development Team** valida tarefas usando o **cartão de confirmação**.  
- Apenas tarefas que cumprem todos os **critérios de aceite** são movidas para **Concluída**.  
- Isso garante **qualidade**, **consistência** e **clareza** sobre o que significa “pronto”.

---

## 8️⃣ Deploy e Demonstração de Telas

- **Deploy:** Publicação em ambiente de teste ou produção [(Vercel](https://vercel.com/prisma-b3f7426a), [GitHub Pages](https://docs.github.com/pt/pages), etc.).  
- **Demonstração de telas:** Apresentação das funcionalidades, incluindo prints, vídeos ou demonstração ao vivo para feedback.  

---

## 9️⃣ Fluxo Completo do Projeto

1. Planejamento do backlog pelo Product Owner.  
2. Criação de cartões de tarefa com critérios de aceite.  
3. Desenvolvimento em pair programming pelo Development Team.  
4. Registro de conversas no cartão de conversa.  
5. Testes e QA usando cartão de confirmação.  
6. Correção de bugs e atualização de issues.  
7. Deploy em ambiente de teste ou produção.  
8. Demonstração de telas e coleta de feedback.  
9. Confirmação de conclusão de tarefas.  
10. Retrospectiva e planejamento da próxima sprint.  

---

## 1️⃣0️⃣ Referências

- Pressman, R. S. (2016). *Engenharia de Software Moderna* (8ª edição). McGraw-Hill Education.  
- Beck, K. (2000). *Extreme Programming Explained: Embrace Change*. Addison-Wesley.  
- Schwaber, K. & Sutherland, J. (2020). *The Scrum Guide*. Scrum.org  

---

 **Resumo final:**  
Seguindo estas práticas com os papéis do Scrum, a equipe consegue desenvolver software de forma colaborativa, organizada e iterativa, garantindo entregas contínuas, qualidade e rastreabilidade de todas as tarefas.
