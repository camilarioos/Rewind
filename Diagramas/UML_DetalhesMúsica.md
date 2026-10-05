```mermaid
sequenceDiagram
    actor Usuario as Usuário
    participant FrontEnd
    participant BackEnd
    participant BD as Banco de dados

    Usuario->>FrontEnd: Seleciona uma música
    FrontEnd->>BackEnd: Solicita os detalhes da música
    BackEnd->>BD: Consulta os dados da música
    BD-->>BackEnd: Retorna título, ano, artista e gênero
    BackEnd-->>FrontEnd: Envia os detalhes da música
    FrontEnd-->>Usuario: Exibe as informações da música
