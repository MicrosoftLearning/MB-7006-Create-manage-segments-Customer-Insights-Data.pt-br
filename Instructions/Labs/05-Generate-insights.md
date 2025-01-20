---
lab:
  title: 'Laboratório 5: Gerar insights'
---

# Laboratório 5: Gerar insights 

Neste laboratório, você aprenderá a:
- Gerar insights sobre seus segmentos 
- Visualizar diferenciais e fazer sobreposição entre segmentos 
- Criar segmentos sugeridos com base em um segmento 

## Exercício 1: Gerar insights sobre seus segmentos
### Tarefa 1: Segmentar diferenciadores
Muitas vezes, você terá clientes que existem em vários segmentos. Pode ser útil entender quando pode haver sobreposição entre eles. Vamos tentar descobrir os clientes comuns que pertencem aos segmentos **Clientes do Texas** e **Promoção de liquidação de outono** e também o que diferencia esses dois segmentos em termos de **Pontos de recompensa** e **LifetimeSpend**.

1. Selecione **Insights > Segmentos** no menu de navegação à esquerda. Selecione a guia **Insights (versão prévia)** e **+ Novo** na barra de comandos ou clique no botão **+ Novo insight**.

1. Agora você verá duas opções. Vamos criar usando **Diferenciadores** primeiro para ver o que distingue esses dois segmentos. Selecione **Diferenciadores**.

1. Escolha **Promoção de liquidação de outono** como o segmento principal. Selecione **Avançar**.

1. Escolha **Clientes do Texas** como outro segmento e, em seguida, selecione **Avançar**.

1. Agora escolha **Pontos de recompensa** em **Campos do cliente** e **LifetimeSpend** em **Campos de medida** para ver como os segmentos acima diferem uns dos outros em relação a **Pontos de recompensa** e **LifetimeSpend**. Desmarque todos os outros campos de cliente e medida.

1. Selecione **Avançar** e nomeie o insight como **Promoção de liquidação x Clientes do Texas**.

1. Verifique se o nome da **Entidade de saída** está definido como **FallPromotionvsCustomersfromTexas**. Selecione **Salvar**.

1. Depois que o insight terminar de ser atualizado, abra o insight criado. Selecione as guias **Atributos** ou **Medidas** para ver como os segmentos diferem uns dos outros em relação aos campos selecionados. Observe a **Pontuação de diferença**, que significa o grau de diferença. Quanto maior a pontuação, mais diferentes eles são.

1. Selecione cada medida e atributo para ver insights mais detalhados.

### Tarefa 2: Sobreposição de segmento
Agora que criamos um insight de segmento usando **Diferenciadores**, vamos criar um insight usando **Sobreposição**.

1. Verifique se você ainda está na guia **Segmentos > Insights (versão prévia)** e selecione **+ Novo** na barra de comandos. Escolha **Sobrepor**.

1. Selecione os segmentos **Promoção de liquidação de outono** e **Clientes do Texas** para descobrir seus clientes compartilhados.

1. Selecione **Avançar**.

1. Nomeie o segmento como **Clientes da promoção de outono sobrepostos com Clientes do Texas** e verifique se o **Nome da tabela de saída** está definido como **FallPromotionCustomersOverlappedwithTexasCustomers**. Selecione **Salvar**.

1. Depois que o insight terminar de ser atualizado, abra o insight criado para ver o diagrama de Venn mostrando o total e a porcentagem de clientes compartilhados entre esses dois segmentos.

## Exercício 2: Expansão de segmento e segmentos sugeridos
### Tarefa 1: Expansão de segmento
A expansão de segmento pode ser usada para encontrar clientes semelhantes à sua base de clientes de segmento usando Inteligência Artificial. Anteriormente, criamos um segmento chamado **Clientes da promoção de outono**, que contém clientes millennials com compras na loja acima da média. Agora, vamos expandir esse segmento e encontrar clientes semelhantes a eles para comercializarmos nosso recém-lançado Cold Brew Coffee.

1. Selecione **Insights > Segmentos** no menu de navegação à esquerda e selecione a guia **Todos os segmentos**.

1. Escolha o segmento **Clientes da promoção de outono**. Este se tornará nosso segmento de origem.

1. Selecione **Localizar clientes semelhantes** na barra de comandos.

1. Nomeie o segmento como **FallPromoExpansion**.

1. Selecione **Adicionar campos** na próxima etapa para selecionar atributos e medidas que são usados para localizar clientes semelhantes. Segmentaremos clientes com localização semelhante e compra média na loja, então escolha **PostCode** e **AverageStorePurchase**. Escolha **Aplicar**.

1. Em seguida, você deve escolher quem considerar. Por enquanto, selecione **Todos os clientes, exceto o segmento de origem**.

1. Agora, o número máximo de clientes a serem incluídos deve ser selecionado. Vamos manter **20%**.

1. Se você quiser incluir membros do segmento de origem também, marque a última opção. Caso contrário, deixe-o desmarcado. Para nossos propósitos, podemos deixá-lo desmarcado.

1. Selecione **Executar**.

1. Depois que o segmento terminar de atualizar, abra o segmento para encontrar as **Pontuações de similaridade** e explorar a **Visualização dos membros do segmento**.

### Tarefa 2: Obter segmentos sugeridos 
Use Segmentos sugeridos para descobrir segmentos interessantes com base em um atributo do cliente ou medida de interesse.

1. Selecione **Insights > Segmentos** no menu de navegação à esquerda e selecione a guia **Sugestões (versão prévia).**

1. Selecione **Obter sugestões** para iniciar a experiência de configuração.

1. Escolha **Melhorar uma medida/métrica** e selecione **Iniciar**.

1. Em **Campos de medida**, selecione **LifetimeSpend** como o atributo de destino. Selecione **Avançar**.

1. Em seguida, você selecionará os atributos que podem influenciar o atributo de destino (**LifetimeSpend**) para que o modelo de IA possa encontrar padrões interessantes entre o atributo de influência e o atributo de destino. O modelo sugerirá segmentos com base nesses padrões. Selecione **Assinante de email**, **Renda**, **Nível de fidelidade**, **Ocupação** e **Estado** como os atributos de influência.

1. Selecione **Executar**. O modelo de IA começará a encontrar padrões entre os atributos de influência selecionados e os atributos de destino para sugestões de segmento de superfície. Aguarde alguns minutos para que o modelo termine a análise.

1. Depois que o modelo terminar de ser executado e se ele for capaz de descobrir padrões entre os atributos de influência e o atributo de destino, as sugestões de segmento serão exibidas na guia **Sugestões (versão prévia)**.

1. Para salvar o segmento, selecione **Salvar como segmento** no painel **Detalhes do segmento sugerido**. Selecione **Salvar**.

1. O segmento salvo pode ser visualizado na guia **Todos os segmentos** e pode ser usado para processos downstream como qualquer outro segmento dinâmico. Se você quiser examinar as regras que o modelo aprendeu depois de salvar um segmento, selecione **Editar** na guia **Todos os segmentos**.
