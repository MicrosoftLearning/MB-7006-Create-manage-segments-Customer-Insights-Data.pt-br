---
lab:
  title: 'Laboratório 4: Criar segmentos'
---

# Laboratório 4: Criar segmentos

Neste laboratório, você aprenderá a:
- Criar um segmento a partir de um perfil
- Criar um segmento usando medidas
- Criar um segmento do zero

## Exercício 1: Criar segmentos de várias fontes 
### Tarefa 1: Criar um segmento a partir de um perfil
Nesta primeira tarefa, vamos criar um segmento com base no perfil do cliente. Vamos identificar todos os clientes que residem no estado do Texas. 

1. Expanda **Insights** e selecione **Segmentos** no menu de navegação à esquerda.

1. Selecione **+ Novo > Criar a partir de perfis**.

1. Em **Campo**, selecione **Estado** e, em **Valor**, escolha **Texas**.

1. Selecione **Revisar**.

1. Nomeie o segmento como **Clientes do Texas** e verifique se o **Nome da tabela de saída** foi preenchido automaticamente com **CustomersFromTexas**.

1. Selecione **Salvar**.

### Tarefa 2: Criar um segmento usando medidas 
O Marketing da Contoso Coffee quer fazer uma nova promoção. Com base em dados históricos, o marketing identificou que quer atingir clientes que preparam bebidas em casa com um valor de compra online acima da média para fazê-lo. Desta vez, vamos criar o segmento usando a opção **Criar a partir de medidas**. 

1. Selecione **Insights > Segmentos** no menu de navegação à esquerda.

1. Selecione **+ Novo > Criar a partir de Medidas**.

1. Selecione o atributo **Compra média na loja (US$).**

1. Defina o **Operador** como **Maior que**.

1. Defina o **Valor** como **100**. O gráfico deve ser preenchido com **Compra média na web (US$)** por percentil.

1. Selecione **Revisar**.

1. Nomeie o segmento como **Clientes do Premiere** e verifique se o **Nome da tabela de saída foi** preenchido automaticamente com **PremiereCustomers**.

1. Selecione **Salvar**.

### Tarefa 3: Criar um segmento do zero
A cada temporada, a Contoso Coffee realiza promoções diferentes. Este ano, eles querem fazer uma promoção de liquidação de outono com o objetivo de vender os modelos de final de ano restantes. Eles querem atingir a Geração X com uma compra na loja acima da média com o recém-lançado Cold Brew Coffee. Como há vários critérios necessários para esse segmento, vamos criá-lo do zero.

1. Selecione **Insights > Segmentos** no menu de navegação à esquerda. Selecione **+ Novo > Criar o seu**.

1. Ao lado do texto do cabeçalho **Segmento sem título**, selecione **Editar detalhes** e altere o **Nome** para **Promoção de liquidação de outono**.

1. Verifique se o **Nome da entidade de saída** foi preenchido automaticamente com **FallCloseoutPromotion** e selecione **Concluído**.

1. Usando o painel **Adicionar à Regra 1** no lado direito da tela, expanda **Cliente : CustomerInsights** e selecione **DateofBitrh**. 

1. Selecione **é** e **em ou após** e insira a data como **01/01/1965**.

1. Adicione outra condição com um qualificador **e**.

1. Defina essa condição como **DateOfBirth** é **em ou antes de 31/12/1979**.

1. Adicione outra condição com um qualificador **e**. 

1. Expanda **Customer_Measure: CustomerInsights**.

1. Selecione a medida **Média de Compra na Web (US$)** e adicione-a à **Regra 1**. 

1. Selecione **é** e **maior ou igual a 125**.

1. Adicione outra condição com um qualificador **e**. 

1. No campo **Inserir um nome de atributo ou adicionar a partir do painel**, insira **Gênero** e selecione-o na lista exibida. 

1. Selecione **é** e **igual a masculino**.

1. Marque a caixa de seleção **Ignorar caso**.

1. Em **Regra 1**, selecione **+ Adicionar Regra**. 

1. Selecione a caixa **União** e altere-a para **Exceto**.

1. No painel **Adicionar à Regra 2**, expanda **Cliente: CustomerInsights** e selecione **Estado**. 

1. Selecione **é** e **igual a Flórida**.

1. Selecione **Salvar**.

1. Selecione **Executar**.
