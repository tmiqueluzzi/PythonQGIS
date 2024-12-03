# PythonQGIS

Algumas funções úteis no QGis utilizando a linguagem python.

## AdicionarCamadas

Automatiza o processo de varredura de um diretório indicado pelo operar e suas subpastas em busca de arquivos no formato shapefile (.shp) e os adiciona ao projeto QGIS atual.

1. Pega o caminho indicado pelo operador;
2. Cria a lista que vai armazenar os caminhos para os arquivos '.shp';
3. Percorre as pastas e subpastas, adicionando os arquivos '.shp' à lista criada no passo anterior;
4. Roda a lista, adicionando os arquivos.

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


## ReprojetaRaster


## ObterDeclividade


## VetorizaRaster


## SimbologiaAltitude


## SimbologiaDeclividade


## CriarMapa


## EditarMapa
