<p align="center">
   <img src="assets/img/header.png">  
</p>


# Machine Learning applied to Sports - Web scraping/Web Crawler/Search Engine

**Alunos:** Danielle Regina Bernardes, João Fernando V. Franciscon, Fernando Rafael Araújo e Marcos Paulo de Oliveira
**Orientador**: Robson P. Bonidia

Este projeto é divido em duas partes:
  - **Scraper:** raspa os dados das temporadas e dos times;
  - **Experimentos:** contém *notebooks* com todos os experimentos realizados para construção do modelo para predição dos resultados.
    - Os arquivos estão vagamente organizados por versões, cada versão com experimentos e resultados diferentes.

Também realizamos uma [competição Kaggle](https://www.kaggle.com/competitions/1-desafio-cd-fatec-ourinhos/) com os dados obtidos neste projeto.

---

## Scraper

### Instruções
#### Raspagem
 - Crie um novo ambiente e o ative
 - Faça a instalação dos módulos necessários: ``` pip install requirements.txt ``` 
 - Execute o script: ``` web_scaper.py [ano_inicial] [ano_final] ```
   - Exemplo:  ``` web_scaper.py 2005 2010 ```
   - Opções extras:
     - ``` -o ```
       - exporta dados da temporada
     - ``` -ts ```
       - exporta dados dos jogos dos times
     - ``` -stat ```
       - exporta nomes e descrições das colunas
     - ``` -pickle ```
       - exporta os dados em formato .pickle
     - ``` -w=[n] ```
       - específica o número de *workers* que o script irá utilizar (padrão = 4)
       - exemplo: ``` -w=6 ```
       - Mais *workers* significa menos tempo de execução, porém mais consumo de memória e processamento.
       - Para máquinas com 8GB de RAM, utilize no máximo **6**.

 - Pasta destino padrão: ```./data/```
 
#### Junção dos dados
  - Após colher os dados, é necessário unir os dados dos jogos da temporada com os dados dos times.
  - Execute o *script* ```merge_script/merge_games_team_stats.py```
  - Talvez seja necessário alterar o caminho dos arquivos de entrada, abra o *script* e altere as linhas indicadas.

Informações recolhidas do site https://www.pro-football-reference.com/.

---

## Experimentos
Os experimentos realizados se encontram no caminho ```experimentos/```.

Todos estão no formato ```.ipynb``` e utilizam diversas bibliotecas e *frameworks*.

Originalmente, os experimentos foram executados no **Kaggle**, então é recomendado subir os *notebooks* lá, para garantir que todos os requisitos estão instalados.
