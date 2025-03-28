---
lab:
  title: 'Laboratório 3: Criar medidas'
---

# Laboratório 3: Criar medidas

Neste laboratório, você aprenderá a:
- Defina medidas de negócios para acompanhar o desempenho e a integridade dos negócios
- Defina medidas do cliente para obter insights sobre clientes individuais

## Exercício 1: Definir medidas e atributos
### Tarefa 1: Valor médio das compras na loja
Nesta primeira tarefa, criaremos uma medida para definir o valor médio de todas as compras na loja feitas na **Contoso Coffee**.

1. Expanda **Insights** e selecione **Medidas** no menu de navegação à esquerda.

1. Selecione **+ Nova** na barra de ferramentas e, em seguida, selecione **Criar a sua**.

1. Selecione **Editar detalhes** ao lado do texto do cabeçalho **Medida sem título**.

1. Defina o **Nome** como **Valor médio de compras na loja (US$)** e selecione **Concluído**.

1. Alterne o **Tipo de medida** de **Cliente** para **Empresarial**.

1. Ao lado de **Cálculo 1**, selecione **Editar nome**.

1. Defina o **Nome** como **Valor médio de compra na loja (US$)**.

1. Verifique se o **Nome do atributo de saída** está definido como **AverageStorePurchaseValue**.

1. Selecione **Concluído**.

1. No cálculo **Valor médio de compra na loja (US$)**, escolha **Média** no menu suspenso **Selecionar função**.

1. Selecione **+ Adicionar atributo**, expanda **Compras: PDV** e selecione **TotalPrice**.

1. Selecione **Adicionar**.

1. Clique no botão **Executar** para concluir a medida.

    Nesta próxima tarefa, criaremos uma medida para definir o valor médio de todas as compras na Web feitas na **Contoso Coffee**.

1. Selecione **Insights > Medidas** no menu de navegação à esquerda.

1. Selecione **+ Nova > Criar a sua** na barra de ferramentas.

1. Selecione **Editar detalhes** ao lado do texto do cabeçalho **Medida sem título**.

1. Defina o **Nome** como **Valor médio de compra na Web (US$)** e selecione **Concluído**.

1. Alterne o **Tipo de medida** de **Cliente** para **Empresarial**.

1. Ao lado de **Cálculo 1**, selecione **Editar nome**.

1. Defina o **Nome** como **Valor médio de compra na Web (US$)**.

1. Verifique se o **Nome do atributo de saída** está definido como **AverageWebPurchaseValue**.

1. Selecione **Concluído**.

1. No cálculo **Valor médio de compra na Web (US$)**, escolha **Média** no menu suspenso **Selecionar função**.

1. Selecione **+ Adicionar atributo**, expanda **Compras: Comércio eletrônico** e selecione **TotalPrice**.

1. Selecione **Adicionar**.

1. Clique no botão **Executar** para concluir a medida.

### Tarefa 2: Definir medidas do cliente
Precisaremos de duas medidas de cliente que possam ser usadas para calcular um atributo do cliente. Criaremos uma medida para determinar o gasto total dos clientes em **Compras online** e uma medida para determinar o gasto total em **Compras na loja**. Depois de criá-las, podemos criar um atributo de cliente para somar as duas.

Nesta tarefa, criaremos uma medida para definir o total de todas as compras feitas na loja.

1. Selecione **Insights > Medidas** no menu de navegação à esquerda.

1. Selecione **+ Nova > Criar a sua** na barra de ferramentas.

1. Selecione **Editar detalhes** ao lado do texto do cabeçalho **Medida sem título**.

1. Defina o **Nome** como **Total de gastos na loja** e selecione **Concluído**.

1. No cálculo **Total de gastos na loja**, escolha **Soma** no menu suspenso **Selecionar função**.

1. Selecione **+ Adicionar atributo**, expanda **Compras: PDV**, selecione **TotalPrice** e selecione **Adicionar**.

1. Para configurar o cálculo da medida, selecione **Dimensões (1)**.

1. Selecione **Editar Dimensões**.

1. Expanda **Compras: PDV**, selecione **LoyaltyId** e selecione **Concluído**.

1. Escolha **Aplicar**.

1. Clique no botão **Executar** para concluir a medida. Se você encontrar um erro e precisar escolher o **Caminho do relacionamento**, selecione **PoS_Purchases > Cliente** e clique no botão **Executar** para concluir.

    A seguir, criaremos uma medida para definir o total de todas as compras feitas online.

1. Selecione **Insights > Medidas** no menu de navegação à esquerda.

1. Selecione **+ Nova > Criar a sua** na barra de ferramentas.

1. Selecione **Editar detalhes** ao lado do texto do cabeçalho **Medida sem título**.

1. Defina o **Nome** como **Total de gastos online** e selecione **Concluído**.

1. No cálculo **Total de gastos online**, escolha **Somar** no menu suspenso **Selecionar função**.

1. Selecione **+ Adicionar atributo**, expanda **Compras: Comércio eletrônico**, selecione **TotalPrice** e clique em **Adicionar**.

1. Em **Configurar cálculos de** medida, selecione **Dimensões (1)**.

1. Selecione **Editar dimensões**.

1. Expanda **Compras: Comércio eletrônico**, selecione **ContactID** e selecione **Concluído**.

1. Escolha **Aplicar**.

1. Clique no botão **Executar** para concluir a medida.

### Tarefa 3: Definir atributos do cliente 
Primeiro, definiremos o **Total de Pontos de Fidelidade** ganhos por cada cliente.

1. Se necessário, selecione **Insights > Medidas** no menu de navegação à esquerda.

1. Selecione **+ Nova > Criar a sua** na barra de ferramentas.

1. Selecione **Editar detalhes** ao lado do texto do cabeçalho **Medida sem título**.

1. Defina o **Nome** como **Total de pontos do clube** e selecione **Concluído**.

1. No cálculo **Total de pontos do clube**, escolha **Somar** no menu suspenso **Tipo de função**.

1. Selecione **+ Adicionar atributo**, expanda **Compras: PDV**, selecione **RewardPointsAdded** e selecione **Adicionar**.

1. Clique no botão **Executar** para concluir a medida.

    A seguir, definiremos o valor total de todas as compras feitas de cada cliente.

1. Selecione **Insights > Medidas** no menu de navegação à esquerda.

1. Selecione **+ Nova > Criar a sua** na barra de ferramentas.

1. Selecione **Editar detalhes** ao lado do texto do cabeçalho **Medida sem título**.

1. Defina o **Nome** como **Gasto vitalício (US$)** e selecione **Concluído**.

1. No cálculo **Gasto vitalício (US$)**, escolha **Soma** no menu suspenso **Tipo de função**.

1. Selecione **+ Adicionar atributo**.

1. Selecione a guia **Medidas**, expanda **TotalInStoreSpend: CustomerInsights**, selecione **Cálculo 1** e **Adicionar**.

1. Selecione o **+ (sinal de mais)** para adicionar um sinal de mais após o atributo que você acabou de adicionar. O sinal de mais aparecerá na fórmula de cálculo.

1. Selecione **+ Adicionar atributo**.

1. Selecione a guia **Medidas**, expanda **TotalOnlineSpend: CustomerInsights**, selecione **Cálculo 1** e **Adicionar**.

1. Clique no botão **Executar** para concluir a medida.

    A seguir, definiremos o valor médio de todas as compras na loja feitas de cada cliente.

1. Selecione **Insights > Medidas** no menu de navegação à esquerda.

1. Selecione **+ Nova > Criar a sua** na barra de ferramentas.

1. Selecione **Editar detalhes** ao lado do texto do cabeçalho **Medida sem título**.

1. Defina o nome como **Média de compras na loja (US$)** e selecione **Concluído**.

1. No cálculo **Média de compras na loja (US$),** escolha **Média** no menu suspenso **Selecionar função**.

1. Selecione **+ Adicionar atributo**, expanda **Compras: PDV**, selecione **Preço total** e **Adicionar**.

1. Clique no botão **Executar** para completar a medida.

### Tarefa 4: Valor médio das compras na web
A seguir, definiremos o valor médio de todas as compras na web feitas de cada cliente.

1. Se necessário, selecione **Medidas** no menu de navegação à esquerda.

1. Selecione **+ Nova > Criar a sua** na barra de ferramentas.

1. Selecione **Editar detalhes** ao lado do texto do cabeçalho **Medida sem título**.

1. Defina o nome como **Média de compras na Web (US$)** e selecione **Concluído**.

1. No cálculo **Média de compras na Web (US$),** escolha **Média** no menu suspenso **Selecionar função**.

1. Selecione **+ Adicionar atributo**, expanda **Compras: Comércio eletrônico**, selecione **Preço total** e **Adicionar**.

1. Clique no botão **Executar** para concluir a medida.
