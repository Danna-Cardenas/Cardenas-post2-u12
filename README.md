# Integracion de Patrones y Arquitecturas — U12 Post 2

## Objetivo
Validar la arquitectura con ArchUnit, documentar decisiones en ADRs y ejecutar
reglas en GitHub Actions.

## Arquitectura
- Dominio: entidades y puertos.
- Aplicacion: orquestacion de procesamiento.
- Adaptadores: REST, facade y procesadores.
- Infraestructura: persistencia y notificaciones.

## Metricas SonarQube
| Metrica | Antes | Despues |
|---------|-------|---------|
| Cyclomatic Complexity (servicio principal) | X | X |
| Cognitive Complexity | X | X |
| Coverage | X% | X% |
| Quality Gate | Failed/Passed | Passed |

## Validacion Arquitectonica
- Regla 1: el dominio no depende de infraestructura ni adaptadores.
- Regla 2: los controladores solo acceden a la facade.
- Regla 3: los puertos de dominio son interfaces.
- Regla 4: los procesadores implementan `ProcesadorPedido`.
- Regla 5: la infraestructura no accede a adaptadores REST.

## ADRs
- docs/adr/ADR-001.md
- docs/adr/ADR-002.md
- docs/adr/ADR-003.md

## Pipeline
El workflow de validacion esta en `.github/workflows/arquitectura.yml`.

## Evidencias
![Dashboard antes](img/sonar-dashboard-antes.png)
![Dashboard despues](img/sonar-dashboard-despues.png)

## Notas
- Coloca las capturas en `img/` con los nombres indicados.
