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

## ExcluirSemFeicoes


## ObterAltitude


## ReprojetaRaster


## ObterDeclividade


## VetorizaRaster


## SimbologiaAltitude


## SimbologiaDeclividade


## CriarMapa


## EditarMapa
