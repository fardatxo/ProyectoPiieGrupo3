# 📄 Informe de Digitalización: SerraInnova

**Proyecto**: PIIE - Grupo 3
**Fecha**: 13 de Febrero de 2026

---

## 1. Contexto y Objetivos de Digitalización

El sector inmobiliario tradicional se ha basado históricamente en procesos manuales, documentación física y una falta de transparencia en cuanto al rendimiento energético de las viviendas. **SerraInnova** nace con el objetivo de **digitalizar la intermediación inmobiliaria sostenible**, transformando cómo se compran, venden y gestionan las propiedades eficientes.

### Objetivos Principales:

- **Desmaterialización**: Eliminar el uso de papel en la gestión de fichas de propiedades y comunicaciones iniciales.
- **Acceso a la Información**: Democratizar el acceso a datos técnicos de sostenibilidad (certificaciones energéticas, emisiones) que antes eran complejos de obtener.
- **Automatización de Consultoría**: Sustituir el asesoramiento manual inicial sobre ahorro energético por herramientas digitales interactivas (Calculadora CO2).

---

## 2. Qué se digitaliza con la Web

La plataforma web de SerraInnova actúa como el eje central de esta transformación digital, cubriendo cinco bloques fundamentales:

### a. Catálogo Sostenible

Digitalizamos el inventario de viviendas, pasando de simples "fichas de venta" a **activos digitales con metadatos de sostenibilidad**.

- **Antes**: Ficha en papel en escaparate con precio y fotos.
- **Ahora**: Base de datos consultable con filtros avanzados por **Certificación Energética (A-G)**, tipo de energía renovable (Solar, Aerotermia) y características constructivas (Aislamiento SATE).

### b. Calculadora de Impacto

Digitalizamos el proceso de **auditoría energética preliminar**.

- Esta herramienta permite al usuario introducir datos de su vivienda actual o deseada y obtener instantáneamente un cálculo de emisiones de CO2 y ahorro potencial.
- Transforma fórmulas complejas de ingeniería en una interfaz web amigable, ofreciendo valor inmediato al usuario.

### c. Backoffice (Panel de Administración)

Digitalizamos la **gestión interna de la inmobiliaria**.

- Permite a los administradores gestionar el ciclo de vida de las propiedades (Altas, Bajas, Modificaciones) y los contenidos del blog en tiempo real, sin depender de terceros ni procesos manuales.

### d. Área de Normativa (Blog Educativo)

Digitalizamos la **divulgación legal y técnica**.

- Centralizamos información sobre subvenciones (Fondos Next Generation), normativas de construcción y leyes de vivienda en un repositorio digital accesible y actualizado, facilitando el cumplimiento normativo a los usuarios.

### e. Servicios

Digitalizamos la **captación y atención al cliente**.

- El formulario de contacto y la presentación de servicios online sustituyen la necesidad de una primera visita presencial a la oficina, agilizando el embudo de ventas.

---

## 3. Convergencia IT y OT en el Proyecto

En el contexto de SerraInnova, es crucial diferenciar las tecnologías de la información (IT) de las tecnologías de operación (OT), y cómo convergen:

### 💻 Parte IT (Tecnologías de la Información)

Es el núcleo de nuestro proyecto actual. Comprende todo el software y hardware utilizado para procesar datos y gestionar información:

- **Infraestructura Web**: Servidor (Apache/Nginx), Base de Datos (MySQL).
- **Aplicación**: Framework Laravel (Backend) y Vue.js (Frontend).
- **Dispositivos de Usuario**: Ordenadores y móviles desde los que se accede a la web.

### ⚙️ Parte OT (Tecnologías de Operación)

Aunque la web no controla maquinaria industrial directamente, **conecta con el mundo OT** de las viviendas inteligentes (Smart Homes):

- **Datos de Sensores**: La plataforma está preparada para (en el futuro) digitalizar datos provenientes de contadores inteligentes, inversores solares y sistemas domóticos.
- **Certificación**: La "etiqueta energética" que mostramos es el resultado digital de mediciones físicas (aislamiento, rendimiento de calderas) realizadas en el entorno OT de la vivienda.

---

## 4. Tecnologías Habilitadoras Digitales (THD) Implicadas

Para hacer posible esta plataforma, aplicamos varias THD clave:

1.  **Cloud Computing (Computación en la Nube)**:
    - La plataforma está diseñada para desplegarse en la nube, permitiendo acceso ubicuo y escalabilidad sin necesidad de infraestructura física propia en la inmobiliaria.
2.  **Ciberseguridad**:
    - Implementamos protocolos para proteger la integridad de los datos de las propiedades y la privacidad de los usuarios.
3.  **Big Data y Analítica de Datos (Incipiente)**:
    - A través de la calculadora y las búsquedas, recolectamos datos sobre tendencias de demanda energética, lo que permite generar "insights" sobre qué tipo de eficiencia valoran más los usuarios.
4.  **Plataformas Digitales**:
    - SerraInnova actúa como una plataforma bilateral que conecta oferta (propiedades sostenibles) con demanda (compradores concienciados).

---

## 5. Datos: Recogida y Almacenamiento

La digitalización se basa en el dato. En SerraInnova gestionamos:

### 📂 Qué recogemos

- **Datos de Propiedades (Públicos)**: Especificaciones técnicas, fotos, ubicación, certificado energético.
- **Datos de Usuarios (Privados)**: Nombres, correos electrónicos y mensajes de contacto (Lead generation).
- **Datos de Comportamiento (Anónimos)**: Cálculos realizados en la calculadora de CO2 (para estadísticas).

### 💾 Dónde se guardan

- **Base de Datos Relacional (MySQL/SQLite)**: Estructurada en tablas (`properties`, `users`, `messages`).
- **Almacenamiento de Archivos (Storage)**: Imágenes y documentos PDF de certificaciones guardados en el sistema de archivos del servidor, vinculados por referencias en la BD.

---

## 6. Riesgos de Ciberseguridad y Medidas

Al digitalizar el negocio, nos exponemos a riesgos que mitigamos activamente:

| Riesgo                         | Descripción                                        | Medida de Mitigación (Digitalización Segura)                                        |
| :----------------------------- | :------------------------------------------------- | :---------------------------------------------------------------------------------- |
| **SQL Injection**              | Ataque a la base de datos a través de formularios. | Uso de **Eloquent ORM** de Laravel que sanitiza automáticamente las consultas.      |
| **XSS (Cross-Site Scripting)** | Inyección de scripts maliciosos en el navegador.   | Motor de plantillas de Vue.js y Laravel que escapan la salida de datos por defecto. |
| **Robo de Identidad**          | Acceso no autorizado al panel admin.               | Sistema de autenticación robusto y contraseñas hasheadas (Bcrypt).                  |
| **Intercepción de Datos**      | Escucha de comunicaciones.                         | Uso de protocolo **HTTPS** (TLS/SSL) obligatorio en producción.                     |

---

## 7. Impacto Social y Ambiental

La digitalización de SerraInnova trasciende lo técnico para generar impacto real:

### 🌍 Impacto Ambiental

- **Reducción de Huella de Carbono**: Al facilitar la compra de viviendas eficientes, contribuimos directamente a reducir el consumo energético del parque inmobiliario.
- **Concienciación**: La calculadora visualiza el impacto invisible del CO2, educando al usuario.

### 👥 Impacto Social

- **Transparencia de Mercado**: Eliminamos la asimetría de información. El comprador sabe exactamente qué eficiencia compra.
- **Accesibilidad**: Cualquier persona con conexión a internet puede aprender sobre ayudas públicas y normativas sostenibles sin coste alguno.
