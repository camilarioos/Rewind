```mermaid
sequenceDiagram
    actor Usuario as Usuário
    participant FrontEnd
    participant BackEnd
    participant BD as Banco de dados

    Usuario->>FrontEnd: Acessa "Minha Cápsula"
    FrontEnd->>BackEnd: Solicita os favoritos do usuário
    BackEnd->>BD: Consulta músicas favoritas
    BD-->>BackEnd: Retorna lista de músicas favoritas
    BackEnd-->>FrontEnd: Envia os favoritos
    FrontEnd-->>Usuario: Exibe as músicas salvas na Minha Cápsula
