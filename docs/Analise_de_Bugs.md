# Análise e Classificação de Bugs


### Bug 1: Quiz publicado pelo professor não é visível para o aluno

-   **Tipo**: Lógico
-   **Local Plausível**:
    -   Front-end: Na página que lista os quizzes para o aluno em quizaluno.jsx.
    -   Back-end: Na `view` da API que retorna a lista de quizzes disponíveis para um aluno.
-   **Descrição**: Um quiz que foi criado e devidamente publicado pelo professor não está sendo exibido na área de atividades do aluno. O problema provavelmente está na lógica de consulta do back-end, que não está filtrando ou retornando corretamente os quizzes que deveriam estar visíveis para o perfil do aluno.

---

### Bug 2: Não é possível fazer login como professor

-   **Tipo**: Lógico
-   **Local Plausível**:
    -   Front-end: `Login.jsx`
    -   Back-end: `usuarios/views.py`
-   **Descrição**: Na página de `Login.jsx`, um usuário com credenciais corretas e perfil de "professor" tenta fazer login. Apesar dos dados estarem certos, o sistema retorna uma mensagem de "Usuário ou senha inválidos". O problema reside na lógica do back-end, no arquivo `usuarios/views.py`, que não está validando corretamente o perfil "professor".

---

### Bug 3: E-mail de recuperação de senha não é enviado

-   **Tipo**: Runtime (Erro em tempo de execução)
-   **Local Plausível**:
    -   Front-end: `RecuperarSenha.jsx`
    -   Back-end (Lógica): `usuarios/views.py`
    -   Back-end (Configuração): `backend/settings.py`
-   **Descrição**: O usuário acessa a página `RecuperarSenha.jsx` e solicita a recuperação. A interface exibe uma mensagem de sucesso, mas o e-mail nunca chega. A falha ocorre no back-end devido a uma configuração incorreta do serviço de envio de e-mails (SMTP) no arquivo `backend/settings.py`.

### Bug 2: Não é possível fazer login como professor

-   **Tipo**: Lógico
-   **Local Plausível**:
    -   Front-end: `Login.jsx`
    -   Back-end: `usuarios/views.py`
-   **Descrição**: Na página de `Login.jsx`, um usuário com credenciais corretas e perfil de "professor" tenta fazer login. Apesar dos dados estarem certos, o sistema retorna uma mensagem de "Usuário ou senha inválidos". O problema reside na lógica do back-end, no arquivo `usuarios/views.py`, que não está validando corretamente o perfil "professor", tratando-o como inválido.

---

### Bug 3: E-mail de recuperação de senha não é enviado

-   **Tipo**: Runtime (Erro em tempo de execução)
-   **Local Plausível**:
    -   Front-end: `RecuperarSenha.jsx`
    -   Back-end (Lógica): `usuarios/views.py`
    -   Back-end (Configuração): `backend/settings.py`
-   **Descrição**: O usuário acessa a página `RecuperarSenha.jsx` e solicita a recuperação. A interface exibe uma mensagem de sucesso, mas o e-mail nunca chega. A falha ocorre no back-end devido a uma configuração incorreta do serviço de envio de e-mails (SMTP) no arquivo `backend/settings.py`, causando um erro de autenticação em tempo de execução no servidor que não é comunicado ao usuário.

