# Auditoría ASG y Refactorización Sostenible

## **1\. INTRODUCCIÓN**

La empresa que he seleccionado es **Aceituneros de Salteras SL**, perteneciente al sector agrícola, ganadería, silvicultura y pesca. Es una microempresa de máximo 10 empleados y con una facturación mayor a 2.500€.

El enlace a la web es el siguiente: https://www.expansion.com/directorio-empresas/aceituneros-de-salteras-sl_1195321_A01_41.html

## **2\. FASES DE LA AUDITORÍA** 

### **FASE 1: Inventario y Dimensión Ambiental (A)**
Por una parte, la huella de carbono estimada por visita de esta página web es del 54%, eso significa que cada vez que un usuario visita esta página se emite una cantidad de carbono superior a la media global. Esto refleja una oportunidad de mejora en cuanto a optimización de recursos y sostenibilidad digital.

He conseguido este dato gracias a la herramienta gratuita ***Website Carbon Calculator**.*

<img width="1215" height="668" alt="image" src="https://github.com/user-attachments/assets/7fa01a92-b79a-4757-a149-c72bff48d08b" />


Por otra parte, inspeccionando la pestaña ***Network*** de las herramientas de desarrollador del navegador, los 3 recursos más pesados que se descargan al abrir la página son:

1. **pbex.js (149 kB)**: librería JavaScript externa  
2. **vendor.js (135 kB)** : librería JavaScript de dependencias  
3. **icon-s137c41c0f9.png (128 kB)**: imagen de iconos sin optimizar

Estos tres recursos son scripts de **JavaScript** y una imagen en formato **PNG** que se carga de forma pesada sin necesidad de ello, contribuyendo al alto consumo de la página.

En esta imagen podemos ver los recursos más pesados de la página web, aunque hay muchos más.

<img width="448" height="710" alt="image" src="https://github.com/user-attachments/assets/397855a0-7719-494e-9cae-9dacaea234fe" />


Una vez analizado el peso y el consumo de la página web, podemos llegar a la conclusión de que está web consume mucho más de lo que debería, llegando a sufrir una “**inflación de software**”. Como hemos podido ver en la imagen anterior, la página web genera **405 solicitudes** y **carga 16,6 MB** de recursos en total, una cifra muy por encima de lo recomendable.   
Por todo esto, podemos tomar consciencia de que la **sostenibilidad digital** es un aspecto fundamental que se debería de tomar en cuenta siempre.


### **FASE 2: Dimensión Social y Equidad (S)**
Para ver la accesibilidad de la página web, hacemos uso de ***WAVE Web Accessibility Evaluation Tool***. Al ver los resultados, podemos ver que dicha página obtiene una puntuación de 4,6 sobre 10, lo que indica un nivel de accesibilidad deficiente.

Los datos que se reflejan en la imagen son preocupantes, ya que la página presenta 9 errores de accesibilidad, 22 errores de constante y 37 alertas. Esto da a entender que no cumple con los estándares mínimos de accesibilidad web.
<img width="376" height="479" alt="image" src="https://github.com/user-attachments/assets/f58881b9-f039-4ce0-836d-ed841e92ef73" />


Los dos problemas más graves en contratos son los **9 errores de accesibilidad** y los **22 errores de contraste**.s

- Los **problemas de accesibilidad** son probablemente por imágenes sin atributo ***alt*** o formularios sin etiquetas lo que impide que los lectores transmitan correctamente el contenido a personas con discapacidad visual.  
- Los **problemas de contraste**, que son más del doble, es causado por numerosos elementos de texto no tienen suficiente contraste con el fondo, lo que dificulta o impide de su lectura a personas con baja visión o con algún problema de visión-.


### **FASE 3: Dimensión de Gobernanza y Ética (G)**
Si hablamos de la transparencia de la web, esta página no obliga al usuario a aceptar cookies no esenciales ni recurre a patrones oscuros para acondicionarlo.

En cuanto a los datos innecesarios, el registro únicamente requiere el correcto electrónica y su contraseña, con opción de acceso a Google en este caso, pero sin solicitar datos personales adicionales como el numero de telefono o la direccion.


### **FASE 4: Propuesta de Refactorización (Green Coding)**
Una vez visto el código de la web, he visto varias cosas que puedo corregir para que sea más sostenible el código y la página web para el usuario. 

En la parte de la **optimización de activos**, convertiría las imágenes actuales (.jpg) al formato **.WebP**, ya que este reduce el tamaño un 70% sin pérdida de calidad. Además, implementaría **Lazy Loading** para que solo carguen al entrar en el campo de visión del usuario, eliminando transferencias de datos completamente innecesarias.

En la parte de la **reducción de peticiones**, el problema que existe es que los scripts consumen mucho, entonces debería optimizar su carga. Para ello, pienso que se deberían cargar cada script de manera diferida para que no bloqueen la carga inicial de la página, y así reducir el número de publicidades activas de forma simultánea. Con esto reducimos significativamente el impacto ambiental y consumiría menos recursos, ya que, por ejemplo, el script que más pesa es pbex.js con **149 kB** de un sistema de pujas publicitarias.

Por último, según la **Paradoja de Jevons**, si la web carga más rápido, atraerá más visitas, pudiendo aumentar el consumo energético total y anular el ahorro logrado. Para evitar eso, combina la optimización técnica con el alojamiento en servidores de energía renovable, de modo que el crecimiento del tráfico no implique mayor impacto ambiental.  

## **3\. PROPUESTA DE REFACTORIZACIÓN**
Tras analizar el código fuente de la empresa, voy a proponer varias mejoras en las diferentes dimensiones explicadas anteriormente. Estas mejoras técnicas permiten reducir su impacto ambiental, mejorar su accesibilidad y reforzar la transparencia hacia el usuario.

### 3.1. Mejoras ambientales (A)
Analizando el peso y las peticiones de la página, voy a proponer varias optimizaciones para reducir su huella de carbono digital.

* **Optimización de imágenes**: convertir las imágenes a formato WebP, ya que así se reduce el peso hasta un 70%, sin pérdida de calidad y disminuyendo la energía consumida en cada transferencia.   
* **Peticiones HTTP**: limitar el número de redes publicitarias activas a la vez, ya que actualmente se gestionan más de 10, generando cientos de peticiones innecesarias.  
* **Lazy loading**: implementar carga diferida en imágenes para que solo se descarguen cuando el usuario las necesita.  
* **Eliminación de código no utilizado**: cargar primero el contenido principal y luego los scripts de seguimiento (Charbeat, Permutive, Omniture), de modo que el usuario vea el contenido más rápido y consuma menos energía.

### 3.2. Mejoras sociales (S)
Basándome en los resultados WAVE realizados anteriormente y en las pautas WCAG 2.2 \[1\], la página web presenta barreras de accesibilidad, por lo que a nivel social se podrían mejorar muchas cosas.

* **Uso de HTML semántico**: el código utiliza etiquetas genéricas como es \<div\> en  vez de usar etiquetas modernas y concretas como son \<header\>, \<nav\>, \<main\>, \<section\> y \<footer\>. Esto dificulta la navegación y no le dice al usuario lo que hay dentro de cada sección.  
* **Atributos alt**: varias imágenes carecen del atributo alt, incumpliendo el principio de perceptibilidad de las WCAG 2.2. Este atributo lo que hace es describir el contenido de la imagen.  
* **Mejora del contraste**: corregir los 22 errores de contraste que tiene la web detectados por WAVE para cumplir el nivel AA de las WCAG 2.2.  
* **Navegación accesible**: añadir una etiqueta descriptiva en el código para indicar que es cada elemento. Por ejemplo, que el menú principal se identifique como “menú principal” y no como una simple sección sin nombre.

### 3.3. Mejoras de gobernanza (G)
* **Consentimiento de cookies transparente**: rediseñar el banner de cookies para que las opciones de aceptar y rechazar tengan el mismo peso visual, eliminado el patrón oscuro actual.  
* **Simplificación de textos legales**: los textos del pie de página son extensos y técnicos, por lo que vendría bien simplificarlos para que así sea más comprensible para cualquier usuario.  
* **Eliminación de prácticas engañosas**: retirar el uso de colores y tamaños que dirigen al usuario inconscientemente hacia la aceptación de las cookies.  
* **Mejora de la privacidad**: reducir el número de servicios de rastreo activos al mínimo necesario, ya que actualmente hay varios como Amazon Ads, Permutive o ChartBeat.


## **4\. REFERENCIAS**
[1] W3C Web Accessibility Initiative (WAI), "Sumario de WCAG 2," *W3C*, 2025\. \[En línea\]. Disponible en: (https://www.w3.org/WAI/standards-guidelines/wcag/es)  
  
[2] S. Luján Mora, "Pautas de accesibilidad al contenido web 2.2," *Universidad de Alicante*, 2026\. \[En línea\]. Disponible en: (https://accesibilidadweb.dlsi.ua.es/?menu=pautas-2.2)
