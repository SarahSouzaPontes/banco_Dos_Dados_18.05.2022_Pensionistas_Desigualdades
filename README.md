# banco_Dos_Dados_18.05.2022_Pensionistas_Desigualdades
Banco_Dos_Dados_18.05.2022_Pensionistas_Desigualdades

CARACTERÍSTICAS DOS BENEFICIÁRIOS E TIPO DE BENEFÍCIOS
PENSIONÁRIOS

INTRODUÇÃO


O Brasil, de acordo com o seu perfil sociodemográfico, vem apresentando uma
transição demográfica em que a sua teoria tradicional possui três postulados centrais, o
primeiro consiste na queda da mortalidade, o segundo na transição reprodutiva, e o terceiro
nas influências do crescimento econômico. No primeiro, as melhorias do saneamento básico e
a erradicação e controle de doenças diminui consideravelmente as elevadas taxas de
mortalidade, principalmente infantil. O segundo baseia-se no retardamento dos casamentos e
o controle da fecundidade desses indivíduos. E o terceiro, baseado no êxodo rural e
crescimento da população urbana causam efeitos no incremento da queda das taxas
fecundidade.
Ou seja, todas as teorias acabam se baseando na redução na questão da transição da
fecundidade que podem ser correlacionadas pela escassez ou ausência de perspectivas
financeiras gerando novos padrões de comportamentos reprodutivos e difusão do uso dos
métodos contraceptivos. Associado a isso, o envelhecimento da população o economicamente
ativa e aumento do número das doenças crônicas, degenerativas e exaustivas gera
perspectivas questionáveis do quanto a previdência social do país pode suportar e sustentar
essa população que por sua vez pode necessitar desse benefício visto a necessidade e
demanda de um número cada vez maior de recursos.
Pois, é pouco conhecido o perfil desse beneficiário nesse momento, assim como suas
características sociodemográficas. Desta forma, o seguinte estudo tem como objetivo analisar
a prevalência das características dos beneficiários, tipo de pensão, correlacionar o
rendimento bruto, idade do servidor, escolaridade e pagamento suspenso do benefício.

METODOLOGIA

Estudo transversal descritivo, utilizando os dados datalake público com recorte de
tempo de 1994 a 2021 Serão analisadas variáveis como data de nascimento e falecimento do
servidor, tipo de beneficiário, rendimento líquido e pagamento suspenso. Será avaliada a
correlação entre as variáveis considerando o valor de p 0,05 para significativa
estatisticamente.
Toda análise de dados se encontra disponível no GitHub (repositório:
https://github.com/SarahSouzaPontes/banco_Dos_Dados_18.05.2022_Pensionistas_Desigua
ldades). Os dados foram secundários do datalake público
(https://basedosdados.org/dataset/br-me-pensionistas?bdm_table=microdados), banco dedados realizado o download (https://basedosdados.org/dataset/br-me-pensionistas) em
formato CSV e analisado via Google Colab através da Linguagem Python.
A variável pagamento suspenso foi descrita de forma dicotômica "sim" ou "não" e na
análise descritiva através da frequência e histograma foi possível verificar a discrepância
entre valores. Optamos assim por balancear os dados para não favorecer o overtraining dos
valores mais frequentes (não) e underfitting ("sim").
Os modelos selecionados para verificar a fase do projeto de Machine Learning foram:
Regressão Linear Múltipla. O modelo de aprendizagem de máquina apresentou acurácia de
99% (0.999994 (0.000009)). Foram selecionadas como variáveis target pagamento suspenso
do benefício e variáveis independentes rendimento bruto e idade do servidor.

RESULTADOS

O formato do banco de dados analisados constou de 310.003 linhas e 30 colunas com
variáveis tais como: ano, mês, nome do servidor, cpf do servidor, data de nascimento e
falecimento do servidor, matrícula, nome do órgão, sigla do órgão, código do órgão
superior, cargo do servidor, escolaridade, classe, padrão, referência, nível, ocorrência,
nome, cpf, data de nascimento, sigla vinculação, tipo do beneficiário, natureza da pensão,
data de início e fim do benefício, rendimento bruto e líquido e pagamento suspenso. O
dataset constava de 15,9% de missing (visualizadas pelo Relatório da biblioteca do Pandas
Profilling).
A tabela foi reduzida com intuito de analisar dados mais específicos e dirigidos ao
objeto do estudo, data de nascimento e falecimento do servidor, tipo de beneficiário,
rendimento líquido e pagamento suspenso. Assim, calculado a idade apresentando uma média
de 56 anos após imputar a moda nos dados faltantes de nascimento e utilizar a biblioteca date
time para substituir a data atual nas células do dataset na coluna fim do benefício não
preenchidas. Foram observados outliers, considerando inconsistências, pois o valor mínimo
da idade era de -28 e valor máximo de 180, optamos por considerar dados no intervalo de 18
a 120 anos, pois a idade possível de exercer cargos laborais e o limite superior justifica-se
pela idade historicamente mais tardia de um indivíduo vivo.
Analisado a variável tempo de benefício com uma média de 39 anos, desvio padrão
de 13 e valor mínimo de -193 e máximo de 128 anos, decidimos excluir todos valores abaixo
de 0, uma vez que não há coerência nos dados com tempo de benefício negativo. As
características mais prevalentes dos beneficiários eram: viúvas, filha maior solteira sem
cargo público, filho, filha, companheira (o), filho invalido e viúvo variando de 137.788
indivíduos a 2.611 mil. As demais categorias representavam menos de 2.500 tipos de benefícios  entre 34 categorias como mãe, enteado, irmã viúva, pai, sobrinhos menores entre
outras.
Os tipos de pensão mais prevalentes fora
3373/58, e Lei 8112/90.
A Lei nº 3.373/1958 c/c a Lei nº 6.782/1980 estabelece que, em caso de óbito de
servidor público, as suas filhas solteiras e maiores de 21 anos possuem direito ao recebimento
de pensão. A Lei n.º 8.112/90,descreve os beneficiários da pensão por morte, os filhos, ou
enteados do servidor falecido, até 21 anos de idade, ou inválidos,de acordo com a
permanência da invalidez, devido às Leis 3373/58 com 6782/80, Lei
Realizada uma nova formatação do
bruto, idade do servidor, escolaridade do cargo e pagamento suspenso, transformadas em
variáveis dummies. Foram normalizadas as variáveis rendimento bruto e idade do servidor,
por serem numéricas. Avaliada a correlação entre as variáveis apresentand
significativa estatisticamente e positiva para


###GRÁFICO###
Fonte: Produzido pela autora.
Figura 2. Correlação entre as variáveis


CONCLUSÃO
Os beneficiários são mais representativos viúvas, filha
público, filho, filha, companheira (o), filho invalido e viúvo e o tipo de benefício devido: Leis
3373/58 com 6782/80, Lei 3373/58 isolada e Lei 8112/90.

