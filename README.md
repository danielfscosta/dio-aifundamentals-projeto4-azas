# Desafio de Projeto 4 - Azure Cognitive Search: Utilizando AI Search para indexação e consulta de Dados

Neste desafio, busca-se atender a necessidade de um gestor de uma grande cadeia de Cafés de extrair percepções sobre experiências de usuários baseando-se em avaliações de clientes. A obtenção de conhecimento ao utilizar-se de serviços inteligentes de aprendizagem a partir de um grande volume de dados, também chamada de *knowledge mining* ou mineração de conhecimento, é um ramo em pleno crescimento na inteligência artificial.

Para o objetivo definido, serão utilizados os recursos ***Azure AI Search*** (que conduzirá a indexação e pesquisa), ***Azure AI services*** (cujos serviços para o enriquecimento de dados através de inteligência artificial serão aproveitados nesta solução) e ***Storage account*** (para o armazenamento de documentos em sua forma crua).

## Passo-a-Passo

### Criação de um recurso *Azure AI Search*

1. Para criação deste recurso é possível selecionar ***+ Create a resource*** na página inicial do [Azure portal](https://portal.azure.com/). Na tela ***Create a resource***, procurar por *Azure AI Search*, selecionar ***Create*** e, em seguida, ***Azure AI Search***.

![image](https://github.com/danielfscosta/dio-aifundamentals-projeto4-azas/assets/69484807/4151d058-5770-4c72-989d-3a5198b89516)

![image](https://github.com/danielfscosta/dio-aifundamentals-projeto4-azas/assets/69484807/fd285351-7672-4d09-9a5a-57fe1edbd2a5)

2. Na página ***Create a search service***, realizar as configurações conforme sugerido abaixo, selecionar ***Review + Create*** e então, após obter sucesso na validação e revisão das configurações na próxima página, selecionar ***Create***. Esperar que os recursos sejam completamente provisionados.

- ***Subscription***: Escolher a assinatura a ser utilizada na criação do recurso;
- ***Resource Group***: Grupo de recursos onde será alocado. Caso não exista um grupo de recursos definido, um novo poderá ser criado neste passo através do link *Create New*;
- ***Service Name***: Escolher um nome único para o recurso;
- ***Location***: Selecionar a região em que serão provisionados o recursos, atentando-se para a diferença de precificação em cada região;
- ***Princing tier***: Basic. Através do link *Change Princing Tier*, uma nova página com uma tabela comparativa de níveis de especificações de *hardware* é aberta para escolha. Depois de escolhido o nível, selecionar ***Select***;

![image](https://github.com/danielfscosta/dio-aifundamentals-projeto4-azas/assets/69484807/09760ea4-1648-425d-a8d1-5fac3526635c)

![image](https://github.com/danielfscosta/dio-aifundamentals-projeto4-azas/assets/69484807/7a38374e-7d1f-4bed-a9e2-fb05ef18eeca)

![image](https://github.com/danielfscosta/dio-aifundamentals-projeto4-azas/assets/69484807/05028328-f200-4a69-a9ed-1fe8059000e5)

![image](https://github.com/danielfscosta/dio-aifundamentals-projeto4-azas/assets/69484807/fb532de4-8e3b-4ddb-9a81-070adbe17733)

### Criação de um recurso *Azure AI services***

1. Este recurso será utilizado pela solução de pesquisa para o enriquecimento dos dados armazenados com percepções geradas através de inteligência artificial. Para criação deste recurso é possível selecionar ***+ Create a resource*** na página inicial do [Azure portal](https://portal.azure.com/). Na tela ***Create a resource***, procurar por *Azure AI services*, selecionar ***Create*** e, em seguida, ***Azure AI services***.

![image](https://github.com/danielfscosta/dio-aifundamentals-projeto4-azas/assets/69484807/3c4cde18-72ee-413b-9ad7-194c414c7028)

![image](https://github.com/danielfscosta/dio-aifundamentals-projeto4-azas/assets/69484807/4a1c43dd-a80a-4472-ad56-e404dc80a3d1)

2. Na página ***Create Azure AI services***, realizar as configurações conforme sugerido abaixo, selecionar ***Review + Create*** e então, após a revisão das configurações na próxima página, selecionar ***Create***. Esperar que os recursos sejam completamente provisionados.

- ***Subscription***: Escolher a assinatura a ser utilizada na criação do recurso;
- ***Resource Group***: Grupo de recursos onde será alocado. Nesse caso, o mesmo em que o *Azure AI Search* se encontra;
- ***Region***: Selecionar mesma região em que se encontra o recurso *Azure AI Search* para provisionamento;
- ***Name***: Escolher um nome único para o recurso;
- ***Princing tier***: Standard S0;
- ***By checking this box I acknowledge that I have read and understood all the terms below***: Selecionar.

![image](https://github.com/danielfscosta/dio-aifundamentals-projeto4-azas/assets/69484807/1d057b82-21b4-4911-bc2c-45526d6b3602)

![image](https://github.com/danielfscosta/dio-aifundamentals-projeto4-azas/assets/69484807/41ef1814-8635-4045-a8a9-0301a4277619)

### Criação da *Storage account*

1. Para criação deste recurso é possível selecionar ***+ Create a resource*** na página inicial do [Azure portal](https://portal.azure.com/). Na tela ***Create a resource***, procurar por *Storage account*, selecionar ***Create*** e, em seguida, ***Storage account***.

![image](https://github.com/danielfscosta/dio-aifundamentals-projeto4-azas/assets/69484807/8b55d883-f98d-42ab-a24f-ba12ac5784f3)

![image](https://github.com/danielfscosta/dio-aifundamentals-projeto4-azas/assets/69484807/f92493c9-f578-4b22-8778-c74fcc7c2cba)

2. Na página ***Create a storage account***, realizar as configurações conforme sugerido abaixo, selecionar ***Review + Create*** e então, após a revisão das configurações na próxima página, selecionar ***Create***. Esperar que os recursos sejam completamente provisionados e então selecionar ***Go to resource***.

- ***Subscription***: Escolher a assinatura a ser utilizada na criação do recurso;
- ***Resource Group***: Grupo de recursos onde será alocado. Nesse caso, o mesmo em que o *Azure AI Search* se encontra;
- ***Storage account name***: Escolher um nome único para o conta de armazenamento;
- ***Location***: Selecionar a região em que será provisionado o recurso, atentando-se para a diferença de precificação em cada região;
- ***Performance***: Standard;
- ***Redundancy***: Locally redundant storage (LRS).

![image](https://github.com/danielfscosta/dio-aifundamentals-projeto4-azas/assets/69484807/68f7ee98-0319-4a9e-8137-40622dda9c53)

![image](https://github.com/danielfscosta/dio-aifundamentals-projeto4-azas/assets/69484807/09d7d76c-aad2-4399-a76c-c311ba4b0392)

![image](https://github.com/danielfscosta/dio-aifundamentals-projeto4-azas/assets/69484807/46878cf8-a624-410f-b7ed-9e1bd0605326)

3. No menu à esquerda da página do recurso, selecionar ***Configuration*** (na seção ***Settings***). Na página de configuração, escolher ***Enabled*** no campo ***Allow Blob anonymous access*** e selecionar ***Save***.

![image](https://github.com/danielfscosta/dio-aifundamentals-projeto4-azas/assets/69484807/1c1ff0ef-d80e-4bd7-afae-a4d3a741ba7e)

### Carregamento dos documentos no *Azure Storage*


