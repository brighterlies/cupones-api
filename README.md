# GRUPO 9 Ejercicio Guiado: Pruebas de Regresión Automatizadas en una API de Cupones

## 1. ¿Por qué fue difícil detectar la regresión sin pruebas?

El error no fue evidente de inmediato porque el sistema siguió funcionando, aunque dejó de aplicar correctamente el cupón `“BIENVENIDA”`. Al no haber pruebas automatizadas, resultó casi imposible detectar el fallo al revisar manualmente el código.

## 2. ¿Cómo te ayuda el testing automatizado a mantener calidad?

Las pruebas permiten detectar errores rápidamente y aseguran que el código siga funcionando tras cambios. Integradas en CI, como `GitHub Actions`, validan de forma automática y continua.

## 3. ¿Qué otras partes del código deberías cubrir con pruebas?

La prueba de integración del endpoint `/precio` cubre cupones inválidos, omisión del campo impuesto, tipos de datos incorrectos, uso sin cupón y validación de respuestas HTTP ante entradas inválidas.

## 4. ¿Cómo evitarías errores similares en el futuro?

Mejorar la calidad del código mediante pruebas de regresión actualizadas, TDD, validaciones automáticas en `pull requests` y refactorización con apoyo de cobertura y CI.

----------------

## Capturas de pantalla
- Las capturas de pantalla del test fallando (regresión) y del test funcionando 
(corregido) se encuentran en la carpeta `screenshots`.
- La captura del workflow corriendo en `GitHub Actions` también se encuentra en `screenshots`.

## Resumen:
- Aplicamos pruebas unitarias a la lógica de cupones y detectamos un error al eliminar el cupón `"BIENVENIDA"`. Lo restauramos y validamos nuevamente. Automatizamos el proceso con `GitHub Actions` para prevenir futuras regresiones y mantener la calidad del sistema.