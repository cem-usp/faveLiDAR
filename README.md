# faveLiDAR

Projeto de análises de dados LiDAR 3D em assentamentos informais e favelas

## Motivação

São Paulo e algumas cidades do Brasil tem levantamentos LiDAR 3D. Tais dados contínuos de toda a área da cidade podem conter informações importantes para análises, classificações e descrições de áreas de assentamento precário como as favelas.

## Objetivo

O objetivo desse repositório e estudar, apresentar técnicas, experimentar e avaliar métodos de trazer subsídios para esse tema a partir dos levantamentos LiDAR 3D de algumas cidades brasileiras a começar por São Paulo.

## Materiais e métodos

São Paulo tem a disposição dois levantamentos LiDAR 3D, realizados em 2017 e 2020, assim como uma extensa quantidade de dados e levantamentos disponíveis no GeoSampa. A partir de tais conjuntos de dados iremos utilizar linguagem de programação Python em Notebooks afim de gerar resultados como:

* Área contruída estimada
* Densidade Cosntruída
* Aumento/Decréscimo das áreas contruiídas
* Restituição das edificações
* Contagem de edificações
* Dimensões qualitativas da forma
* Classificação tipomórfica das edificações por grau de precariedade
* Presença ou auséncia de recuos para iluminação e ventilação
* Identificação de rotas e acessos
* Segmentação e busca de áreas favelizadas e não favelizadas

### Instalação do ambiente de trabalho

Como utilizamos a biblioteca `pdal` precisamos instalar um ambiente de trabalho compatível:

```
conda create --yes --name pdal --channel conda-forge pdal ipykernel pip

conda activate pdal

pip install -r requirements.txt
```

E para subir o banco de dados:

```
docker run -d -e POSTGRES_USER=postgres -e POSTGRES_PASS=1234 -e POSTGRES_DBNAME=faveLiDAR -e ALLOW_IP_RANGE=0.0.0.0/0 -p 5432:5432 -v pg_data:/var/lib/postgresql --restart=always kartoza/postgis:15-3.3
```

## Resultados

Espera-se com esse repositório, além dos resultados práticos a serem publicados a medida que forem processados, persistir e disseminar ténicas de LiDAR para as análises da morfologia urbana

