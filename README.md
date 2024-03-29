# <div align="center">Desafio 4 - Microsoft Azure AI Fundamentals</div>
## _Azure Cognitive Search: Utilizando AI Search para indexação e consulta de Dados_



Atividade desenvolvida seguindo as orientações do curso da DIO com a orientadora Valéria Baptista bem como com o passo a passo descrito no link: [AI Search](https://github.com/skyzinha-chan/mslearn-ai-fundamentals/blob/main/Instructions/Labs/11-ai-search.md).

>- A Pesquisa de IA do Azure fornece recuperação de informações seguras em escala sobre o conteúdo de propriedade do usuário nos aplicativos de pesquisa tradicionais e generativos.</br>
>- A recuperação de informações é fundamental para qualquer aplicativo que apresenta texto e vetores.</br>
>- Os cenários comuns incluem pesquisa de catálogos ou documentos, exploração de dados e, cada vez mais, aplicativos no estilo de chat sobre os dados de aterramento proprietários.</br>
>- Os passos a seguir desta pesquisa simples indexa apenas alguns dos recursos do serviço de Pesquisa de IA do Azure.</br>
>
>

```
Situação-problema: Numa rede de café ampla, precisa-se saber se os clientes estão satisfeitos com os
produtos oferecidos, o setor da área de tecnologia dessa rede irá fazer esse levantamento de informações.
```


## Criar recurso Azure AI.

- Criação de um espaço de trabalho ou utilização de um já existente, para este caso criei um novo no portal do Azure, que ao final do projeto será excluido para não utilizar os créditos da Azure.
- Configuração de um recurso dentro do espaço de trabalho de acordo com a vídeo aula e criação de Azure AI Services.
- Após a criação do recurso é realizado os passos do laboratório 4.

***
## <div align="center">Atividades desenvolvidas:</div>

- [x] Um recurso de Pesquisa de IA do Azure, que gerenciará a indexação e a consulta.
      
![Criação de um Azure AI Search](https://github.com/skyzinha-chan/mslearn-Azure-Cognitive-Search-ai-900/blob/main/prints/cria%C3%A7%C3%A3o%20de%20resourse%2C%20cria%C3%A7%C3%A3o%20de%20azure%20ai%20search%2C%20configura%C3%A7%C3%A3o%20e%20deploy.jpeg)

- [x] Criação de um recurso LAB4-AI-900 de serviços de IA do Azure, que fornece serviços de IA para habilidades que sua solução de pesquisa pode usar para enriquecer os dados na fonte de dados com insights gerados por IA.
      
![Criação de um Azure AI Services](https://github.com/skyzinha-chan/mslearn-Azure-Cognitive-Search-ai-900/blob/main/prints/cria%C3%A7%C3%A3o%20do%20lab%20e%20services.jpeg)

- [x] Uma conta de armazenamento com contêineres de blob, que armazenará documentos brutos e outras coleções de tabelas, objetos ou arquivos.
      
![Criação de um Azure AI Storage Account](https://github.com/skyzinha-chan/mslearn-Azure-Cognitive-Search-ai-900/blob/main/prints/cria%C3%A7%C3%A3o%20store%20account.jpeg)


## <div align="center">Detalhes Específicos:</div>

1. Carregando documentos no storage account;</br>

2. Criando o Contêiner: coffee-reviews;</br>

3. Importando e indexando dados para o [AI SEARCH](https://github.com/skyzinha-chan/mslearn-Azure-Cognitive-Search-ai-900/tree/main/reviews);</br>
   
![Coffe-Reviews-Criado](https://github.com/skyzinha-chan/mslearn-Azure-Cognitive-Search-ai-900/blob/main/prints/coffe-reviews%20criado.jpeg)

4. Na página Visão geral do serviço de Pesquisa, selecione Gerenciador de pesquisa na parte superior da tela.</br>

5. Observe como o índice selecionado é o coffee-index que foi criado. Abaixo do índice selecionado, a exibição é alterada para JSON view.</br>

 >Agora vamos filtrar por sentimento. No campo Editor de consultas JSON é colocado o código exibido no manual.</br>
 >Dessa forma a consulta pesquisa todos os documentos no índice e filtra por avaliações com um sentimento negativo.

![search explorer por sentimentos](https://github.com/skyzinha-chan/mslearn-Azure-Cognitive-Search-ai-900/blob/main/prints/search%20explorer%20por%20sentimentos.jpeg)


6. Revisar o knowledgestore acessando o Contêiner;</br>

 >Dentro da **knowledgestore**, encontra-se os dados enriquecidos extraídos pelas habilidades de IA persistem na forma de projeções e tabelas.
 >Selecionando qualquer um dos itens, clica-se no arquivo objectprojection.json.
 >E selecione Editar para ver o JSON produzido para um dos documentos do armazenamento de dados do Azure.</br>

![Dados enriquecidos extraídos pelas habilidades de IA](https://github.com/skyzinha-chan/mslearn-Azure-Cognitive-Search-ai-900/blob/main/prints/dados%20enriquecidos%20extra%C3%ADdos%20pelas%20habilidades%20de%20IA.jpeg)


7. Retornando ao menu Contêineres, selecione o contêiner coffee-skillset-image-projection. E selecione qualquer um dos itens.</br>

![tabelas e contêiners criadas](https://github.com/skyzinha-chan/mslearn-Azure-Cognitive-Search-ai-900/blob/main/prints/tabelas%20e%20cont%C3%AAiners%20criadas.jpeg)

8. Selecione qualquer um dos .jpg dos arquivos. Novamente em Editar para ver a imagem armazenada do documento. Observe como todas as imagens dos documentos são armazenadas dessa maneira.</br>

![Imagem armazenada do documento](https://github.com/skyzinha-chan/mslearn-Azure-Cognitive-Search-ai-900/blob/main/prints/imagem%20armazenada%20do%20documento..jpeg)

9. Há uma tabela para cada entidade no índice. Selecione a tabela coffeeSkillsetKeyPhrases.</br>

![Há uma tabela para cada entidade no índice](https://github.com/skyzinha-chan/mslearn-Azure-Cognitive-Search-ai-900/blob/main/prints/H%C3%A1%20uma%20tabela%20para%20cada%20entidade%20no%20%C3%ADndice.jpeg)

>Veja as frases-chave que o knowledgestore conseguiu capturar do conteúdo das avaliações. Muitos dos campos são chaves, portanto, você pode vincular as tabelas como um banco de dados relacional.

***

>No aplicativo cliente, a experiência de pesquisa é definida usando APIs da IA do Azure Search e
>pode incluir ajuste de relevância, classificação semântica, preenchimento automático, correspondência de sinônimos, correspondência difusa, correspondência de padrões, filtro e classificação.

***
As funcionalidades que a integração desta API pode resultar em aplicações são vastas,
visando desenvolver e trazer métricas reais para o cliente, podem ser feitas os ajustes
necessários na empresa solicitante de acordo com critérios de local, produtos e reviews
buscando dessa forma ter um olhar de mudanças e melhoras contínuas com as informações capturadas,
a empresa consegue acompanhar todo este processo pelo qual passa e visualizar onde aplicar as adapções
precisas em busca de rentabilidade.

Talita Mendonça Marquês
***


![I-900 ](https://hermes.dio.me/tracks/4d998d5c-36c1-497b-8da0-8db465c820eb.png )
