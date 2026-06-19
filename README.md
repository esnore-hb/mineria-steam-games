# Estudio a los usuarios de la plataforma Steam

En el presente repositorio se tienen los programas necesarios para responder
3 preguntas de un caso de estudio. Este caso de estudio es a los usuarios de la
plataforma de Steam.

Las preguntas que se estudiarion fueron:

- ¿Cuál es el tiempo de juego que dedican los usuarios de Steam? (playtime)
- ¿Qué factores influyen en la valoración de un juego y su reseña? (LikeReview)
- ¿Qué tipos de desarrolladores existen en la plataforma?  (developers)

Para ello, se dedican tres archivos `.ipynb` para poder responderlas, donde
las palabras en paréntesis se refieren a sus archivos respectivos.

## Pasos para poder ejecutar el código fuente

El primer paso es utilizar Visual Studio Code, luego clonar y abrir este
repositorio e instalar las extensiones recomendadas.

Luego de eso, establecer un ambiente necesario para poder ejecutar el código
Python, instalando los `requirements.txt`.

```bash
python -m venv .venv
source .venv/bin/activate # En linux
pip install -r requirements.txt
```

Finalmente, decirle a Visual Studio Code que use este ambiente de Python como
su Kernel.

### Playtime

No se puede ofrecer una solución directa más que workarounds si es que se desea
ejecutar en Colab, pues existe un tratamiento a los datos hecho por el archivo
`clean.py` que, por ejemplo, traduce los géneros que existen en Steam fila a
fila. Este archivo es vital para poder tener un mejor estudio, pero por
implementación no se decidió colocar en el `.ipynb` dada su extensión.

### LikeReview

Si al momento de querer ejecutar este código no se posee una tarjeta gráfica
dedicada, es recomendable usar Colab. Si se puede subir el archivo directamente
y no debería tener problemas (probado con `runtime T4 GPU`). Esto debido al
paquete `torch`, dada su naturaleza computacional, se beneficia del
procesamiento paralelo que ofrece este hardware.

### Developers

No se requieren consideraciones adicionales para ejecutar este código. Se puede
omitir la sección Exploración de datos si solo se quieren evaluar los modelos.
