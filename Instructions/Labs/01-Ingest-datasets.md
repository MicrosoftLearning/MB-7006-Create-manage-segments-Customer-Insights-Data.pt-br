---
lab:
  title: 'Laboratório 1: Ingerir conjuntos de dados'
---

# Laboratório 1: Ingerir conjuntos de dados
Neste laboratório, você aprenderá a:
- Trazer vários conjuntos de dados usando o PowerQuery
- Transformar conjuntos de dados e alterar tipos de coluna
- Monitorar o status da importação

Para criar segmentos, primeiro precisamos importar os dados que usaremos em nossos segmentos. Neste laboratório, importaremos alguns conjuntos de dados como pré-requisito para unificar os dados e criar nossos segmentos.

## Exercício 1: Ingerir fontes de dados
Para este projeto guiado, você precisará importar várias fontes de dados. Essas fontes de dados serão usadas na criação dos perfis unificados de cliente.

### Tarefa 1: Ingerir dados do cliente a partir da plataforma de comércio eletrônico
1. No **Customer Insights - Data**, expanda **Dados** no menu de navegação esquerdo e selecione **Fontes de Dados**.

1. Selecione **+ Adicionar uma fonte de dados**. Veja os métodos disponíveis de ingestão de dados. Para este laboratório, escolha **Microsoft Power Query**, nomeie a fonte como **Comércio eletrônico** e clique em **Avançar**.

1. Você verá uma tela com as **fontes de dados do Power Query** que o **Customer Insights** pode ingerir. Anote os tipos de conectores disponíveis. Selecione o conector **Texto/CSV**.

1. Insira `https://aka.ms/CI-ILT/Contacts` em **Caminho do arquivo ou URL** e clique em **Avançar**. Pode demorar um pouco para que os dados carreguem.

1. Agora você deve ver os dados da fonte tabulados. Selecione **Transformar dados** para configurar os tipos e formatos dos dados que serão ingeridos.

1. Você observará que o cabeçalho da coluna foi mostrado na primeira linha dos dados. Para corrigir isso, selecione **Transformar > Usar a primeira linha como cabeçalhos** na guia **Página Inicial** ou selecione a guia **Transformar** e, em seguida, **Usar a primeira linha como cabeçalhos**.

1. Como ingerimos os dados de uma **fonte de Texto/CSV**, todas as colunas são padronizadas como o **Tipo de dados** "Texto". Para ingerir e modelar os dados com êxito, podemos definir o tipo de dados como colunas que não são de texto.

1. Para alterar o tipo de dados, selecione o ícone **ABC** no título de cada coluna. Atualize o tipo de dados das colunas:
    - **DateOfBirth**: Data
    - **CreatedOn:** Data
    - **Income:** Moeda

1. Verifique se o campo **Nome** no painel **Configurações de consulta** está definido como **Contatos**. Selecione **Avançar**.

1. Selecione **Atualizar manualmente** e, em seguida, **Salvar**.

Parabéns. Você criou sua primeira fonte de dados com um conjunto de dados. Continuaremos importando o próximo conjunto de dados na próxima tarefa.

### Tarefa 2: Ingerir dados do cliente a partir do esquema de fidelidade
1. No **Customer Insights**, expanda **Dados** no menu à esquerda e selecione **Fontes de dados**.

1. Clique em **+Adicionar uma Fonte de Dados** e escolha **Microsoft Power Query** como o método de importação. Nomeie a fonte como **Lealdade** e clique em **Avançar**.

1. Selecione o conector **Texto/CSV**.

1. Insira `https://aka.ms/CI-ILT/LoyaltySchemeCustomers` em **Caminho do arquivo ou URL**, clique em **Avançar** e, em seguida, em **Transformar dados**.

1. Como antes, selecione **Transformar** e, em seguida, **Usar a primeira linha como cabeçalhos**.

1. Atualize o tipo de dados das colunas:
    - **DateOfBirth**: Data
    - **RewardPoints**: Número inteiro
    - **CreatedOn:** Data

1. Renomeie essa consulta como **Clientes** no painel **Configurações de consulta** e clique em **Avançar**.

1. Selecione **Atualizar manualmente** e, em seguida, **Salvar**.

### Tarefa 3: Ingerir dados do cliente a partir de compras no ponto de venda
1. No **Customer Insights**, expanda **Dados** no menu de navegação esquerdo e selecione **Fontes de Dados**.

1. Selecione **+ Adicionar uma fonte de dados**, escolha **Microsoft Power Query** e nomeie o **PoS** de origem e clique em **Avançar**.

1. Selecione o conector **Texto/CSV**.

1. Digite `https://aka.ms/CI-ILT/POSPurchases` em **Caminho do arquivo ou URL**. Clique em **Avançar** e **Transformar dados**.

1. Como antes, selecione **Transformar** e, em seguida, **Usar a primeira linha como cabeçalhos**.

1. Atualize o tipo de dados das colunas:
    - **PurchasedOn:** Data
    - **TotalPrice**: Moeda
    - **RewardPointsAdded:** Número inteiro

1. No campo **Nome** do painel **Configurações da consulta**, renomeie a consulta para **Compras**.

1. Selecione **Avançar**.

1. Escolha **Atualizar manualmente** e selecione **Salvar**.

### Tarefa 4: Ingerir dados de compras online
1. Nesta tarefa, você vai ingerir os dados de **compras online**, que representam as compras feitas no site da **Contoso Coffee**.

1. No **Customer Insights**, expanda **Dados** no menu à esquerda e selecione **Fontes de dados**. (Certifique-se de que o status da fonte de dados **Comércio eletrônico** seja **Êxito**.)

1. Selecione o conjunto de dados **Comércio eletrônico** que você criou na primeira tarefa e selecione **Editar**. (Se os seus dados ainda estiverem sendo atualizados, você precisará aguardar a conclusão antes de editar.)

1. Selecione **Avançar**. 

1. Você verá a tela do **Power Query** com os dados dos **Contatos de Comércio eletrônico** ingeridos na Tarefa 1. Na guia **Página Inicial**, selecione **Obter dados**.

1. Você verá uma tela com os conectores de fonte de dados que o **Customer Insights** pode ingerir. Selecione **Texto/CSV**.

1. Insira `https://aka.ms/CI-ILT/OnlinePurchases` em **Caminho do arquivo ou URL** e clique em **Avançar**. Selecione **Criar**.

1. Como antes, selecione **Transformar** e, em seguida, **Usar a primeira linha como cabeçalhos**.

1. Atualize os tipos de dados para as seguintes colunas:
    - **PurchasedOn:** Data
    - **TotalPrice**: Moeda

1. Nomeie essa consulta como **Compras** e clique em **Salvar**.

**Importante:** você terá que aguardar que o status de todas as suas fontes de dados seja **Êxito** antes de avançar para o próximo exercício.
