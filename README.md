# Evaluar recomendador externo en Elliot

## Indice

- [Evaluar recomendador externo en Elliot](#evaluar-recomendador-externo-en-elliot)
  - [Indice](#indice)
  - [Preparación del entorno](#preparación-del-entorno)
  - [Pasos del tutorial](#pasos-del-tutorial)
  - [Ejecución del experimento](#ejecución-del-experimento)

Este repositorio contiene un ejemplo completo de cómo evaluar un modelo recomendador externo en la librería [Elliot](https://elliot.readthedocs.io/en/latest/index.html).

## Preparación del entorno

El tutorial que se muestra a continuación se ha ejecutado en un entorno con las siguientes características:

- Versión de Python 3.8.18
- Versión de tensroflow 2.3.2

Lo más aconsejable es preparar un entorno virtual con estas características usando [pyenv](https://github.com/pyenv/pyenv) y [virtualenv](https://github.com/pyenv/pyenv-virtualenv). Para instalar **elliot** hay que seguir las instrucciones publicadas en su [documentación](https://github.com/sisinflab/elliot#install-from-source).

## Pasos del tutorial

Para poder evaluar un modelo externo en *elliot*, este utiliza un `ProxyRecommender`. Este tipo de modelo utiliza un dataset donde se han calculado las predicciones para todo el dataset. La explicación de este tipo de modelos se encuentra en su [documentación](https://elliot.readthedocs.io/en/latest/guide/proxy_model.html).

En el ejemplo del tutorial se crea un modelo basado en factorización de matrices usando el dataset de Movielens 1M. Los pasos a seguir son:

1. **Preparar los datos para el `ProxyRecommender`.** Estos pasos se encuentran en el notebook `Prepare_RecSys_Model.ipynb`.
2. **Crear el fichero de configuración del experimento.** En el tutorial, el fichero que usaremos es `exp_configuration.yml`. Para saber cómo hacer una configuración de un experimento en *elliot*, se puede consultar su [documentación](https://elliot.readthedocs.io/en/latest/guide/config.html).
3. **Crear un script para ejecutar el experimento.** Por último, preparamos un script en python que ejecute el experimento que hemos configurado.

## Ejecución del experimento

Una vez que se han seguido los pasos del tutorial, solo hay que ejecutar el siguiente comando en el terminal:

```bash
python experimento.py
```
