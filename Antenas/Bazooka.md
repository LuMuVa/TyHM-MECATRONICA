# Diseño de linea de transmision de antena 
## Factores a tener en cuenta
1. **Frecuencia de operacion**: La frecuencia de operación es 27.46 MHz, lo que corresponde a una longitud de onda (λ = v / f) de aproximadamente 10.91 metros en el vacío.
v = f λ
λ = v / f
* v es la velocidad de la luz en el vacío (3×10^8 m/s),
* f es la frecuencia de operación (27.46 MHz).
** Esto da una longitud de onda de 10.91 metros.**
2. **Longitud de la línea de transmisión**: La longitud de la línea debe ser una fracción de la longitud de onda. Dependiendo de la aplicación, puede ser λ/4, λ/2 o una longitud completa de la onda. En este caso, una longitud común es de λ/2, lo que sería aproximadamente 5.45 metros. Esto se ajustará según la longitud real de la antena y la distancia al equipo.
3. **Impedancia de la línea de transmisión**: La impedancia de la línea debe coincidir con la impedancia de la antena (50 ohms) para evitar pérdidas por reflexión. El tipo de cable (coaxial, de par trenzado, microstrip, etc.) debe ser elegido en función de la impedancia característica y de las condiciones de instalación.
* Si se utiliza un cable coaxial, es común utilizar un cable coaxial con impedancia de 50 ohms. Algunos ejemplos incluyen cables como RG-58 o LMR-400, que son adecuados para frecuencias de 27.46 MHz.
* Para una línea de transmisión de microstrip, la impedancia se puede ajustar mediante el ancho de la pista y el grosor de la substratación.
6. **Pérdidas y materiales**: Se deben considerar las pérdidas en la línea de transmisión, que dependen del material conductor y dieléctrico. En general, materiales con baja conductividad y constante dieléctrica baja serán preferidos para minimizar las pérdidas.
7. **Conexión de la antena**: Asegurarse de que el punto de conexión entre la antena y la línea de transmisión tenga una impedancia de 50 ohms para evitar desajustes de impedancia que causen pérdidas de potencia.
##  Diseño teniendo en cuenta que es para un cuarto de estudiante 
Para diseñar una línea de transmisión en un cuarto de estudiante con las condiciones techo a 6 m de altura y dimensiones de 4x4 m, se deben tomar en cuenta varios factores:
1. **Longitud de la línea de transmisión**: Dado que la frecuencia de operación es de 27.46 MHz, la longitud de onda es de aproximadamente 10.91 metros, como se calculó anteriormente. Si se va a utilizar una línea de transmisión con una longitud de λ/2, esta debería ser de unos 5.45 metros.
2. **Tipo de línea de transmisión**:
* Si la línea de transmisión es cable coaxial, se puede utilizar un cable estándar como RG-58 o LMR-400, ambos con una impedancia de 50 ohms. El cable puede ser fácilmente instalado en el cuarto sin grandes restricciones.
* Si se desea hacer una línea de transmisión de microstrip, se puede usar una placa de sustrato, por ejemplo, un PCB de FR4, con las dimensiones y la distribución adecuadas para que la impedancia sea de 50 ohms. Sin embargo, las líneas de transmisión de microstrip suelen ser más difíciles de implementar en un espacio pequeño sin un equipo adecuado.
3. **Ubicación y rutas del cable**:Dado que el techo está a 6 metros de altura y el cuarto tiene 4x4 metros, es importante asegurarse de que el cable coaxial o la línea de transmisión no cause interferencias o molestias. Puedes aprovechar el espacio vertical para elevar el cable hacia el techo y minimizar el impacto visual y físico. Si es posible, instalar el cable por las esquinas o a lo largo de las paredes.
 * Si la línea de transmisión debe recorrer un trayecto largo, como una distancia desde un equipo hasta la antena, asegúrate de que el cable tenga suficiente longitud para llegar a la antena sin que se doble excesivamente ni se convierta en una fuente de pérdidas adicionales.
4. **Antena y altura**:Dado que el techo tiene una altura de 6 metros, se puede montar la antena en esa altura para mejorar la propagación de la señal. Si se está utilizando una antena tipo dipolo o una antena de tipo vertical, aseguarase de que la antena esté bien posicionada para optimizar la radiación. Si la antena es muy grande, tal vez se deba buscar un modelo compacto adecuado para el espacio disponible.
5. **Ajustes de impedancia**: Es crucial que la impedancia de la línea de transmisión coincida con la de la antena (50 ohms) para evitar pérdidas. En un cuarto pequeño, se debe asegurar de que las conexiones entre la antena y la línea de transmisión estén bien aseguradas y libres de desajustes.
6. **Posibles limitaciones**: Considerando que el cuarto tiene dimensiones de 4x4 metros, es importante gestionar bien el espacio para evitar interferencias con otros equipos electrónicos o limitaciones de espacio físico para el cableado y la antena.

Si la longitud de la línea de transmisión excede la distancia disponible, también se pueden considerar soluciones como antenas más cortas o el uso de materiales para reducir las pérdidas

# Comparacion entre antena Bazooka y antena Zepelli
| Aspecto                    | Bazooka                              | Zepp                                  |
| -------------------------- | ------------------------------------ | ------------------------------------- |
| Impedancia de entrada      | \~50 ohm                             | \~2000 ohm (sin adaptación)           |
| Necesita adaptador (balun) | No (alimentación directa)            | Sí                                    |
| ROE (SWR) típico           | Bajo                                 | Alto sin adaptación                   |
| Facilidad de construcción  | Media                                | Fácil a nivel mecánico                |
| Banda pasante              | Amplia                               | Estrecha                              |
| Eficiencia                 | Alta                                 | Alta si se adapta bien                |
| Ideal para                 | Operación multibanda o sin acoplador | Instalaciones fijas bien sintonizadas |
## Recomendación 
* Si se está trabajando en frecuencia fija (27.46 MHz) y tenés un acoplador, la Zepp puede darte buena eficiencia.

* Pero si querés alimentación directa con 50 ohm, baja ROE, y más flexibilidad sin ajustar tanto, la Bazooka es más conveniente y amigable con los equipos modernos.

# Inconveniente
Al realizar la antena (de largo total de 5m y largo interior de 3,6m) y probarla nos encontramos con el incoveniente de que en vez de resonar a 27.46MHz que era lo esperado, fianlmente resonó a 22,3MHz.
Los factores que pueden estar implicados en esta variación podrian ser:
1. **Longitud de la antena**: La frecuencia de resonancia de una antena está inversamente relacionada con su longitud. La longitud de la antena debe ser un múltiplo o fracción de la longitud de onda de la frecuencia deseada. En este caso, la longitud de la antena se calculó para alcanzar una frecuencia de 27 MHz, pero la longitud real de la antena fue de 5 metros, lo que corresponde a una frecuencia resonante más baja, ya que la longitud es menor de lo esperada.
2. **Longitud de los elementos**: La antena Bazooka está compuesta por un dipolo que generalmente tiene dos elementos coaxiales. Si los elementos internos fueron demasiado cortos o mal dimensionados, esto podría haber desplazado la frecuencia de resonancia hacia una frecuencia más baja.
3. **Impedancia y carga capacitiva**: La configuración y el diseño del coaxial pueden influir en la impedancia de la antena. Si la impedancia no es la correcta o si hay un desajuste en la carga capacitiva, la frecuencia resonante podría no coincidir con la calculada.
4. **Condiciones ambientales**: Factores como la altura de instalación, la proximidad a objetos metálicos o el entorno de la antena también pueden afectar la frecuencia de resonancia. Aunque el diseño teórico indique una resonancia a 27 MHz, la antena podría estar influenciada por el entorno, desplazando su frecuencia de resonancia.
5. **Error en el cálculo de la longitud**: El cálculo de la longitud de la antena se basa en la suposición de que la velocidad de la señal es la misma en el aire. Sin embargo, si la
antena no está construida con precisión, o si el material del coaxial tiene características dieléctricas que afectan la velocidad de propagación, la frecuencia de resonancia podría cambiar.

Por lo tanto, la discrepancia entre la frecuencia calculada de 27 MHz y la frecuencia real de 22.3 MHz podría ser resultado de una combinación de los factores mencionados anteriormente. Para ajustar la antena a la frecuencia deseada, sería necesario modificar la longitud de los elementos o considerar ajustes en la construcción, como la inclusión de ajustes en la longitud de los elementos coaxiales o la modificación de su configuración.
