# UTNOutdoors
Actividad formativa N°2 de AED
Alumno: Meza, Leandro David
Comisión: ISI B (k1.2)

# https://zponzio.github.io/UTNOutdoors/


1. Nombre y Descripción Innovadora

Nombre del proyecto: UTN Outdoors

UTN Outdoors es una tienda inteligente de artículos de camping y pesca pensada para entusiastas del aire libre que valoran tanto la libertad de elegir producto por producto como la comodidad de llevarse una solución ya armada. El concepto central es el de combo temático inteligente: en lugar de limitarse a vender carpas, cañas, reels o mochilas de forma aislada, la plataforma agrupa esos mismos productos del catálogo base en paquetes pensados para una actividad concreta — un fin de semana en la isla, una jornada de pesca de dorado, una travesía de trekking — a un precio promocional.

Desde el punto de vista de datos, lo interesante (y el eje de esta actividad) es que un producto individual y un combo no son dos entidades distintas, sino dos variantes de un mismo registro homogéneo: el combo simplemente activa un campo compuesto adicional que referencia a los productos que lo integran. Esto permite recorrer, ordenar y buscar todo el catálogo —individual y combinado— con una única estructura, demostrando en la práctica la diferencia entre campos de contenido simple y campos continente (compuestos).


2. Diseño del Registro Principal (Notación Formal UTN)

Se define una única estructura de registro homogénea, capaz de representar tanto un producto individual como un combo temático, evitando la duplicación de estructuras y favoreciendo la integridad del archivo de catálogo.

```
ACCION GestionCatalogoUTNOutdoors ES;
AMBIENTE
ITEMCATALOGO = Registro
    idProducto             : AN(7);
    nombreItem             : AN(40);
    tipoItem               : Caracter;
    categoria              : AN(25);
    descripcionBreve       : AN(150);
    precioUnitario         : Real;
    stockDisponible        : Entero;
    componentesCombo = Registro
        idComponente1      : AN(7);
        cantidad1          : Entero;
        idComponente2      : AN(7);
        cantidad2          : Entero;
        idComponente3      : AN(7);
        cantidad3          : Entero;
        idComponente4      : AN(7);
        cantidad4          : Entero;
    Fin Registro;
    precioComboPromocional : Real;
    porcentajeAhorro       : Real;
    imagenReferencia       : AN(120);
Fin Registro;
```

3. Enlaces a chats con Gemini y Claude

- https://gemini.google.com/share/9994453b06e5
- https://claude.ai/share/da084830-7a3c-4eb6-90e7-52e93c4b4417

4. Reflexión

    El trabajar con la IA como herramienta para el desarrollo de código, asistente para la planificación y despliegue, y la redacción de texto; es sin dudas una forma de trabajar inexorable en la actualidad. Negar su uso hubiese implicado en este caso, tener que dediccar semanas, y seguramente meses, al aprendizaje de diferentes lenguajes y comprensión del uso de la plataforma de GitHub.
   Sin embargo requiere una revisión constante y activa de cada uno de los detalles del contenido que dicha herramienta produce, de lo contrario existirían errores muy significativos en el producto final.
    Otro aspecto realmente importante a considerar es el costo de la inteligencia artificial. Esto se vio reflejado en mi decisión de utilizar dos modelos diferentes, dedicando uno a la planificación y otro para el desarrollo.
