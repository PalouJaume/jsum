# JSUM: JSON Summary Tool

Herramienta CLI que analiza archivos JSON y genera un resumen/reporte.

## Funcionalidades

- [ ] Subcomando `stats` que cuenta key totales y profundidad máxima.
- [ ] Leer archivo pasado como argumento.
- [ ] Errores con contexto usando con `thiserror`.
- [ ] Un par de tests básicos.

## Uso

```bash
# Analiza un archivo y muestra estadísticas
jsum stats data.json

# Output:
# Keys totales: 47
# Profundidad máxima: 4
# Tipos encontrados: object (12), array (5), string (23), number (7)
# Arrays vacíos: 2
# Tamaño en memoria estimado: 2.3 KB

# Lista todas las keys únicas (paths)
jsum keys data.json

# Output:
# .name
# .users[]
# .users[].id
# .users[].email
# .config.timeout

# Extrae un valor por path
jsum get data.json ".users[0].name"

# Output
# <Name>
```

