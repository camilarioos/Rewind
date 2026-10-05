```mermaid
sequenceDiagram
    actor Usuario as Usuário
    participant FrontEnd
    participant BackEnd
    participant BD as Banco de dados

    Usuario->>FrontEnd: Acessa a tela "Explorar"
    FrontEnd->>BackEnd: Solicita as músicas disponíveis
    BackEnd->>BD: Consulta músicas cadastradas
    BD-->>BackEnd: Retorna as músicas
    BackEnd-->>FrontEnd: Envia a lista de músicas
    FrontEnd-->>Usuario: Exibe as músicas disponíveis
