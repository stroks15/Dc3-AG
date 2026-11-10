# Generador de constancias DC-3

Aplicación web estática para capturar trabajadores, seleccionar un curso de capacitación, revisar constancias y descargar un PDF individual por trabajador.

## Uso

1. Abre `index.html` en un navegador moderno.
2. Selecciona las fechas y el curso impartido.
3. Pega un trabajador por renglón con el formato `NOMBRE COMPLETO, CURP, PUESTO`.
4. Genera la vista previa y verifica cuidadosamente los datos.
5. Descarga los PDF individuales o usa la opción de impresión.

El puesto es opcional y, si se omite, se asigna `TÉCNICO`. Las líneas con CURP distinta de 18 caracteres alfanuméricos se omiten y se reportan para corrección.

## Datos de la empresa

Los datos de empresa, registro patronal, RFC, ocupación y agente capacitador están definidos en el objeto `EMPRESA` dentro de `index.html`. Actualízalos antes de emitir constancias si corresponde.

## Privacidad y requisitos

- El procesamiento de trabajadores ocurre localmente en el navegador; no hay backend ni almacenamiento remoto.
- La biblioteca `html2pdf.js` se carga desde cdnjs, por lo que se requiere conexión a internet para generar PDF.
- Revisa nombres, CURP, fechas, curso, horas, firmas y requisitos aplicables antes de utilizar o entregar cualquier constancia. Esta herramienta no valida ni certifica por sí misma el cumplimiento ante la STPS.
