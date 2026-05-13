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
