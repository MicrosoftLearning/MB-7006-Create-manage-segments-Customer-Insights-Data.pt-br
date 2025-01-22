---
lab:
  title: 'Laboratório 2: Criar perfis de cliente unificados'
---

# Laboratório 2: Criar perfis de cliente unificados
Neste laboratório, você aprenderá a:
- Mesclar dados das fontes de dados brutos em um perfil de cliente
- Selecionar uma chave primária 
- Criar regras de correspondência
- Definir índices e atividades de pesquisa e filtro

O objetivo é descobrir quantos perfis de cliente exclusivos a **Contoso Retail** tem em várias fontes de dados.

## Exercício 1: Unificar os dados
### Tarefa 1: Mapear contatos para tipos de dados comuns
1. Entre no **Customer Insights - Data**.

1. No painel de navegação à esquerda, expanda **Dados** e selecione **Unificar**. Selecione **Introdução**.

1. Escolha **Selecionar tabelas e colunas**.

1. Selecione as tabelas que representam o perfil do cliente – **Contatos (Comércio eletrônico)** e **Clientes (Lealdade)**. Escolha **Aplicar**.

1. Agora você verá os mapeamentos da tabela de origem referentes aos tipos de modelo padrão. É possível examinar os tipos na tabela.

1. Escolha uma **"Chave primária"** para cada entidade que foi ingerida. A chave primária deve ser uma referência exclusiva. Para **Contatos de comércio eletrônico**, selecione **ContactId** como a chave primária.

1. Os dados dos **Contatos de comércio eletrônico** contêm uma coluna chamada **Assinante de email** que será mapeada para um tipo incorreto, **Identity.Service.Email**, devido ao nome. Abra o menu suspenso desta coluna e selecione a opção vazia (nada/em branco). Se não fizermos isso, o comportamento padrão do sistema é mesclar esse campo com o campo **Email**, o que não queremos.

1. Selecione **Lealdade dos clientes** em **Tabelas** e defina **LoyaltyId** como a chave primária.

1. Selecione **Salvar colunas de origem** no canto superior esquerdo.

1. Clique no botão **Avançar** e **Avançar** novamente para ignorar a verificação de duplicatas e passar para a etapa **Regras de correspondência**.

### Tarefa 2: Especificar ordem de correspondência
No próximo estágio, você deve selecionar a ordem na qual mesclar os perfis. Você poderá mesclar atributos para garantir que os perfis unificados estejam completos e definir a prioridade das fontes que serão usadas para esses atributos.

1. Você deve selecionar a fonte de perfil mais completa ou precisa como a **Fonte primária (primeira)**. Verifique se **Contatos: comércio eletrônico** é a fonte primária (primeira).

1. Verifique se **Clientes: Fidelidade** é a segunda fonte na lista. 

1. Verifique se a opção **Incluir todos os registros** está marcada para ambas as fontes de dados.

### Tarefa 3: criar uma regra de correspondência
1. Há um indicador de aviso na linha **Clientes: Fidelidade**. Selecione **+ Adicionar regra**.

1. Adicione sua primeira condição usando **FullName**:
    - Na tabela **Contatos: comércio eletrônico**, selecione o campo **FullName**.
    - Na tabela **Clientes: Fidelidade**, selecione o campo **FullName**.
    - Deixe o menu suspenso **Normalizar** em branco.
    - Defina o **Nível de Precisão** como **Básico**.
    - Defina o **Valor de Precisão** como **Exato** usando o controle deslizante.
    - Insira o nome **FullName, Email** para o **Nome da regra**.

1. Adicione uma segunda condição para o endereço de email clicando em **+ Adicionar** e escolhendo **Adicionar condição**.
    - Na tabela **Contatos: comércio eletrônico**, selecione o campo **Email**.
    - Na tabela **Clientes: Fidelidade**, selecione o campo **Email**.
    - Deixe o menu suspenso **Normalizar** em branco.
    - Defina o **Nível de Precisão** como **Básico**.
    - Defina o **Valor de Precisão** como **Exato**.

1. Selecione **Concluído**.

1. Selecione **Avançar**.

1. Não faremos nenhuma alteração na tela **Exibição de dados unificados**. Selecione **Avançar** para passar para a tela de revisão.

1. Na tela **Revisão**, selecione **Criar perfis de cliente**. Agora, o Customer Insights está fazendo a correspondência dos dados dos clientes com base em todas as fontes de informações dos clientes para identificar quantos perfis de clientes exclusivos você tem com base nas suas regras. Pode levar algum tempo para criar os perfis.

Parabéns! Você unificou os dados de várias fontes no **Customer Insights** para criar um **Perfil unificado de cliente** que pode ser usado para obter insights de toda a sua base de clientes.

## Exercício 2: Configurar índices e atividades de pesquisa e filtro
Neste exercício, configuraremos os critérios de **pesquisa e filtro** para permitir que os usuários do Customer Insights pesquisem perfis unificados do cliente. Depois, configuraremos as atividades.

### Tarefa 1: Configurar colunas de pesquisa e índices de filtro 
1. No **Customer Insights**, selecione **Clientes** no menu de navegação à esquerda.

1. Selecione **Pesquisar e filtrar índice.** Alguns campos já são adicionados por padrão. Selecione **+ Adicionar** na barra de ferramentas.

1. Selecione **CustomerId, FirstName, LastName, FullName, DateOfBirth, EMail, PostCode, ContactId (eCommerce_Contacts) e LoyaltyId** (se não estiverem selecionados). Desmarque todos os outros campos marcados. Escolha **Aplicar**.

1. Selecione **Salvar**.

1. Selecione **Executar**.

1. No **Customer Insights**, selecione **Clientes** no menu de navegação à esquerda. Você verá um conjunto de cartões de cliente, representando os **Perfis Unificados**. Você pode expandir os cartões para ver mais sobre o cliente ou classificá-los por vários campos. Tente isso clicando em **Expandir cartões** e **Classificar por** na barra de ferramentas.

1. Você pode usar **Pesquisar clientes** para pesquisar atributos de texto relacionados a perfis unificados de cliente. Por exemplo, Pesquisar "1" pesquisará todos os atributos de texto e retornará correspondências e correspondências parciais).

### Tarefa 2: Criar atividades
1. No **Customer Insights**, expanda **Dados > Atividades** no menu de navegação à esquerda e selecione **+ Configurar atividades**.

1. Clique em **Selecionar tabelas**.

1. Selecione as tabelas **Compras: Comércio eletrônico** e **Compras: PDV** e selecione **Adicionar**.

1. Em **Compras: Comércio eletrônico**, configure da seguinte maneira:
    - Defina o **Tipo de atividade** como **SalesOrder**.
    - Defina a **Chave primária** como **PurchaseId**.

1. Em **Compras: PDV**, configure da seguinte maneira:
    - Defina o **Tipo de atividade** como **SalesOrder**.
    - Defina a **Chave primária** como **PurchaseId**.

1. Selecione **Avançar**.
   
1. Configure **Comércio eletrônico: Compras** da seguinte maneira:
    - Insira **OnlinePurchase** em **Nome da atividade**.
    - Preencha os seguintes campos (para quaisquer campos não mencionados, deixe em branco):
        - **Timestamp**: PurchasedOn
        - **Atividade do evento**: ActivityTypeDisplay
        - **Detalhe adicional**: Assunto
        - **Mostrar esta atividade na linha do tempo do perfil do cliente?** Sim
        - **Ícone**: Selecione sacola de compras.
        - **Definir tipos de campo de mapa para os atributos da sua atividade?** Sim e configurar da seguinte maneira:
            - **ID da ordem de venda**: PurchaseID
            - **Data da ordem**: PurchasedOn
            - **Valor da venda**: TotalPrice

1. Configure **PDV: Compras** da seguinte maneira:
    - Insira **PoSPurchase** em **Nome da atividade**.
    - Preencha os seguintes campos (para quaisquer campos não mencionados, deixe em branco):
        - **Timestamp**: PurchasedOn
        - **Atividade do evento**: ActivityTypeDisplay
        - **Detalhe adicional**: Assunto
        - **Mostrar esta atividade na linha do tempo do perfil do cliente?** Sim
        - **Ícone**: Selecione sacola de compras.
        - **Definir tipos de campo de mapa para os atributos da sua atividade?** Sim e configurar da seguinte maneira:
            - **ID da ordem de venda**: PurchaseID
            - **Data da ordem**: PurchasedOn
            - **Valor da venda**: TotalPrice

1. Selecione **Avançar**.

1. Na tela **Configurar relacionamentos da atividade**, com **Comércio eletrônico: Compras** selecionado, selecione **+ Adicionar relacionamento**.

1. No painel **Adicionar caminho de relacionamento**, defina os seguintes valores:
    - **Chave estrangeira**: ContactId
    - **Para o nome da tabela**: Contatos: Comércio eletrônico
    - **Nome do relacionamento**: eCommPurchasesToContacts
    - Escolha **Aplicar**.

1. Selecione **PDV: Compras**. Selecione **+ Adicionar relação**.

1. No painel **Adicionar caminho de relacionamento**, defina os seguintes valores:
    - **Chave estrangeira**: LoyaltyId
    - **Para o nome da tabela**: Clientes: Fidelidade
    - **Nome do relacionamento**: PoSPurchasesToLoyalty
    - Escolha **Aplicar**.

1. Selecione **Avançar**.

1. Selecione **Criar atividades**.

1. Aguarde enquanto as **Atividades** são atualizadas e unificadas.



