MANUAL DE USUARIO
Probador de ICL7107 
Escuela de Ingeniería Eléctrica — Universidad de los Andes

1. Descripción General y Vista de la Tarjeta
El Probador de ICL7107 EVM es un módulo de prueba y evaluación desarrollado en la Escuela de Ingeniería Eléctrica de la Universidad de los Andes. Permite la verificación rápida, precisa y segura del correcto funcionamiento del circuito integrado ICL7107 (conversor analógico-digital de 3½ dígitos con salida directa para Displays de 7 segmentos LED).
 
Figura 1: Vista isométrica 3D del Probador de ICL7107 EVM.
2. Especificaciones Técnicas y Controles
• Alimentación:  Alimentación de +5 VDC mediante puerto microUSB integrado (PowerSupply +5VDC microUSB).
• Zócalo de Prueba:  Zócalo DIP-40 para fácil inserción y extracción del circuito integrado.
• Botón de Prueba:  Pulsador SW1 (TEST) para la verificación instantánea de todos los segmentos de la pantalla y la lógica interna.
• Ajuste de Referencia:  Potenciómetro multivuelta RV1 para calibrar el voltaje entre los puntos de prueba TP1 (REF_HI) y TP2 (REF_LO).
• Rango de Medición:  Soporta tensiones de prueba entre -100 mV y +100 mV en los bornes de entrada analógica (J1).
3. Procedimiento de Calibración de la Tensión de Referencia
Para garantizar una medición exacta en el rango de ±100 mV, es fundamental calibrar el voltaje de referencia de la tarjeta antes de realizar pruebas de medición:
1. Conecte la alimentación de +5V a la tarjeta (sin necesidad de insertar aún el chip o manteniendo el cuidado adecuado).
2. Coloque las puntas de un multímetro digital en los puntos de prueba TP1 (REF_HI) y TP2 (REF_LO), ubicados en la esquina inferior derecha cerca de los bornes de entrada.
3. Ajuste el potenciómetro azul RV1 hasta que la diferencia de potencial entre TP1 y TP2 sea exactamente de 100 mV; ( También se puede calibrar a un valor menor a los 100mV, recordando que la entrada no podrá superar este valor ) .
4. Una vez calibrado a 100 mV de referencia, el circuito integrado podrá medir voltajes de entrada precisos dentro del rango de -100 mV a +100 mV.
4. Instrucciones de Uso Paso a Paso
⚠️ REGLA DE SEGURIDAD OBLIGATORIA
IMPORTANTE: Para prevenir daños permanentes en los pines del circuito integrado o en la tarjeta por picos de tensión o cortocircuitos, la tarjeta DEBE ESTAR COMPLETAMENTE DESENERGIZADA (desconectada de la fuente de alimentación USB) al insertar o retirar el ICL7107 del zócalo.

Paso 1: Inserción del Integrado (Tarjeta Desenergizada). Asegúrese de que el cable microUSB esté desconectado. Inserte cuidadosamente el integrado ICL7107 en el zócalo de 40 pines, verificando la muesca de orientación (pin 1 hacia la izquierda).
Paso 2: Energización de la Tarjeta. Conecte la alimentación de +5VDC al puerto microUSB para energizar el probador.
Paso 3: Prueba de Display y Lógica (-1888). Presione el botón SW1 (TEST). El display LED debe indicar de forma inmediata el valor -1888. Esto confirma el funcionamiento de la lógica interna, el decodificador y la totalidad de los segmentos LED de la pantalla.
Paso 4: Verificación en Vacío (Ruido Ambiental). Con las entradas analógicas sin conectar (entradas flotantes), es normal observar lecturas fluctuantes (por ejemplo, entre 300 mV y -300 mV). Al no tener una impedancia de entrada conectada, el integrado detecta el ruido electromagnético ambiental, lo cual es indicativo del correcto funcionamiento de la etapa analógica de alta impedancia.
Paso 5: Prueba de Medición con Voltaje de Entrada. Aplique el voltaje a medir en los bornes verdes J1. Con la referencia calibrada a 100 mV (TP1 a TP2), introduzca un voltaje dentro del rango de -100 mV a +100 mV y verifique la coincidencia exacta de la lectura en el display.
5. Resumen de Diagnóstico
Prueba / Condición	Lectura Esperada	Diagnóstico / Significado
Pulsar Botón TEST (SW1)	-1888	Displays, driver de segmentos y lógica interna OK.
Sin entrada (Flotante)	Fluctuación (±300 mV)	Comportamiento normal. Etapa analógica detecta ruido ambiental.
Voltaje de Entrada en J1	Valor real (-100 mV a +100 mV)	Conversión A/D correcta con referencia de 100 mV (TP1-TP2).

 
Figura 2: Pulsando el Botón de Test
 
Figura 3: Sin entrada (Ruido Ambiental)
