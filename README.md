# ProduccionSQL
Flujo de Trabajo scripts enviados a producción, Análisis Léxico y Sintactico 

## Semestre I
  Flujo de Trabajo: 
  
      . Basado en outlook
      . Ejecución en sesión personal de  Outlook
      . Respuesta correo destinatarios operaciones producción hasta paso a Centros Desarrollo
      
  Análisis:
  
      . codificación ANSI
      . léxico: NIF, CIF, CCCC, Datos de Caracter Personal
      . Sintactico: detecta la tabla donde ocurre el Identificador de Persona Física
      . Sin Emulación
      
## Semestre II

  Flujo de Trabajo:
    Licencia VS Code para capturar Formulario M365 y envío correo a Director de Centro Desarrollo para, aprobado, envío paquete a buzon producción

  Análisis

    Léxico:
    
      Ampliar Identificadores de Persona Física por paises: Argentina, Colombia...

    Sintactico:

        . Análisis dentro del script:
          . Casos de producto cartesiano por no estar las tablas referenciadas mutuamente
          . Casos de falta de índices
          . Contemplar casos recibidos de operaciones producción 

         . Análisis en BDA/BML/DML

           . Invocaciones conocidas al rutinas programadas fuera del script que responden 100 Mb de datos
           . Diseño emulador base de datos basada en Tablas Oracle Y Teradata

    Ejecución

        . Carga de datos de prueba para estadística de uso automatizado fuera de entorno producción o en desarrollo
        . Si la aplicación no tiene estadística de uso, resultados de emulación en entorno test dentro de producción
        . Automatización gitactions para emular el proceso en GOOGLE Data Studio
