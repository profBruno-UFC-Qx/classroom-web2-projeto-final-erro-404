# 🏁 CinePrime

O CinePrime é uma aplicação web completa para gestão de cinemas, permitindo que usuários visualizem filmes disponíveis, comprem ingressos e que administradores gerenciem salas, sessões e funcionários.

# 🧑‍💻 Membros da equipe

- 542646, Hyarlei Silva Freitas, Sistemas de Informação.

# 💡 Objetivo Geral

Desenvolver uma aplicação web robusta e intuitiva para a gestão completa de um cinema, otimizando tanto a experiência do cliente final quanto as operações administrativas internas do estabelecimento.

# 👀 Público-Alvo

O projeto destina-se a dois grupos principais:

    1.  **Clientes de Cinema:** Usuários que desejam consultar a programação de filmes, obter detalhes sobre as sessões e comprar ingressos de forma rápida e online.
    2.  **Administradores/Funcionários do Cinema:** Equipe interna que necessita de uma ferramenta centralizada para gerenciar as operações do dia-a-dia, como cadastro de salas, agendamento de sessões e gerenciamento de funcionários.

# 🌟 Impacto Esperado

Para os **Clientes**, espera-se uma melhoria significativa na experiência de compra, facilitando o acesso à informação e reduzindo o tempo de espera em filas.

Para a **Administração do Cinema**, o projeto visa centralizar e automatizar processos, melhorar a eficiência operacional, reduzir erros manuais no agendamento de sessões e fornecer um controle claro sobre as transações e o gerenciamento da equipe.

# 🧑‍🤝‍🧑 Papéis ou tipos de usuário da aplicação

A aplicação possui três tipos principais de usuários:

    1.  **Visitante (Usuário Não Logado):** Pode navegar pelo site, visualizar a lista de filmes em cartaz e ver os detalhes de cada filme e sessão (horários, salas, sinopse).
    2.  **Cliente (Usuário Logado):** Além de todas as permissões do Visitante, pode realizar a compra de ingressos e visualizar seu histórico de compras.
    3.  **Administrador (Logado):** Possui acesso a um painel administrativo restrito onde pode gerenciar (CRUD) salas, sessões e funcionários, além de visualizar todas as transações de vendas.

# 🚩 Principais funcionalidades da aplicação

### Funcionalidades Públicas (Acessíveis a todos)

- Visualizar lista de filmes em cartaz.
- Ver detalhes de filmes específicos (sinopse, duração, classificação).
- Consultar horários e salas das sessões disponíveis.

### Funcionalidades Restritas (Requerem autenticação)

**Para Clientes (Logados):**

- Autenticação (Login/Cadastro).
- Realizar a compra de ingressos para uma sessão.
- Visualizar o histórico de compras pessoais.
- Gerenciar dados do seu perfil.

**Para Administradores (Logados):**

- Dashboard com visão geral das vendas e operações.
- Gerenciamento completo (CRUD) de Salas de cinema.
- Gerenciamento completo (CRUD) de Sessões (agendamento de filmes, definição de preços).
- Gerenciamento de Funcionários/Administradores.
- Visualização de todas as transações de ingressos vendidos.

# 🗓️ Entidades ou tabelas do sistema

Com base nas funcionalidades, as principais entidades (que se traduzem em tabelas no banco de dados) são:

- **Usuario** (Para armazenar dados de Clientes e Administradores, diferenciados por um campo de "tipo" ou "role").
- **Filme** (Armazena título, sinopse, duração, pôster, etc.).
- **Sala** (Armazena o nome/número da sala e sua capacidade total).
- **Sessao** (Entidade que liga um `Filme` a uma `Sala` em uma data e horário específicos, contendo também o preço).
- **Ingresso** (Registra um assento comprado por um `Usuario` para uma `Sessao` específica).
- **Transacao** (Pode ser usada para agrupar múltiplos `Ingressos` em uma única compra/pagamento).
