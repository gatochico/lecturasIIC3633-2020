# Comentario de "A user-centric evaluation framework for recommender systems." (2011)

El paper trata sobre un Framework creado por los autores, el cual tiene como objetivo evaluar el rendimiento de un sistema recomendador ya implementado, sin embargo esta vez no basándose en métricas como las vistas a lo largo del curso, sino que basándose en la percepción de los usuarios sobre el sistema.

Esta percepción es evaluada mediante un cuestionario, el cual está por dividido por secciones que buscan evaluar diversos aspectos de un sistema recomendador que tienen que ver con la interacción con un usuario. Estas secciones son: __Recommendation Quality__, __Interface Adequacy__, __Interaction Adequacy__, __Information sufficiency and explicability__, __perceived usefulness__, __perceived ease of use__, __control and transparency__. Finalmente, también se provee con una versión reducida del Framework, en caso de que no haya tiempo para usar la versión completa. El paper propone como investigación a futuro el analizar las respuestas de los usuarios y ver el sesgo que pueden tener las influencias culturales y el dominio de los datos a recomendar sobre el comportamiento de los usuarios.

Nuevamente, el paper leido me parece bastante interesante, debido a que se enfoca en uno de los aspectos que uno suele olvidar o dejar de lado a medida que se inserta en el campo de los sistemas recomendadores: la percepción de los usuarios objetivo sobre el sistema. Uno tiende a enfocarse en métricas más 'objetivas' que apuntan a la __accuracy__ del modelo, o a disimuir su tiempo de ejecución, por ejemplo, y pierde la noción de que estos sistemas recomendadores terminarán la mayoría del tiempo siendo usados por usuarios en tiempo real. Por más optimizado que esté un sistema, no puede ser considerado exitoso si es que es mal calificado por los usuarios o no es adoptado por estos.

En particular, en este ámbito (evaluar la percepción de un usuario sobre un sistema), me interesan las decisiones tomadas acerca de la **privacidad** de los usuarios. En el paper "Making Decisions about Privacy; Information Disclosure in Context-Aware Recommender Systems" (2013), se demuestra que las preocupaciones por la privacidad y que un sistema avise al respecto tiene una influencia en la percepción que tiene un usuario con el sistema. Incluso, si se hace consciente a un usuario de la entrega de datos posiblemente privados, la satisfacción y confianza del usuario en el sistema decrece. Esto demuestra que la privacidad es un aspecto importante a tomar en cuenta en un sistema, algo que no puede ser medido sin Frameworks como el presentado en el paper.

## Referencias:

Bart P. Knijnenburg and Alfred Kobsa. 2013. Making Decisions about Privacy: Information Disclosure in Context-Aware Recommender Systems. ACM Trans. Interact. Intell. Syst. 3, 3, Article 20 (October 2013), 23 pages. DOI:https://doi.org/10.1145/2499670

  