# 1-Sistema-Clasificación-Textos
1. [Instalación librería NLTK](#schema1)
2. [Caso Práctico Clasificación Textos – Tokenizar](#schema2)


<hr>

<a name="schema1"></a>


## 1. Instalación librería NLTK

1. Creación de un entorno virtual:
```bash
virtualenv mi_entorno
```
2. Activación del entorno virtual:
```bash
source mi_entorno/bin/activate

```
3. Instala NLTK:
```bash
pip install nltk

```

4. Instalar los paquetes de NLTK

```python
import nltk
nltk.download(all)
```
<hr>

<a name="schema2"></a>

## 2. Caso Práctico Clasificación Textos – Tokenizar
Análisis página web: https://librefinanciero.com
1. Tokenizar Texto:

  - Dividir el texto en “tokens”, es decir, piezas más pequeñas (se puede tokenizar por palabraso por sentencias)

    - La casa de Juan es blanca --> La - casa – de – Juan - es – blanca (6 Tokens)
  - Crear tokens por palabras, con `word_tokenize`hacemos la division del texto en tokens.
  ```python
    from nltk.tokenize import word_tokenize
    tokens = word_tokenize(text,"spanish")
    tokens=[word.lower() for word in tokens if word.isalpha()] # Remover los signos de puntuación
    print(tokens)
  ```