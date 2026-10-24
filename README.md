# Sobre o Dataset

Este conjunto de dados abrange, sem duplicatas ou registros corrompidos, os 6.445 exoplanetas confirmados catalogados pelo NASA Exoplanet Archive (IPAC/Caltech) até outubro de 2026, contemplando dinâmicas orbitais, propriedades planetárias globais, parâmetros das estrelas hospedeiras e métricas multidimensionais de habitabilidade.

## Como executar

O notebook principal [dataset_espacial_principal.ipynb](dataset_espacial_principal.ipynb) lê os arquivos CSV diretamente da raiz do projeto. Para manter compatibilidade com a execução local e com o histórico do repositório, os dados também estão disponíveis em [dados-base/](dados-base/) e em cópias na raiz do projeto.

## Classificação dos planetas e estrelas

### Arquétipo planetário

* Sub-Netuno/Mini gasoso (2 a 4 raios terrestres): 2119 planetas (32,88%);
* Gigante gasoso/Júpiter (4 a 15 raios terrestres): 2011 planetas (31,20%);
* Superterra (1,25 a 2 raios terrestres): 1366 planetas (21,20%);
* Terrestre Rochoso (menos de 1,25 raio terrestre): 583 planetas (9,05%);
* Super-Júpiter Extremo (mais que 15 raios terrestres): 366 planetas (5,68%).

![01_massa_vs_raio](https://github.com/user-attachments/assets/21c138bb-1eaf-4ed7-8110-ec288d1d4549)

### Zona de habitabilidade térmica

* Infernal (Temperatura de equilíbrio superior a 500 Kelvin): 4042 planetas (62,72%) - acoplamento de maré, atmosferas abrasadoras;
* Morno/Temperado (320 K a 500 K): 1219 planetas (18,91%);
* Gélido/Criogênico (inferior a 200 K): 755 planetas (11,71%) - Mundos congelados de gás e gelo do sistema externo;
* Zona Habitável Conservadora (200 K a 320 K): 429 planetas (6,66%) - Candidatos ao equilíbrio de água líquida.

![04_periodo_vs_temperatura](https://github.com/user-attachments/assets/e7983a0a-5a02-418b-9fb6-a75730f2f7bd)

### Regimes de arquitetura orbital

* Sistema Interno Compacto (Período de 1 a 10 dias terrestres): 2762 planetas (42,85%);
* Órbita na Zona Habitável (Período de 10 a 400 dias): 2522 planetas (39,13%);
* Sistema Externo Frio (Período superior a 400 dias): 994 planetas (15,42%);
* Período Ultracurto (Período inferior a 1 dia): 167 planetas (2,59%).

![05_arquitetura_orbital](https://github.com/user-attachments/assets/cb9b4b0c-050c-4115-b33c-8f4a8dcb7af6)

### Classe da estrela

* Análoga ao Sol (Anã Classe G) (5200 a 6000 Kelvin): 2879 estrelas (44,67%);
* Anã Laranja (Classe K) (3700 a 5200 K): 1804 estrelas (27,99%);
* Estrela Massiva Quente (Classes F/A) (superior a 6000 K) : 1152 estrelas (17,87%);
* Anã Vermelha (Classe M) (inferior a 3700 K): 610 estrelas (9,46%).

  ![06_classe_estelar](https://github.com/user-attachments/assets/edf310dd-c6ed-4ed3-b449-ccc762010653)
  
  Obs.: para melhor leitura, os outliers superiores das Estrelas Massivas Quentes e inferiores das Anãs Vermelhas não aparecem no gráfico.

## Atributos

| Coluna | Tipo de dado | Descrição |
| --- | --- | --- |
| nome_planeta | String (Qualitativo) | Nome oficial (IAU) do exoplaneta ou designação atribuída por ocasião de sua descoberta. |
| nome_estrela_primaria | String (Qualitativo) | Nome da estrela principal em torno da qual o planeta orbita. |
| metodo_descoberta | String (Qualitativo) | Método principal de detecção observacional. |
| ano_descoberta | Inteiro | Ano em que a descoberta do planeta foi oficialmente anunciada e confirmada (1992 a 2026). |
| observatorio_descoberta | String (Qualitativo) | Missão espacial ou observatório astronômico em solo ao qual se atribui a detecção inicial. |
| periodo_orbital | Float | Período orbital em que o planeta completa uma volta ao redor de sua estrela, expresso em dias terrestres. |
| raio_planetario | Float | Raio do planeta medido em unidades de raios terrestres. |
| massa_planetaria | Float | Massa do planeta ou massa mínima, expressa em unidades de massas terrestres. |
| temp_equilibrio_superf_planetaria | Float | Temperatura de equilíbrio da superfície planetária em Kelvin. |
| temp_superf_estelar | Float | Temperatura da superfície (fotosfera) da estrela, em Kelvin. |
| distancia_sistema | Float | Distância do Sistema Solar a esse sistema estelar, medida em parsecs. |
| arquetipo_planetario | String (Qualitativo) | Arquétipo estrutural do planeta. |
| zona_habitabilidade_termica | String (Qualitativo) | Regime térmico do planeta. |
| nivel_arquitetura_orbital | String (Qualitativo) | Categoria de dinâmica orbital do planeta. |
| classe_estelar | String (Qualitativo) | Categoria espectral da estrela. |

## Referências

### Kaggle

[Dataset NASA Exoplanets Archive no Kaggle](https://www.kaggle.com/datasets/luthfimuthathohirin/nasa-exoplanets-archive)
