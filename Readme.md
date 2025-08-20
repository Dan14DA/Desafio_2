# Proyecto TelecomX - Predicción de Clientes que se van

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/flacoca1970/Desafio_2/blob/main/TelecomX_LATAM_colab.ipynb)

Este proyecto te ayuda a **identificar qué clientes están a punto de irse** de la empresa y **qué hacer para retenerlos**.  
Todo funciona en Google Colab, sin necesidad de instalar nada.

---

## ¿Qué problema resolvemos?

Cuando los clientes se van (esto se llama "churn"), la empresa pierde dinero. Es más barato **retener un cliente** que conseguir uno nuevo. 

Este sistema:
1. **Analiza** los datos de clientes
2. **Predice** quién tiene más riesgo de irse  
3. **Sugiere** qué hacer para retenerlos
4. **Calcula** cuánto dinero puedes ahorrar

---

## Principales hallazgos de nuestro análisis

De 7,267 clientes analizados, **26.5% se fueron** en el período estudiado.

### Los clientes que más se van tienen estas características:

**Tipo de contrato:**
- Mes a mes: **42.7%** se van
- 1 año: **11.3%** se van  
- 2 años: **2.8%** se van

**Forma de pago:**
- Cheque electrónico: **45.3%** se van
- Cheque por correo: **19.1%** se van
- Transferencia automática: **16.7%** se van
- Tarjeta de crédito automática: **15.2%** se van

**Tipo de internet:**
- Fibra óptica: **41.9%** se van
- DSL: **19.0%** se van
- Sin internet: **7.4%** se van

---

## Cómo usar este sistema

### Paso 1: Abrir el proyecto
1. Haz clic en el botón "Open in Colab" de arriba
2. Sube tu archivo de datos o conecta tu base de datos
3. Ejecuta todas las celdas del cuaderno

### Paso 2: Configurar los costos
Antes de ejecutar, define:
- **Valor de retener un cliente**: $100 (puedes cambiarlo)
- **Costo de contactar un cliente**: $5 (puedes cambiarlo)

### Paso 3: Obtener resultados
El sistema te dará:
- Una **lista de clientes en riesgo** ordenada por probabilidad
- **Recomendaciones específicas** para cada grupo
- **Cálculo de ganancia** esperada

---

## Qué hacer con los resultados

### Clientes con MÁS riesgo (actuar YA):

**1. Clientes mes a mes + pago con cheque electrónico**
- **Acción**: Ofrecer descuento por cambiar a plan anual + pago automático
- **Mensaje**: "Te regalamos 1 mes y simplificas tus pagos"

**2. Clientes nuevos (menos de 3 meses)**
- **Acción**: Llamada de bienvenida y verificación del servicio
- **Mensaje**: "¿Todo funcionando bien? Te ayudamos a sacarle el máximo provecho"

**3. Clientes con fibra óptica y problemas**
- **Acción**: Revisión técnica proactiva del servicio
- **Mensaje**: "Queremos asegurar que tengas la mejor experiencia con fibra"

### Clientes con riesgo MEDIO:
- Enviar promociones especiales por email/WhatsApp
- Ofrecer mejoras de servicio

### Clientes con riesgo BAJO:
- Mantener comunicación regular con ofertas atractivas
- Programas de fidelidad

---

## Plan de acción sugerido

### Primeros 30 días:
- Contactar los 500-1000 clientes con mayor riesgo
- Probar 2-3 tipos de ofertas diferentes
- Medir qué funciona mejor

### Siguientes 30 días:
- Expandir las ofertas que funcionaron
- Ajustar el sistema según los resultados
- Implementar contacto automático

### Después de 90 días:
- Sistema funcionando automáticamente cada semana
- Reportes regulares de resultados
- Mejoras continuas

---

## Archivos que genera el sistema

Cuando ejecutes el proyecto, obtendrás:
- `clientes_en_riesgo_topN.csv` - Lista de clientes para contactar
- `README_REPORT.md` - Reporte detallado de resultados  
- `metrics.json` - Números y estadísticas del análisis

---

## Resultados esperados

Con los parámetros actuales (retener cliente = $100, contactar = $5):
- **Ganancia estimada**: $31,635
- **Clientes a contactar**: ~1,100 
- **Clientes que lograrás retener**: ~370

**Esto significa**: por cada $5 que gastes contactando, recuperas aproximadamente $29 en valor de cliente retenido.

---

## Preguntas frecuentes

**¿Qué tan confiable es la predicción?**
El sistema acierta en ~85% de los casos. No es perfecto, pero es mucho mejor que no hacer nada.

**¿Puedo cambiar los costos y valores?**
Sí, solo cambia los números en la sección "Parámetros" y el sistema recalculará todo.

**¿Con qué frecuencia debo ejecutar esto?**
Recomendamos cada semana o cada 15 días para mantener la lista actualizada.

**¿Qué pasa si no tengo todos los datos?**
El sistema puede trabajar con datos incompletos, pero será más efectivo con más información.

---

## Contacto y soporte

Para dudas sobre este proyecto:
- Equipo de Análisis de Datos
- Proyecto de Retención de Clientes TelecomX

**Versión**: Simplificada para Google Colab