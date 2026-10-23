# Evidencias de estabilización y lanzamiento — Semana 3

**Proyecto:** IT Incident Hub  
**Responsable:** Jorge Daniel Achij López  
**Alcance:** entrega documental de la Semana 3; el código fuente y la historia principal se mantienen en [Semana 1](https://github.com/JorgeDanielAchijLopez/it-incident-hub-semana-1).

## Fuentes verificables

- [Release v1.0.0](https://github.com/JorgeDanielAchijLopez/it-incident-hub-semana-1/releases/tag/v1.0.0): versión publicada en el repositorio principal.
- [Historial de Pull Requests](https://github.com/JorgeDanielAchijLopez/it-incident-hub-semana-1/pulls?q=is%3Apr+is%3Aclosed): cambios, revisiones y fusiones.
- [GitHub Actions](https://github.com/JorgeDanielAchijLopez/it-incident-hub-semana-1/actions): compilación, lint, integración PostgreSQL y controles de dependencias.
- [Registro de PR revisados](https://github.com/JorgeDanielAchijLopez/it-incident-hub-semana-1/blob/main/docs/ab29-evidencia-pull-requests.md): tabla de doce PR con referencias.
- [Registro del agente Windows y fallos de CI](https://github.com/JorgeDanielAchijLopez/it-incident-hub-semana-1/blob/main/docs/ci-azure-agente-windows.md): fallo real y posterior corrección.
- [Auditoría de dependencias y deuda técnica](https://github.com/JorgeDanielAchijLopez/it-incident-hub-semana-1/blob/main/docs/ab34-informe-auditoria.md).
- [Preparación del release AB#35](https://github.com/JorgeDanielAchijLopez/it-incident-hub-semana-1/blob/main/docs/ab35-preparacion-release.md): instrucciones y controles de validación.

## Evidencias de ejecución

El proyecto documenta una ejecución fallida de Azure Pipelines `#20261022.1` por disponibilidad transitoria de PostgreSQL, la corrección en commit `14bafed` y la ejecución exitosa `#20261022.2`. También registra la validación posterior de seguridad `#20261022.4`.

El lanzamiento v1.0.0 se realizó en el repositorio principal. La validación de preproducción mediante Azure Environment y aprobación manual **no equivale a despliegue de producción**.

## Alcance y pendientes

Esta carpeta documenta y enlaza evidencias existentes; **no duplica ni atribuye retrospectivamente a Semana 3** los commits realizados en semanas anteriores. Para la entrega académica final faltará adjuntar capturas seleccionadas de Azure Boards, aprobación de preproducción y resultados de los pipelines, junto con un resumen de los requisitos del enunciado.

El informe de seguridad reconoce como pendiente un escaneo integral de secretos de todo el historial Git. No se debe afirmar que ese control se completó sin evidencia adicional.
