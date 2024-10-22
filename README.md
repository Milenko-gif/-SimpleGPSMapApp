CODIGO_PRUEVA (1.0)
# Descripción
Este proyecto es una aplicación Android que implementa medidas de seguridad para proteger 
contra vulnerabilidades comunes. 
# Vulnerabilidades Identificadas
1. App Security Score: 31/100, clasificado como alto riesgo (grado C)​.
2. Problemas en el certificado: La aplicación está firmada con un certificado de depuración, lo cual es un riesgo para un entorno de producción​.
3. Uso de algoritmos débiles: El certificado utiliza SHA1, conocido por problemas de colisión​.
4. Configuración de depuración activa: El APK permite la depuración (android:debuggable=true), lo que facilita el trabajo de los atacantes para obtener información sensible​.
5. Compatibilidad con versiones vulnerables de Android: La aplicación puede instalarse en dispositivos Android con versiones vulnerables, ya que la minSdk es 24 (Android 7.0)​.
# Mejoras Implementadas
1. Eliminar el certificado de depuración: Firmar la aplicación con un certificado de producción seguro.
2. Actualizar el algoritmo de firma: Cambiar a un algoritmo más seguro como SHA-256 o superior.
3. Deshabilitar la depuración: Remover la opción android:debuggable=true en versiones finales.
4. Compatibilidad: Establecer la compatibilidad mínima con versiones más recientes de Android (API 29 o superior).
# Tests de vulnerabilidad
1. Exportación de componentes sin la debida protección: Un receptor de difusión (BroadcastReceiver) está accesible para otras aplicaciones, lo que podría permitir un acceso no autorizado​.
2. Permiso no definido: El receptor está protegido por un permiso que no está claramente especificado, lo que puede representar un riesgo​.
# Documentación
- Análisis de vulnerabilidades
- Implementación de Best Practices
- Security Tips
- Programa de Mejora de Seguridad
# Cómo Ejecutar la Aplicación de Forma Segura
1. Clonar el repositorio 
2. Importar el proyecto en Android Studio 
3. Ejecutar la aplicación en un dispositivo o emulador 
4. Asegurarse de que los permisos necesarios están configurados 
# Reporte de Vulnerabilidades El reporte detallado de las pruebas de vulnerabilidad 
realizadas se encuentra en el archivo `vulnerability_report.pdf`.
