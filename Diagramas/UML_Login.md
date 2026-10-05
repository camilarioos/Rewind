# UML - Tela de Login

```mermaid
sequenceDiagram
    actor Usuario as Usuário
    participant FrontEnd
    participant BackEnd
    participant BD as Banco de dados

    Usuario->>FrontEnd: Informa e-mail e senha e clica em "Entrar"
    FrontEnd->>BackEnd: Envia as credenciais para autenticação
    BackEnd->>BD: Consulta usuário pelo e-mail
    BD-->>BackEnd: Retorna os dados do usuário

    alt Credenciais válidas
        BackEnd-->>FrontEnd: Confirma a autenticação
        FrontEnd-->>Usuario: Redireciona para a tela inicial
    else Credenciais inválidas
        BackEnd-->>FrontEnd: Retorna erro de autenticação
        FrontEnd-->>Usuario: Exibe mensagem de erro
    end
