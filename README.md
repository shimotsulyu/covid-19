# covid-19
O coronavirus é uma família de virus que causam infecções respiratórias. O novo coronavírus foi descoberto em 31/12/2019 na China, e desde então tem se espalhado pelo mundo todo. Hoje o vírus ja atingiu mais de 4,2 milhões de pessoas e causou aproximadamente 290 mil mortes. O número tem aumentado cada vez mais desde então. Por esta razão foi iniciado um estudo para desenvolver uma ferramenta para visualizar e prever os casos no Brasil utilizando métodos estatísticos de previsão.

# bibliotecas
numpy,
pandas,
seaborn,
matplotlib

# resultados parte 1 (Visualização de dados)

A seguir estão alguns resultados obtidos pelas informações fornecidas pelo Ministério da Saúde.

## visualização de casos e óbitos no Brasil
![casosAcumulado_Brasil](https://user-images.githubusercontent.com/59963253/83285558-cfc1ef00-a1b4-11ea-85a4-22fe924b174b.png)
![obitosAcumulado_Brasil](https://user-images.githubusercontent.com/59963253/83285564-d0f31c00-a1b4-11ea-92a0-76c5289a1894.png)


## visutalização comparativa de dos estados com SP
![SP_X_RJ_casos_mi](https://user-images.githubusercontent.com/59963253/83285694-0e57a980-a1b5-11ea-8c82-1541287b2dd1.png)
![SP_X_RJ_obitos_mi](https://user-images.githubusercontent.com/59963253/83285698-0f88d680-a1b5-11ea-8fd9-09a40821ad0e.png)

## visualização rank de casos e óbitos dos estados
![top 10 estados do Brasil_casosAcumulado](https://user-images.githubusercontent.com/59963253/83285566-d0f31c00-a1b4-11ea-822b-4f80a8ffb854.png)
![top 10 estados do Brasil_obitosAcumulado](https://user-images.githubusercontent.com/59963253/83285568-d18bb280-a1b4-11ea-8808-50b8d882cd9a.png)

## visualização do rank de casos e óbitos de cidades
![top 10 cidades do estado de SP_casosAcumulado](https://user-images.githubusercontent.com/59963253/83285866-655d7e80-a1b5-11ea-8e05-66a14eca2c5e.png)
![top 10 cidades do estado de SP_obitosAcumulado](https://user-images.githubusercontent.com/59963253/83285868-668eab80-a1b5-11ea-9c92-3137ab9db179.png)

# resultados parte 2 (Previsão de casos e óbitos)
Em desenvolvimento

# funções

### load_data(endereco,formato,separador)
carrega o data
input: endereço = nome do arquivo a ser carregado
formato = .csv (padrão)
separador = ; (padrão)
output: (dataframe)

### get_states(data)
coleta a lista com nome dos estados
input: data = (dataframe)
output: (dataframe)

### get_city(data,estado)
coleta a lista com o nome das cidades
input: data = (dataframe)
estado = sigla do estado (string)
output: (dataframe)

### cases_city(data,estado,target,n,plot)
rank das cidades com o maior numero de casos
input: data = (dataframe)
estado = sigla do estado (string)
target = nome da coluna a ser utilizada (string)
n = numero de cidades (padrão = 20)
plot = boleano (padrão = True)
output = (dataframe)

### cases_states(data,target,n,plot)
rank dos estados com o maior numero de casos
input: data = (dataframe)
target = nome da coluna a ser utilizada (string)
n = numero de estados (padrão = 20)
plot = boleano (padrão = True)
output = (dataframe)

### casesNdeaths_mi(data)
gera um novo data com os valores de casos e óbitos por milhões de pessoas
input: data = (dataframe)
output:(dataframe)

### horizontal_barplot(data,estado,target,n,pasta,save)
gera um grafico de barras horizontais
input: data = (dataframe)
estado = sigla do estado (string) ou 0 para Brasil (int)
target = nome da coluna a ser utilizada (string)
n = numero de barras (padrão = 20)
pasta = nome da pasta a ser salva a imagem (string)
save = boleano (padrão = True)


### data_barplot(data,target,estado=0,municipio=0,pasta='estados',save=True,ticks=None,label=None)
gera grafico de barras por dia
input: data = (dataframe)
target = nome da coluna a ser utilizada
estado = sigla do estado (string) ou 0 para Brasil (int) - (padrão = 0)
municipio = nome do municipio (string) ou 0 para estado (int) - (padrão = 0)
pasta = nome da pasta a ser salva a imagem (string)
save = boleano (padrão = True)
ticks = espaçamento do eixo y (int) - (padrão = None)
label = nome do arquivo para salvar (string) - (padrão = None)


### data_lineplot(data,target,estado=0,municipio=0,pasta='estados',save=True,label=None)
gera grafico de linhas por dia
input: data = (dataframe)
target = nome da coluna a ser utilizada
estado = sigla do estado (string) ou 0 para Brasil (int) - (padrão = 0)
municipio = nome do municipio (string) ou 0 para estado (int) - (padrão = 0)
pasta = nome da pasta a ser salva a imagem (string)
save = boleano (padrão = True)
label = nome do arquivo para salvar (string) - (padrão = None)

### data_lineplot_v2(data,target,estado1,estado2,pasta='estados',save=True,label=None)
gera grafico de duas linhas
input: data = (dataframe)
target = nome da coluna a ser utilizada
estado1 = sigla do estado (string)
estado2 = sigla do estado (string)
pasta = nome da pasta a ser salva a imagem (string)
save = boleano (padrão = True)
label = nome do arquivo para salvar (string) - (padrão = None)


# referências
https://covid.saude.gov.br/

https://www.cdc.gov/coronavirus/2019-ncov/index.html
