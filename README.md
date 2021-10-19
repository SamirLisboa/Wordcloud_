# Wordcloud_SIMPLY CODE 
# A little test on wordcloud library to my graduation extesnsion project (Um breve teste usando a biblioteca wordcloud para o meu projeto de extensão da graduação)
# BEFORE YOU START TO CODE VERIFY IF YOU GET INSTALLED THE WORDCLOUD LIBRARY (Antes de "codar" verifique se você ja tem todos os pacotes instalados)
# cmd -> -pip --upgrade -q 
#         pip install wordcloud




# Importa os pacotes necessários (The packages)

```python
import matplotlib.pyplot as plt
from wordcloud import WordCloud, STOPWORDS
import sys, os
os.chdir(sys.path[0])
```

# Identifica o texto a ser aberto e lido (Indentify open and read the .txt archive)

```python
text = open('wordcloud.txt', mode='r', encoding='utf-8').read()
```

# Seta as palavras a serem puladas/excluidas do arquivo final (stopword setting)

```python
stopwords = STOPWORDS
```
# Seta as configurações de saída do arquivo png (final arvhive settings)

```python
wc=WordCloud(
        background_color='black',
        stopwords=stopwords,
        height = 600,
        width=400
        )
```

# Gera o arquivo final (Generate the final archive)        
```python
wc.generate(text)
wc.to_file('wordcloud_aqruivodesaida.png')
```
#Arquivo final gerado [primeiro teste]

![wordcloud_aqruivodesaida](https://user-images.githubusercontent.com/84924884/137898215-0f9fb0e7-2f39-4799-bf51-a0dd21b868e6.png)
