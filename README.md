# Desafio de Projeto 4 - Azure Cognitive Search: Utilizando AI Search para indexação e consulta de Dados

Neste desafio, busca-se atender a necessidade de um gestor de uma grande cadeia de Cafés de extrair percepções sobre experiências de usuários baseando-se em avaliações de clientes. A obtenção de conhecimento ao utilizar-se de serviços inteligentes de aprendizagem a partir de um grande volume de dados, também chamada de *knowledge mining* ou mineração de conhecimento, é um ramo em pleno crescimento na inteligência artificial.

Para o objetivo definido, serão utilizados os recursos ***Azure AI Search*** (que conduzirá a indexaxão e pesquisa), ***Azure AI services*** (cujos serviços para o enriquecimento de dados através de inteligência artificial serão aproveitados nesta solução) e ***Storage account*** (para o armazenamento de documentos em sua forma crua).

## Passo-a-Passo

## Criação de um recurso *Azure AI Search*

1. Para criação deste recurso é possível selecionar ***+ Create a resource*** na página inicial do [Azure portal](https://portal.azure.com/). Na tela ***Create a resource***, procurar por *Azure AI Search*, selecionar ***Create*** e, em seguida, ***Azure AI Search***.

![image](https://github.com/danielfscosta/dio-aifundamentals-projeto4-azas/assets/69484807/4151d058-5770-4c72-989d-3a5198b89516)

![image](https://github.com/danielfscosta/dio-aifundamentals-projeto4-azas/assets/69484807/fd285351-7672-4d09-9a5a-57fe1edbd2a5)

2. Na página ***Create a search service***, realizar as configurações conforme sugerido abaixo, selecionar ***Review + Create*** e então, após obter sucesso na validação e revisar as configurações na próxima página, selecionar ***Create***. Esperar que os recursos sejam completamente provisionados.

- ***Subscription***: Escolher a assinatura a ser utilizada na criação do recurso;
- ***Resource Group***: Grupo de recursos onde será alocado. Caso não exista um grupo de recursos definido, um novo poderá ser criado neste passo através do link *Create New*;
- ***Service Name***: Escolher um nome único para o recurso;
- ***Princing tier***: Basic. Através do link *Change Princing Tier*, uma nova página com uma tabela comparativa de níveis de especificações de *hardware* é aberta para escolha. Depois de escolhido o nível, selecionar ***Select***;
- ***By checking this box I acknowledge that I have read and understood all the terms below***: Selecionar.

![image](https://github.com/danielfscosta/dio-aifundamentals-projeto4-azas/assets/69484807/09760ea4-1648-425d-a8d1-5fac3526635c)

![image](https://github.com/danielfscosta/dio-aifundamentals-projeto4-azas/assets/69484807/7a38374e-7d1f-4bed-a9e2-fb05ef18eeca)

![image](https://github.com/danielfscosta/dio-aifundamentals-projeto4-azas/assets/69484807/05028328-f200-4a69-a9ed-1fe8059000e5)

![image](https://github.com/danielfscosta/dio-aifundamentals-projeto4-azas/assets/69484807/1816f3e3-b862-4c3f-9081-e18120c7eca8)
