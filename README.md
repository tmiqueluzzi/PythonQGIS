# PythonQGIS

Algumas funções úteis no QGis utilizando a linguagem python.

## AdicionarCamadas

Percorre um diretório especificado pelo usuário, identifica todos os arquivos com extensão `.shp` (shapefiles) em suas subpastas, e os adiciona ao projeto QGIS atual.

Requisitos:
- O script deve ser executado no ambiente do QGIS.
- O caminho para o diretório de origem deve ser fornecido pelo usuário.

Bibliotecas:
- `os`: Para navegação no sistema de arquivos.
- `qgis.core`: Para manipulação de camadas e projetos QGIS.
- `QInputDialog`: Para permitir que o usuário insira o caminho do diretório.

## ClipagemComSimbologia

Realiza o processo de clipagem de todas as camadas shapefile carregadas em um projeto QGIS, utilizando uma camada de área de interesse (AOI). Após a clipagem, ele salva a simbologia de cada camada original em um arquivo separado.

Requisitos:
- A camada de AOI deve estar carregada no projeto e ser referenciada pelo nome 'Area'.

Bibliotecas:
- `os`: Para manipulação de caminhos e arquivos.
- `qgis.core`: Para interagir com camadas e projetos do QGIS.
- `processing`: Para executar a ferramenta de processamento de clipagem.

## ExcluirSemFeicoes

Percorre todas as camadas vetoriais carregadas no projeto do QGIS e remove automaticamente aquelas que não possuem feições (ou seja, cuja contagem de feições é igual a 0);
Camadas Raster não são afetadas.

Requisitos:
- O projeto deve conter camadas carregadas.

Bibliotecas:
- `qgis.core`: Para interagir com as camadas e o projeto QGIS.

## ObterAltitude

Utiliza o plugin `OTDEMDownloader` para baixar um modelo digital de elevação (DEM) a partir da API do OpenTopography. Ele extrai os parâmetros da camada de entrada (extensão e sistema de referência de coordenadas - SRC), executa o download e adiciona o DEM resultante como uma camada ao projeto QGIS.

Requisitos:
- O plugin `OTDEMDownloader` deve estar instalado no QGIS.
- Uma camada vetorial de entrada carregada no projeto QGIS.
- Uma chave de API válida do OpenTopography.

Bibliotecas:
- `processing`: Para executar o algoritmo de download do DEM.
- `qgis.core`: Para interagir com camadas e projetos QGIS.

## ReprojetaRaster

Realiza a reprojeção de um raster já carregado no projeto QGIS para um Sistema de Referência de Coordenadas (SRC) especificado pelo usuário. O código EPSG do SRC desejado é fornecido por meio de uma caixa de diálogo de entrada.

Requisitos:
- O raster de entrada deve estar carregado no projeto QGIS.
- O nome do raster de entrada deve ser fornecido corretamente.
- O código EPSG válido deve ser informado pelo usuário.

Bibliotecas:
- `processing`: Para executar a reprojeção usando o algoritmo GDAL do QGIS.
- `PyQt5.QtWidgets.QInputDialog`: Para solicitar ao usuário o código EPSG desejado.

## ObterDeclividade

Utiliza a ferramenta "Slope" do GDAL para calcular a declividade de um raster de elevação digital (DEM) carregado no projeto QGIS. O resultado é adicionado automaticamente como uma camada raster ao projeto.

Requisitos:
- O raster de elevação (DEM) deve estar carregado no projeto QGIS com nome 'Raster Reprojetado'.
- O plugin de processamento GDAL deve estar habilitado no QGIS.

Bibliotecas:
- `processing`: Para execução de ferramentas de processamento no QGIS.
- `qgis.core`: Para manipulação de camadas raster e projeto no QGIS.

## VetorizarRaster

Converte rasters carregados no projeto QGIS em camadas vetoriais de polígonos, utilizando a ferramenta GDAL "Polygonize". O resultado é adicionado automaticamente ao projeto, permitindo análises vetoriais a partir dos valores originais do raster.

Requisitos:
- Os rasters de entrada devem estar carregados no projeto QGIS com nomes de 'Declividade Calculada' e 'Raster Reprojetado'.
- O plugin de processamento GDAL deve estar habilitado no QGIS.

Bibliotecas:
- `processing`: Para execução de ferramentas de processamento no QGIS.
- `qgis.core`: Para manipulação de camadas vetoriais e projeto no QGIS.


## SimbologiaAltitude

Ajusta a simbologia de uma camada vetorial de polígonos utilizando uma classificação graduada baseada nos valores de um campo (`DN`). As cores seguem uma rampa linear invertida da paleta "Blues". Os intervalos são criados em classes de 5 unidades.

Requisitos:
- A camada vetorial deve conter um campo numérico chamado `DN`.
- O projeto QGIS deve estar configurado com a camada vetorial nomeada 'Polígonos Raster Reprojetado'.
- O script utiliza funções para arredondamento de valores, criação de classes, interpolação de cores e aplicação de simbologia.


## SimbologiaDeclividade

Ajusta a simbologia de uma camada vetorial de polígonos utilizando uma classificação graduada baseada nos valores de um campo (`DN`). As cores seguem uma rampa linear invertida da paleta "Reds". Os intervalos são definidos de acordo com a divisão da EMBRAPA.

Requisitos:
- A camada vetorial deve conter um campo numérico chamado `DN`.
- O projeto QGIS deve estar configurado com a camada vetorial nomeada 'Polígonos Declividade'.
- O script utiliza funções para arredondamento de valores, criação de classes, interpolação de cores e aplicação de simbologia.

  
## CriarMapa


## EditarMapa
