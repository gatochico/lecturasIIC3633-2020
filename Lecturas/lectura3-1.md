# Comentario "Performance of recommender algorithms on top-N recommendation tasks" (2010)

Este paper trata sobre cómo medir el rendimiento de algorithmos recomendadores al momento de pedir listas de recomendaciones (top-N) de _items_. 

Los autores indican que metodologías basadas en el cálculo del error (como MAE (_Median Absolute Error_) o RMSE (_Root Median Square Error_)) no son un buen marcador del rendimiento al momento de evaluar la recomendación de un Top-N, sino que se deben usar metodologías basadas en métricas de _accuracy_, como por ejemplo _precision_ y _recall_. Esto lo ponen a prueba entrenando y comparando varios modelos, entre ellos modelos con los mejores rendimientos a nivel de RMSE, como SVD++ por ejemplo, y modelos que no están optimizados en base a RMSE, como PureSVD, usando los mismos _datasets_. 

Los resultados que obtienen indican que cuando la tarea pedida es generar un _Ranking_, algoritmos que tenían bajo rendimiento según RMSE consistentemente funcionaban mejor que los algoritmos que RMSE denominaba como mejores. En específico, PureSVD fue el con mejor resultados. Los autores ofrecen como explicación que RMSE _testing_ tiene limitaciones, como el solo tomar en cuenta los items que el usuario sí ha evaluado de forma previa y saltando los items que nunca se han evaluado dentro. Mientras que en realidad estos _missing items_ sí deberían incluise en el entrenamiento, cosa que sí hacen modelos como PureSVD, que incluyen a todos los items y usuarios del espacio. Por lo tanto, se confirma que al momento de evaluar modelos, no se debe basar en una única métrica como RMSE.

Dentro de los aspectos que me parecieron interesantes del paper, está la separación de objetos del dataset entre **_Head_** y **_Tail_**, ya que no es lo mismo recomendar algo popular (que serían los items con mayor cantidad de _Ratings_) a un usuario que recomendar _items_ menos conocidos. Esto me pareció interesante ya que incluye el concepto de la otra lectura de la semana (Recommender Systems Handbook) de **_Novelty_** y de **_Serendipity_** dentro de las formas en que se evalúa un modelo. 

Lo que en particular hace este paper es separar el dataset entre **_Short Head_** que inlcuye la minoría de items más populares y **_Long Tail_**, que incluye al resto de los items, con el fin de analizar la inlfuencia que tiene en el modelo la inclusión de items de la **_Short Head_**. El resultado es que efectivamente ciertos modelos, como NNCosNgbr, bajan su efectivar al excluir esta caveza. Incluso, hay un modelo CorNgbr cuyo rendimiento aumenta al concentrarse en la cola en vez del dataset completo. Sin embargo, el algoritmo con mejor rendimiento en general, PureSVD, fue el _top performer_ ya sea incluyendo o sacando estas cabezas.

Este concepto de _Tail_ y _Head_ no es nuevo: Este fue popularizado en el libro [Long Tail: Why the Future of Business is Selling Less of More](https://dl.motamem.org/long_tail_chris_anderson_motamem_org.pdf) (2006), donde se habla del concepto y su influencia en la economía y mercado. Incluso, si se desea buscar sobre el término en el ámbito de sistemas recomendadores, en el siguiente [paper](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.168.5009&rep=rep1&type=pdf) (2008), ya se comienza a analizar el efecto de la popularidad en las recomendaciones. En dicho paper se comprueba que modelos de collaborative filtering son propensos a tener un _popularity bias_, mientras que otros approaches (content-based y human expert-based) permiten llegar de forma más facil a items de la cola a partir de items en la cabeza.

Para cerrar, el paper me parece un tema interesante, ya que hasta ahora habíamos estado analizando recomendaciones basándonos en métricas como RMSE basadas en error, e ignorando aspectos de los datasets como _popularity bias_. Por lo tanto, la inclusión de estas lecturas permite expandir nuestros conocimientos con respecto a la forma en cómo evlauar los modelos dependiendo de qué forma se usarán (predecir ratings, o generar rankings, por ejemplo).

## Referencias:

Long Tail: Why the Future of Business is Selling Less of More. Chris Anderson (2006).
From Hits to Niches? Or how popular artists can bias music recommendation and discovery. Cano, Celma (2008).