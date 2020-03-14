# Epidemia, nube radiactiva y distanciamiento social



El propósito de este post (algo inusual) es ilustrar de forma sencilla la increíble eficacia potencial de las medidas de distanciamiento social (limitar las reuniones, la higiene, el teletrabajo, el cierre de escuelas...) ante una epidemia que se convierte en pandemia.

Una epidemia es una reacción en cadena, y esto cambia todo sobre el impacto potencial de tales medidas, en comparación con otras fuentes de peligro.

Para entender esto, imaginemos otra situación: asumamos que no nos enfrentamos a una epidemia, sino a otro tipo de peligro, digamos una nube radioactiva (o química). Debido a la presencia de la nube, imaginemos que se vuelve arriesgado salir, que podría hacernos enfermar, o incluso eventualmente matarnos. (Y supongamos que encerrados en casa estamos a salvo).

El gobierno decide tomar medidas para confinar a la gente a sus casas: cerrar algunas escuelas, fomentar el teletrabajo, invitar a la gente a posponer sus viajes, reuniones, etc.).

En este caso, se puede imaginar legítimamente que las vidas salvadas serán proporcionales a la intensidad de los esfuerzos:

* Si el 10% de la gente se queda en casa, evitaremos el 10% de las muertes;
* Si el 50% de la gente se queda en casa, evitaremos el 50% de las muertes.
* Si el 95% de la gente se queda en casa, evitaremos el 95% de las muertes.

El efecto es lineal.

Una epidemia no es así en absoluto. Una epidemia es una reacción en cadena, implica que hay un efecto umbral en la eficacia de las medidas, y este efecto umbral es muy fuertemente no lineal.

Incluso cuando se está familiarizado con las matemáticas asociadas, es bastante difícil imaginar este efecto umbral, así que tomemos un ejemplo concreto de un modelo epidemiológico.

El modelo que voy a usar se llama el modelo SIR. Es uno de los modelos más simples, y el uso que voy a hacer de él no es predictivo. No estoy tratando de predecir el número de muertes o el número de personas infectadas: el modelo es demasiado simple, los parámetros serán demasiado imprecisos.

Voy a utilizarlo con fines educativos, para ilustrar esta noción de umbral, y cómo las medidas de distanciamiento social pueden tener un efecto increíblemente efectivo, nada proporcional al esfuerzo como en el caso de la nube radiactiva.


En este modelo, consideramos que hay 3 poblaciones: la sana, la infectada y la remitida (la que ha tenido el virus y se ha recuperado). Y modelaremos dos fenómenos simples:

    Las personas infectadas infectarán a las personas sanas.
    Las personas infectadas se curarán gradualmente.

Para esto, necesitamos 3 parámetros:

    Duración D de la enfermedad, durante la cual somos contagiosos.
    El número promedio C de contactos que tenemos con otras personas cada día.
    La probabilidad P de que un contacto entre una persona infectada y una persona sana conduzca a una transmisión del virus.

Estos parámetros a menudo no se conocen con precisión y dependerán de la definición precisa de lo que se denomina "contacto". Pero verás que no es muy importante.

Tomemos una persona infectada: cada día se cruzará con gente C, a la que contaminará con una probabilidad de P. Y esto ocurrirá durante cada uno de los días D que dure su enfermedad.

El número total de personas que infectará será, por lo tanto, el producto de estos tres términos, que tradicionalmente anotamos como R0

R_0 = C por P por D.



Este parámetro se denomina tasa de reproducción, e incluso sin ejecutar el modelo matemático, no es muy difícil convencerse de que tiene una influencia decisiva en el destino de la epidemia.

Si vale la pena decir 2: cada persona infectada contaminará a 2 personas, que a su vez contaminarán a 2 personas, que a su vez contaminarán a 2 personas, etc., entonces no es muy difícil convencerse de que tiene una influencia decisiva en el futuro de la epidemia. Hay una reacción en cadena, el número de enfermos aumenta exponencialmente, la epidemia explota.

Ahora bien, si este coeficiente es inferior a 1: cada persona infectada dará la enfermedad a menos de una persona, por lo que el número neto de enfermos disminuirá y gradualmente la epidemia se extinguirá.

Hay un efecto umbral monstruoso. Para extinguir una epidemia "naturalmente", el R0 debe estar por debajo del fatídico umbral de 1, así que ¿cuánto es el R0 en el caso de Covid-19? No lo sabemos exactamente. Probablemente entre dos y cuatro.

Pero como se puede ver, este valor no es intrínseco a la enfermedad, sino que depende de factores de comportamiento: cuántos contactos diarios, qué probabilidad hay de que se produzca la transmisión.


Adoptando medidas de distanciamiento social (menos contacto, mantenerse más lejos, higiene, eliminar reuniones y encuentros innecesarios, cerrar escuelas, teletrabajo, etc.), el R0 puede ser muy fácilmente bajado.

Y el punto clave aquí es que el beneficio no será en absoluto proporcional al esfuerzo. Si se hace lo suficiente para caer rápidamente por debajo del umbral, la recompensa está ahí.

Imaginemos que el R0 es inicialmente 2.5. Es una suposición razonable para Covid-19. Si logramos dividirlo por 4, podemos detener la propagación de la epidemia muy, muy rápidamente.

Dividir el R0 por 4 está lejos de ser inaccesible: puede significar, por ejemplo, tener la mitad de contactos y hacer que la probabilidad de transmisión se divida por 2 (por una mayor distancia y atención a la higiene).

Para ilustrar bien este punto, me divertí al poner un modelo de tipo SIR en Excel (DESCARGAR AQUÍ, si no, ver el final del billete), tomando como punto de partida la situación aproximada en Francia el 11/03/2020.

Una vez más, el objetivo no es hacer predicciones, es para que puedas ver por ti mismo, a través de la experimentación "numérica", que este efecto de umbral R0 es monstruoso. Así que esto es un "modelo de juguete".


Tomemos un R0 de 2.5. Esto se puede obtener diciendo que la enfermedad dura 10 días, y que cada día hay 50 contactos con una probabilidad de transmisión del 0,5%. Estas dos últimas cifras no son importantes, es el producto de las dos que cuenta.

El gráfico siguiente representa el número acumulado de casos en función del tiempo (en días a partir de hoy) en Francia, si nos quedamos en un R0 de 2,5. (¡Esto no es una predicción, es un "modelo de juguete"!)

Podemos ver que en 6 meses, casi todos habrán contraído la enfermedad. Con una tasa de mortalidad del 3%, hay casi 2 millones de muertes (¡Esto no es una predicción, es un "modelo de juguete"!).

Ahora imaginemos que ahora podemos conseguir inmediatamente dividir el R0 por 4: la mitad de contactos, y contactos más distantes que reducen a la mitad la probabilidad de transmisión. Eso no parece inalcanzable, ¿verdad? El R0 será entonces 0.62. Y aquí está el resultado

El límite es de 6000 casos acumulados, y por lo tanto 180 muertes con una tasa de mortalidad del 3% (¡Esto no es una predicción, es un "modelo de juguete"!).

Una monstruosa, enorme diferencia. Totalmente desproporcionado en comparación con el cambio inicial que hicimos ("simple" reducción a la mitad de los contactos y transmisiones).

Un brote es una reacción en cadena. Las medidas de distanciamiento social pueden tener un efecto totalmente desproporcionado. Esto es muy, muy, muy diferente del caso de la nube radiactiva, donde las medidas de contención tendrían un efecto esencialmente lineal.

Y esto está obviamente ligado al hecho de que en el caso de la nube, al ser cuidadoso sólo te proteges a ti mismo. Aquí protegemos a todos.

Eso es todo lo que quería ilustrar. Toma el modelo de Excel, juega con él. Es sólo un modelo, el más simple de todos en epidemiología. NO tiene ningún valor predictivo sobre los detalles de los números. Está ahí para ilustrar el principio de la reacción en cadena, que está en el corazón de la noción de una epidemia. Los detalles del modelo no son importantes, este efecto de reacción en cadena existe en todos los modelos.

Bajar el R0 rápidamente es muy accesible, sin caer necesariamente en una situación de "país muerto" o "ley marcial". Creo que el cierre de escuelas e instituciones educativas podría crear la señal necesaria para que todos se involucren. Y en pocas semanas se doblaría.

Descargue el modelo de juguete. Juega con él. Compruébelo usted mismo.

Edición del 13/03/2020: Mucha gente ha hecho pequeñas aplicaciones que ilustran el modelo de forma interactiva:

[https://jflorian.shinyapps.io/SIRmodel/](https://jflorian.shinyapps.io/SIRmodel/)

[https://sciencetonnante-epidemie.netlify.com](https://sciencetonnante-epidemie.netlify.com)

[https://epidemic.phoenix-it-services.com](https://epidemic.phoenix-it-services.com)
