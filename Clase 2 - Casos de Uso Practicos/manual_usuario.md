# Guía de Usuario: Sistema de Inventario del Hotel
![Badge: Guía de Usuario](https://img.shields.io/badge/Guía-Usuario-blue) ![Badge: Hotel de Lujo](https://img.shields.io/badge/Hotel-De%20Lujo-gold)

## 👋 Introducción

Bienvenido/a al **Sistema de Inventario del Hotel de Lujo**. Esta herramienta te ayudará a consultar y verificar el inventario de todos los productos y materiales disponibles en nuestro hotel, desde artículos de limpieza hasta amenidades de lujo para las habitaciones.

Este manual te explicará de manera sencilla cómo utilizar el sistema, qué información puedes obtener y cómo interpretar los resultados, todo sin necesidad de conocimientos técnicos avanzados.

## ✨ Beneficios del Sistema

Con esta herramienta podrás:
- Ver el inventario actual de cualquier producto del hotel
- Saber dónde se encuentra cada artículo (en qué almacén)
- Conocer el valor de los artículos en inventario
- Generar informes para la gestión del hotel y relojería

## 🚶‍♀️ Pasos para Consultar el Inventario

### 1. Acceso al Sistema

1. Abre el programa SAP en tu ordenador
2. Introduce tu usuario y contraseña
3. En el campo de transacción, escribe: **ZHOTEL_INVENTORY_MGT**
4. Pulsa Enter o haz clic en el botón verde ✓

![Pantalla de Acceso](https://ejemplo-imagen.com/acceso-sap.jpg)
*Ejemplo de pantalla de acceso a SAP*

### 2. Configuración de la Consulta

Una vez que el programa se abra, verás una pantalla con opciones para filtrar el inventario:

![Pantalla de Selección](https://ejemplo-imagen.com/pantalla-seleccion.jpg)
*Pantalla de selección de parámetros*

Rellena los campos según lo que necesites consultar:

| Campo | Qué significa | Cómo usarlo |
|-------|--------------|------------|
| Material | Código o rango de productos | Introduce el código del producto o deja en blanco para ver todos |
| Centro | Ubicación principal (Hotel o Relojería) | Selecciona "HOTEL" o "RELOJ" según corresponda |
| Almacén | Almacén específico | Selecciona el almacén o deja en blanco para todos |
| Fecha | Fecha de referencia | Normalmente se usa la fecha actual (ya viene seleccionada) |

> **Consejo:** Si no estás seguro de los códigos, puedes hacer clic en el botón de ayuda (icono de lupa 🔍) junto a cada campo para buscar valores.

### 3. Ejecutar la Consulta

Una vez configurados los filtros:

1. Haz clic en el botón **Ejecutar** (icono de avión de papel ✈️) en la barra superior
2. O pulsa la tecla F8 en tu teclado

### 4. Revisar los Resultados

Después de unos segundos, verás una tabla con todos los productos que cumplen tus criterios:

![Resultados de Inventario](https://ejemplo-imagen.com/resultados.jpg)
*Ejemplo de resultados de consulta de inventario*

La tabla muestra:
- **Material**: Código del producto
- **Descripción**: Nombre del producto
- **Centro**: Ubicación principal (Hotel/Relojería)
- **Almacén**: Ubicación específica
- **Stock**: Cantidad disponible
- **Precio**: Valor por unidad
- **Moneda**: Tipo de moneda

## 🎯 Qué Hacer con los Resultados

### Verificar Disponibilidad
Utiliza esta información para confirmar si hay suficiente stock de un producto antes de solicitarlo para un evento o servicio.

### Reportar Discrepancias
Si encuentras diferencias entre el inventario mostrado y el inventario físico:
1. Anota el código del material y la cantidad
2. Comunícate con el departamento de inventarios
3. Proporciona la información para que se realice un ajuste

### Exportar Resultados
Para guardar o compartir la información:

1. Haz clic en el botón **Exportar a Excel** (icono de hoja de cálculo) en la barra de herramientas
2. Selecciona la ubicación donde quieres guardar el archivo
3. Dale un nombre descriptivo (ejemplo: "Inventario_Amenidades_Oct2025")
4. Haz clic en Guardar

### Imprimir el Informe
Para obtener una copia física:

1. Haz clic en el botón **Imprimir** (icono de impresora)
2. Selecciona la impresora
3. Ajusta las opciones si es necesario
4. Haz clic en Imprimir

## ❓ Preguntas Frecuentes

### ¿Por qué no veo ningún resultado al ejecutar el informe?
Esto puede ocurrir por varias razones:
- **Los filtros son muy restrictivos**: Intenta ampliar los rangos de búsqueda o dejar algunos campos en blanco
- **No hay stock**: Es posible que no haya inventario que cumpla con tus criterios
- **Error de acceso**: Verifica que tienes permisos para ver el inventario solicitado

### ¿Cada cuánto se actualiza el inventario en el sistema?
El inventario se actualiza en tiempo real. Cada vez que se registra una entrada o salida de productos, el sistema refleja el cambio inmediatamente.

### ¿Qué significa cuando un producto aparece con stock "0"?
Significa que el producto está registrado en el sistema pero actualmente no hay unidades disponibles en el almacén seleccionado. Deberás solicitar una reposición.

### ¿Cómo puedo ver solo los productos por debajo del stock mínimo?
Actualmente esta funcionalidad está en desarrollo. Por ahora, puedes exportar los resultados a Excel y filtrar manualmente los que tengan cantidades bajas.

### ¿Puedo modificar el inventario desde este programa?
No, este programa es solo de consulta. Para modificar el inventario debes usar el programa de gestión de movimientos de mercancía (transacción MB1A).

## 🔧 Solución de Problemas Comunes

### El sistema muestra un mensaje de error
Si aparece un mensaje de error al ejecutar la consulta:
1. Toma nota del mensaje exacto
2. Cierra la ventana del error
3. Verifica que los rangos de fechas y valores sean correctos
4. Intenta ejecutar de nuevo con filtros más simples

### La información no coincide con la realidad
Si sospechas que hay discrepancias entre el sistema y el inventario físico:
1. Realiza un conteo manual del producto específico
2. Documenta la diferencia exacta
3. Contacta al equipo de inventarios para solicitar un ajuste

### El sistema funciona muy lento
Si el sistema tarda mucho en mostrar resultados:
1. Reduce el rango de datos solicitados (sé más específico en los filtros)
2. Evita ejecutar la consulta durante horas pico (inicio de turnos)
3. Cierra programas innecesarios en tu computadora

## 📞 Contacto y Soporte

Si necesitas ayuda adicional con el sistema de inventario:

### Soporte Nivel 1 (Problemas de Acceso/Técnicos)
- **Departamento IT**
- Extensión: 2150
- Email: soporte.it@hotellujo.com
- Horario: Lunes a Domingo, 7:00 - 23:00

### Soporte Nivel 2 (Consultas de Inventario)
- **Departamento de Almacén**
- Extensión: 3201
- Email: almacen@hotellujo.com
- Horario: Lunes a Viernes, 8:00 - 18:00

### Emergencias (Fuera de Horario)
- **Supervisor de Turno**
- Extensión: 1000
- Móvil: +34 600 123 456

---

## 📝 Registro de Capacitación

| Nombre del Empleado | Departamento | Fecha de Capacitación | Firma |
|---------------------|--------------|------------------------|-------|
| __________________ | ____________ | ____ / ____ / ________ | _____ |

---

*Manual preparado por el Departamento IT - Hotel de Lujo & Relojería Barcelona*  
*Actualizado: 22 de octubre de 2025*