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


## ObterDeclividade


## VetorizaRaster


## SimbologiaAltitude


## SimbologiaDeclividade


## CriarMapa


## EditarMapa
