# Trazabilidad de las tres entregas — IT Incident Hub

**Responsable:** Jorge Daniel Achij López  
**Proyecto Azure DevOps:** [IT-Incident-Hub](https://dev.azure.com/devopsOrganizativaUMG01/IT-Incident-Hub)  
**Modalidad:** proyecto académico individual con revisión simulada mediante cuentas propias.

## Repositorios

| Entrega | Repositorio | Evidencia disponible | Alcance |
| --- | --- | --- | --- |
| Semana 1 (12–18 octubre 2026) | [it-incident-hub-semana-1](https://github.com/JorgeDanielAchijLopez/it-incident-hub-semana-1) | Código fuente, historial de commits, PR y arquitectura | Planificación, PostgreSQL, API y React inicial |
| Semana 2 (19–25 octubre 2026) | [it-incident-hub-semana-2](https://github.com/JorgeDanielAchijLopez/it-incident-hub-semana-2) | Copia versionada del código y documentación de CI/seguridad | Integración, pruebas, auditorías y correcciones |
| Semana 3 (26 octubre–1 noviembre 2026, planificada) | [it-incident-hub-semana-3](https://github.com/JorgeDanielAchijLopez/it-incident-hub-semana-3) | README y [registro de evidencias](docs/evidencias-release.md) | Documentación de estabilización y entrega final en preparación |

> Las fechas de las semanas son las del plan académico. Los archivos de este repositorio pueden prepararse antes del inicio de Semana 3; su fecha real de commit es la que informa GitHub. No se atribuyen retrospectivamente cambios a otra semana.

## Cadena de trazabilidad

1. **Planificación:** [Azure Boards](https://dev.azure.com/devopsOrganizativaUMG01/IT-Incident-Hub) contiene Epics, Features, User Stories y Tasks.
2. **Implementación:** el [historial de PR del repositorio principal](https://github.com/JorgeDanielAchijLopez/it-incident-hub-semana-1/pulls?q=is%3Apr+is%3Aclosed) conserva ramas, cambios, revisiones y fusiones.
3. **Revisiones:** [tabla de 12 PR documentados](https://github.com/JorgeDanielAchijLopez/it-incident-hub-semana-1/blob/main/docs/ab29-evidencia-pull-requests.md).
4. **Integración continua:** [GitHub Actions](https://github.com/JorgeDanielAchijLopez/it-incident-hub-semana-1/actions) y Azure Pipelines con agente Windows propio.
5. **Corrección de fallos:** [registro de Azure CI](https://github.com/JorgeDanielAchijLopez/it-incident-hub-semana-1/blob/main/docs/ci-azure-agente-windows.md).
6. **Seguridad:** [auditoría y deudas técnicas](https://github.com/JorgeDanielAchijLopez/it-incident-hub-semana-1/blob/main/docs/ab34-informe-auditoria.md).
7. **Versionado:** [release v1.0.0](https://github.com/JorgeDanielAchijLopez/it-incident-hub-semana-1/releases/tag/v1.0.0).

## Alcance y comprobaciones pendientes

- El repositorio de Semana 3 **todavía no contiene una copia ejecutable** del frontend, backend y base de datos. Para ejecutar la aplicación usar el repositorio principal y las instrucciones de su README.
- Para afirmar que cada entrega es reproducible de forma independiente, documentar el SHA de origen, las instrucciones y los artefactos específicos de cada una.
- La documentación de seguridad reconoce que no se ha acreditado un escaneo integral de secretos del historial Git.
- La aprobación de preproducción no es un despliegue real a producción.
- Adjuntar capturas verificables de Azure Boards, pipelines, aprobación y release al informe final.

**Estado del criterio de tres repositorios:** existencia verificada; diferenciación documental presente; reproducibilidad y cierre académico pendientes de validación.
