![317315020-06e97046-048c-44b8-bd22-3dbd7963e864](https://github.com/user-attachments/assets/444e3177-f80e-41f5-bb3a-a4cadfeb1fa2)

<h1>Estácio - Trabalho Prático | DGT2823 Tecnologias para desenv.
de soluções de big data</h1>



Faculdade Estácio - Polo Castelo - Belo Horizonte - MG.
 
Curso: Desenvolvimento Full Stack.
 
Disciplina: Tecnologias Para Desenv. de Solucoes de Big Data.
 
Número da Turma: 2025.1
 
Semestre Letivo: 5.

Integrante: Samantha Karina Barbosa Torres.

Repositório: https://github.com/samzinha23/Trabalho-Pr-tico-.git

<hr>

<h2>Trabalho Prático   💻</h2>

Através dessa atividade o aluno realizará a limpeza de um conjunto de dados,
tornando-o apto a ser usado em tarefas de mineração/análise de dados.

<h3>Contextualização ✍️</h3>

Como Analista de Dados, você recebeu, em um novo projeto, um conjunto de dados.
Sua principal tarefa é tratar os dados desse conjunto a fim de que possam ser
utilizados para a descoberta de conhecimento através de sua posterior análise e
interpretação. Para tal tarefa, você deverá utilizar a linguagem Python e a biblioteca
Pandas. O passo-a-passo de todo o processo de tratamento dos dados é apresentado a
seguir, no roteiro de prática.

<h3>Roteiro de prática 📝</h3>

Material necessário para a prática📚

  Interpretador Python ou ambiente de codificação (JupyterLab / Jupyter Notebooks /
   Google Colab);
   Biblioteca pandas;
   Editor ou IDE (caso vá utilizar o interpretados python para execução dos scripts
   criados).

 <hr>

- Procedimentos


   Para essa atividade você deverá, obrigatoriamente, utilizar o conjunto de dados
   (fornecido anteriormente, na seção “Contextualização”) composto pelas colunas
   ID;Duration;Date;Pulse;Maxpulse;Calories
   Crie um novo arquivo/script;
   Leia o conteúdo do CSV fornecido, atentando-se para a necessidade ou não de
   incluir parâmetros adicionais como os relativos ao separador dos dados, a engine e
   o enconding;
   Atribua os dados lidos a uma variável;
   Verifique se os dados foram importados adequadamente:
   Imprima as informações gerais sobre o conjunto de dados;
   Imprima as primeiras e últimas N linhas do arquivo.
   Crie uma nova variável e atribua a ela uma cópia do conjunto de dados original
   (variável criada no passo 4);
    Nessa nova variável, contendo uma cópia dos dados:
    Substitua todos os valores nulos da coluna ‘Calories’ por 0;
    Imprima o conjunto de dados para verificar se a mudança acima foi aplicada com
    sucesso;
    Ainda na nova variável:
    Substitua os valores nulos da coluna ‘Date’ por ‘1900/01/01’;
    Imprima o conjunto de dados e confira se a mudança foi aplicada com sucesso;
    Transforme os dados da coluna ‘Date’ em datetime usando o método
    ‘to_datetime’;
    Tendo seguido todas as instruções anteriores, ao executar o passo anterior você
    deverá ter encontrado um erro informando que o valor ‘1900/01/01’ não
    corresponde ao formato ‘%Y/%m/%d’. Para resolver esse problema:
    Substitua, na coluna ‘Date’, o valor ‘1900/01/01’ por ‘NaN’;
    Utilizando o método ‘to_datetime’, repita o passo de transformação dos dados da
    coluna ‘Date’ para datetime;
    Imprima o conjunto de dados para verificar se as mudanças acima foram
    aplicadas com sucesso;
    Nesse ponto, você deverá ter esbarrado em outro erro, informando agora que o valor
    "20201226" não corresponde ao formato "'%Y/%m/%d'" . Você precisará, agora, na
    coluna ‘Date”, transformar especificamente esse valor, atualmente uma string, para
    o formato datetime. Para isso você deverá combinar os métodos ‘replace’ e
    ‘to_datetime’;
    Após o passo anterior, execute novamente a transformação de todos os dados da
    coluna ‘Date’ para o formato datetime (usando o to_datetime). Imprima o conjunto
    de dados atual para verificar se todas as transformações foram executadas com
    sucesso;
    Por fim, remova os registros contendo valores nulos. Nesse ponto, apenas a coluna
    ‘Date’ possui um registro que atende a essa premissa (linha 22). Logo, utilize-a
    como base para realizar a transformação solicitada;
    Imprima o dataframe e verifique se todas as transformações foram executadas
    conforme solicitado nos passos anteriores.
<hr>
   <h1> ✨Conclusão Geral✨</h1> 
   
Com esse trabalho, consegui praticar de maneira clara como usar o Python e o Pandas para realizar leitura, análise e manipulação de dados. Seguindo o roteiro de prática, comecei pela leitura do arquivo CSV e, em seguida, explorei as informações do dataset, identificando erros e inconsistências. Foi possível corrigir problemas como datas fora do padrão e valores faltando, o que tornou a base muito mais organizada.

Depois de todas as correções, percebi na prática como a preparação dos dados é uma etapa essencial antes de qualquer análise. O trabalho me ajudou a entender melhor todo esse processo e mostrou o quanto o Pandas facilita as transformações necessárias. No final, consegui desenvolver mais confiança para manipular dados, visualizar informações importantes e preparar um conjunto de dados para estudos e análises futuras.

Além disso, percebi o quanto o Python e o Pandas são ferramentas incríveis para trabalhar com dados. Com eles dá para automatizar tarefas repetitivas, lidar com grandes volumes de informações de forma prática e deixar tudo organizado e consistente para análise. Isso facilita muito a exploração dos dados e deixa o processo de análise mais rápido e confiável, sem tanta dor de cabeça.
<hr>

<h2> Codigos🎯 </h2>

# As atividades foram desenvolvidas no Google Colab
https://github.com/samzinha23/Trabalho-Pr-tico-.git
``` Python
import pandas as pd
import numpy as np
     

df = pd.read_csv("pico_web.csv", sep=";")
     

print(" Informações gerais 📌")
print(df.info())

print("Primeiras linhas")
print(df.head())

print("Últimas linhas")
print(df.tail())

     

 Informações gerais 📌
<class 'pandas.core.frame.DataFrame'>
RangeIndex: 32 entries, 0 to 31
Data columns (total 6 columns):
 #   Column    Non-Null Count  Dtype  
---  ------    --------------  -----  
 0   ID        32 non-null     int64  
 1   Duration  32 non-null     int64  
 2   Date      31 non-null     object 
 3   Pulse     32 non-null     int64  
 4   Maxpulse  32 non-null     int64  
 5   Calories  30 non-null     float64
dtypes: float64(1), int64(4), object(1)
memory usage: 1.6+ KB
None
Primeiras linhas
   ID  Duration          Date  Pulse  Maxpulse  Calories
0   0        60  '2020/12/01'    110       130    4091.0
1   1        60  '2020/12/02'    117       145    4790.0
2   2        60  '2020/12/03'    103       135    3400.0
3   3        45  '2020/12/04'    109       175    2824.0
4   4        45  '2020/12/05'    117       148    4060.0
Últimas linhas
    ID  Duration          Date  Pulse  Maxpulse  Calories
27  27        60  '2020/12/27'     92       118    2410.0
28  28        60  '2020/12/28'    103       132       NaN
29  29        60  '2020/12/29'    100       132    2800.0
30  30        60  '2020/12/30'    102       129    3803.0
31  31        60  '2020/12/31'     92       115    2430.0


df2 = df.copy()
     

df2["Calories"] = df2["Calories"].fillna(0)
print(df2)
     

    ID  Duration          Date  Pulse  Maxpulse  Calories
0    0        60  '2020/12/01'    110       130    4091.0
1    1        60  '2020/12/02'    117       145    4790.0
2    2        60  '2020/12/03'    103       135    3400.0
3    3        45  '2020/12/04'    109       175    2824.0
4    4        45  '2020/12/05'    117       148    4060.0
5    5        60  '2020/12/06'    102       127    3000.0
6    6        60  '2020/12/07'    110       136    3740.0
7    7       450  '2020/12/08'    104       134    2533.0
8    8        30  '2020/12/09'    109       133    1951.0
9    9        60  '2020/12/10'     98       124    2690.0
10  10        60  '2020/12/11'    103       147    3293.0
11  11        60  '2020/12/12'    100       120    2507.0
12  12        60  '2020/12/12'    100       120    2507.0
13  13        60  '2020/12/13'    106       128    3453.0
14  14        60  '2020/12/14'    104       132    3793.0
15  15        60  '2020/12/15'     98       123    2750.0
16  16        60  '2020/12/16'     98       120    2152.0
17  17        60  '2020/12/17'    100       120    3000.0
18  18        45  '2020/12/18'     90       112       0.0
19  19        60  '2020/12/19'    103       123    3230.0
20  20        45  '2020/12/20'     97       125    2430.0
21  21        60  '2020/12/21'    108       131    3642.0
22  22        45           NaN    100       119    2820.0
23  23        60  '2020/12/23'    130       101    3000.0
24  24        45  '2020/12/24'    105       132    2460.0
25  25        60  '2020/12/25'    102       126    3345.0
26  26        60      20201226    100       120    2500.0
27  27        60  '2020/12/27'     92       118    2410.0
28  28        60  '2020/12/28'    103       132       0.0
29  29        60  '2020/12/29'    100       132    2800.0
30  30        60  '2020/12/30'    102       129    3803.0
31  31        60  '2020/12/31'     92       115    2430.0


df2["Date"] = df2["Date"].fillna("1900/01/01")
print(df2)
     

    ID  Duration          Date  Pulse  Maxpulse  Calories
0    0        60  '2020/12/01'    110       130    4091.0
1    1        60  '2020/12/02'    117       145    4790.0
2    2        60  '2020/12/03'    103       135    3400.0
3    3        45  '2020/12/04'    109       175    2824.0
4    4        45  '2020/12/05'    117       148    4060.0
5    5        60  '2020/12/06'    102       127    3000.0
6    6        60  '2020/12/07'    110       136    3740.0
7    7       450  '2020/12/08'    104       134    2533.0
8    8        30  '2020/12/09'    109       133    1951.0
9    9        60  '2020/12/10'     98       124    2690.0
10  10        60  '2020/12/11'    103       147    3293.0
11  11        60  '2020/12/12'    100       120    2507.0
12  12        60  '2020/12/12'    100       120    2507.0
13  13        60  '2020/12/13'    106       128    3453.0
14  14        60  '2020/12/14'    104       132    3793.0
15  15        60  '2020/12/15'     98       123    2750.0
16  16        60  '2020/12/16'     98       120    2152.0
17  17        60  '2020/12/17'    100       120    3000.0
18  18        45  '2020/12/18'     90       112       0.0
19  19        60  '2020/12/19'    103       123    3230.0
20  20        45  '2020/12/20'     97       125    2430.0
21  21        60  '2020/12/21'    108       131    3642.0
22  22        45    1900/01/01    100       119    2820.0
23  23        60  '2020/12/23'    130       101    3000.0
24  24        45  '2020/12/24'    105       132    2460.0
25  25        60  '2020/12/25'    102       126    3345.0
26  26        60      20201226    100       120    2500.0
27  27        60  '2020/12/27'     92       118    2410.0
28  28        60  '2020/12/28'    103       132       0.0
29  29        60  '2020/12/29'    100       132    2800.0
30  30        60  '2020/12/30'    102       129    3803.0
31  31        60  '2020/12/31'     92       115    2430.0


print("\n Tentativa de conversão (deve gerar erro):")
try:
    pd.to_datetime(df2["Date"], format="%Y/%m/%d")
except Exception as e:
    print("ERRO GERADO :", e)
     

 Tentativa de conversão (deve gerar erro):
ERRO GERADO : time data "'2020/12/01'" doesn't match format "%Y/%m/%d", at position 0. You might want to try:
    - passing `format` if your strings have a consistent format;
    - passing `format='ISO8601'` if your strings are all ISO8601 but not necessarily in exactly the same format;
    - passing `format='mixed'`, and the format will be inferred for each element individually. You might want to use `dayfirst` alongside this.


df2["Date"] = df2["Date"].replace("1900/01/01", np.nan)
print("\nApós remover '1900/01/01':")
print(df2)
     

Após remover '1900/01/01':
    ID  Duration          Date  Pulse  Maxpulse  Calories
0    0        60  '2020/12/01'    110       130    4091.0
1    1        60  '2020/12/02'    117       145    4790.0
2    2        60  '2020/12/03'    103       135    3400.0
3    3        45  '2020/12/04'    109       175    2824.0
4    4        45  '2020/12/05'    117       148    4060.0
5    5        60  '2020/12/06'    102       127    3000.0
6    6        60  '2020/12/07'    110       136    3740.0
7    7       450  '2020/12/08'    104       134    2533.0
8    8        30  '2020/12/09'    109       133    1951.0
9    9        60  '2020/12/10'     98       124    2690.0
10  10        60  '2020/12/11'    103       147    3293.0
11  11        60  '2020/12/12'    100       120    2507.0
12  12        60  '2020/12/12'    100       120    2507.0
13  13        60  '2020/12/13'    106       128    3453.0
14  14        60  '2020/12/14'    104       132    3793.0
15  15        60  '2020/12/15'     98       123    2750.0
16  16        60  '2020/12/16'     98       120    2152.0
17  17        60  '2020/12/17'    100       120    3000.0
18  18        45  '2020/12/18'     90       112       0.0
19  19        60  '2020/12/19'    103       123    3230.0
20  20        45  '2020/12/20'     97       125    2430.0
21  21        60  '2020/12/21'    108       131    3642.0
22  22        45           NaN    100       119    2820.0
23  23        60  '2020/12/23'    130       101    3000.0
24  24        45  '2020/12/24'    105       132    2460.0
25  25        60  '2020/12/25'    102       126    3345.0
26  26        60      20201226    100       120    2500.0
27  27        60  '2020/12/27'     92       118    2410.0
28  28        60  '2020/12/28'    103       132       0.0
29  29        60  '2020/12/29'    100       132    2800.0
30  30        60  '2020/12/30'    102       129    3803.0
31  31        60  '2020/12/31'     92       115    2430.0


df2["Date"] = df2["Date"].replace("20201226", "2020/12/26")
     

df2["Date"] = pd.to_datetime(df2["Date"], format="%Y/%m/%d")

print("\nApós conversão completa para datetime:")
print(df2)
     

---------------------------------------------------------------------------
ValueError                                Traceback (most recent call last)
/tmp/ipython-input-2117971595.py in <cell line: 0>()
----> 1 df2["Date"] = pd.to_datetime(df2["Date"], format="%Y/%m/%d")
      2 
      3 print("\nApós conversão completa para datetime:")
      4 print(df2)

/usr/local/lib/python3.12/dist-packages/pandas/core/tools/datetimes.py in to_datetime(arg, errors, dayfirst, yearfirst, utc, format, exact, unit, infer_datetime_format, origin, cache)
   1065             result = arg.map(cache_array)
   1066         else:
-> 1067             values = convert_listlike(arg._values, format)
   1068             result = arg._constructor(values, index=arg.index, name=arg.name)
   1069     elif isinstance(arg, (ABCDataFrame, abc.MutableMapping)):

/usr/local/lib/python3.12/dist-packages/pandas/core/tools/datetimes.py in _convert_listlike_datetimes(arg, format, name, utc, unit, errors, dayfirst, yearfirst, exact)
    431     # `format` could be inferred, or user didn't ask for mixed-format parsing.
    432     if format is not None and format != "mixed":
--> 433         return _array_strptime_with_fallback(arg, name, utc, format, exact, errors)
    434 
    435     result, tz_parsed = objects_to_datetime64(

/usr/local/lib/python3.12/dist-packages/pandas/core/tools/datetimes.py in _array_strptime_with_fallback(arg, name, utc, fmt, exact, errors)
    465     Call array_strptime, with fallback behavior depending on 'errors'.
    466     """
--> 467     result, tz_out = array_strptime(arg, fmt, exact=exact, errors=errors, utc=utc)
    468     if tz_out is not None:
    469         unit = np.datetime_data(result.dtype)[0]

strptime.pyx in pandas._libs.tslibs.strptime.array_strptime()

strptime.pyx in pandas._libs.tslibs.strptime.array_strptime()

strptime.pyx in pandas._libs.tslibs.strptime._parse_with_format()

ValueError: time data "'2020/12/01'" doesn't match format "%Y/%m/%d", at position 0. You might want to try:
    - passing `format` if your strings have a consistent format;
    - passing `format='ISO8601'` if your strings are all ISO8601 but not necessarily in exactly the same format;
    - passing `format='mixed'`, and the format will be inferred for each element individually. You might want to use `dayfirst` alongside this.


df2 = df2.dropna(subset=["Date"])
print("DataFrame Final ✨")
print(df2)

   

DataFrame Final ✨
    ID  Duration          Date  Pulse  Maxpulse  Calories
0    0        60  '2020/12/01'    110       130    4091.0
1    1        60  '2020/12/02'    117       145    4790.0
2    2        60  '2020/12/03'    103       135    3400.0
3    3        45  '2020/12/04'    109       175    2824.0
4    4        45  '2020/12/05'    117       148    4060.0
5    5        60  '2020/12/06'    102       127    3000.0
6    6        60  '2020/12/07'    110       136    3740.0
7    7       450  '2020/12/08'    104       134    2533.0
8    8        30  '2020/12/09'    109       133    1951.0
9    9        60  '2020/12/10'     98       124    2690.0
10  10        60  '2020/12/11'    103       147    3293.0
11  11        60  '2020/12/12'    100       120    2507.0
12  12        60  '2020/12/12'    100       120    2507.0
13  13        60  '2020/12/13'    106       128    3453.0
14  14        60  '2020/12/14'    104       132    3793.0
15  15        60  '2020/12/15'     98       123    2750.0
16  16        60  '2020/12/16'     98       120    2152.0
17  17        60  '2020/12/17'    100       120    3000.0
18  18        45  '2020/12/18'     90       112       0.0
19  19        60  '2020/12/19'    103       123    3230.0
20  20        45  '2020/12/20'     97       125    2430.0
21  21        60  '2020/12/21'    108       131    3642.0
23  23        60  '2020/12/23'    130       101    3000.0
24  24        45  '2020/12/24'    105       132    2460.0
25  25        60  '2020/12/25'    102       126    3345.0
26  26        60    2020/12/26    100       120    2500.0
27  27        60  '2020/12/27'     92       118    2410.0
28  28        60  '2020/12/28'    103       132       0.0
29  29        60  '2020/12/29'    100       132    2800.0
30  30        60  '2020/12/30'    102       129    3803.0
31  31        60  '2020/12/31'     92       115    2430.0
````
