```mermaid
sequenceDiagram
    actor Usuario as Usuário
    participant FrontEnd
    participant BackEnd
    participant BD as Banco de dados

    Usuario->>FrontEnd: Informa nome, e-mail e senha
    Usuario->>FrontEnd: Clica em "Criar conta"
    FrontEnd->>BackEnd: Envia os dados do cadastro
    BackEnd->>BD: Verifica se o e-mail já está cadastrado
    BD-->>BackEnd: Retorna resultado da consulta
    BackEnd->>BD: Cadastra novo usuário
    BD-->>BackEnd: Confirma o cadastro
    BackEnd-->>FrontEnd: Retorna confirmação
    FrontEnd-->>Usuario: Exibe mensagem de sucesso
