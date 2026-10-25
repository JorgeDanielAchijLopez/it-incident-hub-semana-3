# Lista de verificación de cierre — Epic AB#7

**Proyecto:** IT Incident Hub  
**Responsable:** Jorge Daniel Achij López  
**Epic:** [AB#7 — Automatización DevOps, Calidad y Entrega Continua](https://dev.azure.com/devopsOrganizativaUMG01/IT-Incident-Hub/_workitems/edit/7)

## Criterios y evidencias

| # | Requisito | Evidencia / estado |
| --- | --- | --- |
| 1 | Azure Boards con 2 Epics, 4 Features, 8 User Stories y Tasks vinculadas | Estructura revisada durante el proyecto; verificar nuevamente el árbol y estados en Azure Boards antes de cerrar |
| 2 | Flujo de ramas `feature/*`, `fix/*`, `refactor/*` y `main` estable | [Repositorio principal](https://github.com/JorgeDanielAchijLopez/it-incident-hub-semana-1) y [estrategia de ramas](https://github.com/JorgeDanielAchijLopez/it-incident-hub-semana-1/blob/main/docs/branching.md); verificar ejemplos de cada tipo |
| 3 | Trazabilidad de commits/PR con AB#ID | [Pull Requests](https://github.com/JorgeDanielAchijLopez/it-incident-hub-semana-1/pulls?q=is%3Apr+is%3Aclosed) y documentación del proyecto |
| 4 | Mínimo seis PR revisados | [Registro de doce PR](https://github.com/JorgeDanielAchijLopez/it-incident-hub-semana-1/blob/main/docs/ab29-evidencia-pull-requests.md); revisar aprobaciones reales en GitHub |
| 5 | Pipeline Azure con build, tests, seguridad y artefactos | [Documentación de Azure Pipelines](https://github.com/JorgeDanielAchijLopez/it-incident-hub-semana-1/blob/main/docs/ci-azure-agente-windows.md) y ejecuciones observadas en Azure DevOps |
| 6 | Agente autohospedado ejecutó un job | Capturas del pool `Default`, agente `ITIncidentHub-Windows` Online y trabajos exitosos |
| 7 | GitHub Actions complementario | [Workflow](https://github.com/JorgeDanielAchijLopez/it-incident-hub-semana-1/blob/main/.github/workflows/ci.yml); confirmar al menos una ejecución exitosa en [Actions](https://github.com/JorgeDanielAchijLopez/it-incident-hub-semana-1/actions) |
| 8 | Cinco deudas técnicas, dos corregidas | [Informe de auditoría y deuda](https://github.com/JorgeDanielAchijLopez/it-incident-hub-semana-1/blob/main/docs/ab34-informe-auditoria.md) |
| 9 | Vulnerabilidades de dependencias analizadas | [Auditoría y mitigaciones](https://github.com/JorgeDanielAchijLopez/it-incident-hub-semana-1/blob/main/docs/seguridad-dependencias.md); confirmar resultados de CI |
| 10 | Protección de secretos | [Escaneo Gitleaks](ab34-escaneo-gitleaks.md): 81 commits, cero hallazgos, exit 0; guardar captura; alcance limitado al historial del repositorio principal |
| 11 | SemVer `v1.0.0` | [Release publicado](https://github.com/JorgeDanielAchijLopez/it-incident-hub-semana-1/releases/tag/v1.0.0) |
| 12 | Tres repositorios semanales | [Trazabilidad de entregas](trazabilidad-entregas.md); Semana 3 es documental y reproduce el código mediante tag de Semana 1 |

## Verificaciones finales pendientes

- [x] Cierre de AB#7 mostrado en evidencia de Azure Boards; conservar la captura y comprobar los estados individuales de Features/Stories/Tasks antes de presentar el PDF.
- [x] GitHub Actions: [ejecución #30 exitosa](https://github.com/JorgeDanielAchijLopez/it-incident-hub-semana-1/actions/runs/40239671615) sobre el merge del PR #21.
- [ ] Confirmar ejemplos de todas las categorías de ramas exigidas.
- [x] Capturas de Gitleaks y aprobación de preproducción identificadas para el informe; conservar los originales al preparar el PDF.
- [ ] Preparar PDF final con evidencias y aclaración de que no se efectuó despliegue real a producción.
- [x] AB#7 aparece cerrado en la evidencia facilitada. La revisión final del cumplimiento se mantiene documentada y no se confunde con despliegue a producción.

## Validación posterior al release

El [PR #21](https://github.com/JorgeDanielAchijLopez/it-incident-hub-semana-1/pull/21) fue fusionado en `main` (`f3f5bab`). El cambio incluyó documentación final y una actualización del lockfile de backend para corregir la vulnerabilidad reportada en `body-parser`. El usuario verificó `npm run check` y `npm audit --prefix backend --omit=dev` con cero vulnerabilidades antes del merge. La ejecución [GitHub Actions #30](https://github.com/JorgeDanielAchijLopez/it-incident-hub-semana-1/actions/runs/40239671615) finalizó correctamente. El tag `v1.0.0` no se movió y permanece en `f55a55f`.

## Restricciones de veracidad

La publicación del release no implica despliegue a producción. El escaneo de Gitleaks no garantiza ausencia absoluta de secretos. La creación de tres repositorios no acredita por sí sola tres aplicaciones independientes. No atribuir fechas de desarrollo distintas de las registradas en GitHub.
