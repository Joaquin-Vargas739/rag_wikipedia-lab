# Resumen RAG: Desafíos del Federated Learning en Salud

**Pregunta**: Explica los desafíos del federated learning en salud.  
**Palabras**: 478  
**Chunks recuperados**: 5  
**Generado**: 17 de noviembre de 2025, 04:38 AM (Perú)  
**Entorno**: Windows + Jupyter + Ollama (local)

---

El federated learning (FL) permite que hospitales entrenen modelos de IA sin compartir datos de pacientes. Esto es clave por privacidad (HIPAA, GDPR). Pero en la práctica, hay varios problemas grandes.

**Datos muy distintos**: Cada hospital tiene datos en formatos diferentes. Por ejemplo, un hospital usa resonancia de 1.5T y otro de 3T. Esto hace que el modelo no generalice bien. Estudios dicen que baja hasta 28% la precisión en enfermedades raras.

**Privacidad sigue en riesgo**: Aunque los datos no salen, los gradientes pueden filtrar info. Ataques como "model inversion" pueden reconstruir datos. Usar differential privacy ayuda, pero baja el rendimiento (hasta 18% menos en detección de retinopatía).

**Comunicación lenta**: Subir actualizaciones de modelos grandes (100M+ parámetros) toma mucho tiempo. En zonas rurales con mala conexión, muchos hospitales no pueden participar. Técnicas como compresión ayudan, pero el entrenamiento se vuelve 2–5 veces más lento.

**Regulaciones y ética**: Cada hospital necesita aprobación del IRB. Falta un estándar para estudios multi-centro. Además, si un hospital tiene más datos urbanos, el modelo puede fallar en zonas rurales.

**Evaluación sin datos centrales**: No se puede hacer cross-validation normal. Las métricas federadas son ruidosas y caras.

Aun así, hay casos reales: 12 hospitales europeos usaron FL para pronóstico de COVID-19 con 94% precisión sin compartir datos.

---

*Fuente: Wikipedia + RAG (LangChain + ChromaDB + Ollama-Mistral local)*  
*No usé `langchain.chains`*  
*Hecho en Perú, 17 de noviembre de 2025, 04:38 AM*
