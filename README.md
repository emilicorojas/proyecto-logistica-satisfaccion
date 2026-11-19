# Logística y satisfacción en Olist

Proyecto integrador del Módulo I del Diplomado Métodos estadísticos y matemáticos para la ciencia de datos (Facultad de Ciencias, UNAM). Autor: Emiliano Corona Rojas.

## Preguntas

1. ¿Cómo se relaciona el tiempo de entrega de los pedidos con el nivel de satisfacción de los clientes?
2. ¿Existe una asociación entre los meses de mayor volumen de pedidos y el incremento en los retrasos de entrega?

## Contenido

| Archivo o carpeta | Qué contiene |
|---|---|
| `analisis_logistica_satisfaccion.ipynb` | El análisis completo: datos, limpieza, figuras e interpretaciones |
| `requirements.txt` | Versiones de las bibliotecas usadas |
| `resultados/` | Las figuras que genera el notebook |
| `.vscode/settings.json` | Hace que VS Code use el entorno `.venv` de esta carpeta |

## Cómo correrlo en VS Code

Se necesita Python 3.12, Git y VS Code con las extensiones **Python** y **Jupyter**.

0. Obtener el proyecto, clonándolo o descomprimiendo el zip:

   ```bash
   git clone https://github.com/emilicorojas/proyecto-logistica-satisfaccion.git
   ```

1. Abrir la carpeta `proyecto-logistica-satisfaccion` en VS Code (*File → Open Folder*).
2. Abrir una terminal en VS Code (*Terminal → New Terminal*) y descargar los datos de Olist dentro de esta carpeta:

   ```bash
   git clone https://github.com/olist/work-at-olist-data.git
   ```

   Para usar exactamente la versión del análisis (opcional): `git -C work-at-olist-data checkout d9e4980`.
   Sin Git, se puede descargar el ZIP desde la página del repositorio (*Code → Download ZIP*) y descomprimirlo aquí con el nombre `work-at-olist-data`.

3. Crear el entorno e instalar las dependencias:

   ```bash
   python -m venv .venv
   ```

   ```bash
   .venv\Scripts\python.exe -m pip install -r requirements.txt
   ```

   En macOS o Linux, el segundo comando es `.venv/bin/python -m pip install -r requirements.txt`.

4. Abrir `analisis_logistica_satisfaccion.ipynb`, elegir el kernel `.venv` (arriba a la derecha) y ejecutar *Restart* y luego *Run All*.

El notebook encuentra los datos solo: busca `work-at-olist-data/datasets` en esta carpeta y en las superiores, o en la ruta de la variable de entorno `OLIST_DATA_DIR`.

## Datos

Se usan dos tablas del conjunto público de Olist ([work-at-olist-data](https://github.com/olist/work-at-olist-data), licencia MIT): `olist_orders_dataset.csv` y `olist_order_reviews_dataset.csv`. Los CSV no se modifican; versión utilizada: commit `d9e4980`.

## Estado

El análisis de las dos preguntas está completo, con ocho decisiones de limpieza documentadas en el notebook. Falta la sección final de conclusiones y el registro de contribuciones.
