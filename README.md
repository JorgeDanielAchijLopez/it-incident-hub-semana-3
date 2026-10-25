# IT Incident Hub — Semana 3

## Proyecto integrador DevOps

**Estudiante:** Jorge Daniel Achij López  
**Universidad:** Universidad Mariano Gálvez de Guatemala  
**Proyecto:** IT Incident Hub  
**Etapa:** Semana 3 — Estabilización y entrega final

## Descripción

IT Incident Hub es un sistema web para registrar, consultar y gestionar incidentes de soporte técnico.

Esta tercera entrega está destinada a documentar la estabilización del proyecto, la validación de pruebas, la preparación del lanzamiento y las evidencias finales del proceso DevOps.

## Tecnologías utilizadas

- React y TypeScript para el frontend.
- Node.js, Express y TypeScript para el backend.
- PostgreSQL para almacenar los incidentes.
- Docker para ejecutar servicios.
- GitHub Actions para integración continua.
- Azure DevOps para planificación, seguimiento y pipelines.

## Repositorios del proyecto

- [Semana 1 — Planificación y desarrollo](https://github.com/JorgeDanielAchijLopez/it-incident-hub-semana-1)
- [Semana 2 — Integración continua y seguridad](https://github.com/JorgeDanielAchijLopez/it-incident-hub-semana-2)
- [Semana 3 — Estabilización y entrega](https://github.com/JorgeDanielAchijLopez/it-incident-hub-semana-3)

## Versión del proyecto

La versión `v1.0.0` se encuentra publicada en el repositorio principal.

[Consultar release v1.0.0](https://github.com/JorgeDanielAchijLopez/it-incident-hub-semana-1/releases/tag/v1.0.0)

## Evidencias DevOps

El repositorio principal contiene los Pull Requests, revisiones, historial de commits, pruebas automatizadas y documentación de los pipelines.

La validación de Azure Pipelines incluye ejecuciones fallidas, correcciones verificables y ejecuciones exitosas mediante un agente Windows autohospedado.

## Estado de la entrega

La documentación de cierre de Semana 3 está organizada en `docs/` y enlaza las evidencias verificables de las tres entregas. La aplicación ejecutable se conserva en Semana 1; este repositorio funciona como entrega documental y guía de reproducción del tag `v1.0.0`.

**Última actualización verificada del repositorio principal:** PR [#21](https://github.com/JorgeDanielAchijLopez/it-incident-hub-semana-1/pull/21) fusionado a `main` (`f3f5bab`), con documentación final y corrección de dependencia `body-parser`. GitHub Actions [ejecución #30](https://github.com/JorgeDanielAchijLopez/it-incident-hub-semana-1/actions/runs/40239671615) finalizó correctamente. El tag `v1.0.0` permanece en el commit original `f55a55f`; los cambios posteriores no modifican retroactivamente esa versión.

### Documentación de cierre

- [Checklist del Epic AB#7](docs/checklist-cierre-epic-ab7.md)
- [Evidencias de lanzamiento](docs/evidencias-release.md)
- [Reproducir la versión publicada](docs/reproducir-v1.0.0.md)
- [Trazabilidad de entregas](docs/trazabilidad-entregas.md)
- [Verificación de repositorios](docs/verificacion-tres-repositorios.md)
- [Escaneo de secretos](docs/ab34-escaneo-gitleaks.md)

**Alcance:** se documentó una aprobación de preproducción; no se declara despliegue real a producción. El informe académico en PDF y su selección de capturas se preparan por separado.
