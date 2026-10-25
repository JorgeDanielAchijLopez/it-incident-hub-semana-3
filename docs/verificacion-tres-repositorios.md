# Verificación de evolución — tres repositorios

**Proyecto:** IT Incident Hub  
**Responsable:** Jorge Daniel Achij López  
**Criterio:** Epic AB#7, aceptación 12: tres repositorios con evolución y trazabilidad verificables.

## Referencias verificadas en GitHub

| Entrega | Repositorio | Último commit observado al realizar esta verificación | Evidencia |
| --- | --- | --- | --- |
| Semana 1 | [it-incident-hub-semana-1](https://github.com/JorgeDanielAchijLopez/it-incident-hub-semana-1) | [`f3f5bab`](https://github.com/JorgeDanielAchijLopez/it-incident-hub-semana-1/commit/f3f5babfc69905f695e139bc0f61ee8232e628f1) | Código funcional, PR #21 fusionado, CI; tag v1.0.0 conservado en `f55a55f` |
| Semana 2 | [it-incident-hub-semana-2](https://github.com/JorgeDanielAchijLopez/it-incident-hub-semana-2) | [`3338443`](https://github.com/JorgeDanielAchijLopez/it-incident-hub-semana-2/commit/333844319100bc1dbc4c3db7a1f1dabcee20f76b) | Código versionado, CI, pruebas y documentación de seguridad |
| Semana 3 | [it-incident-hub-semana-3](https://github.com/JorgeDanielAchijLopez/it-incident-hub-semana-3) | [`f2c545c`](https://github.com/JorgeDanielAchijLopez/it-incident-hub-semana-3/commit/f2c545c7b293da51a831ba301468e21c070e5322) | README, evidencias del release, Gitleaks, reproducción desde tag y checklist de cierre |

## Actualización posterior al release

El [PR #21](https://github.com/JorgeDanielAchijLopez/it-incident-hub-semana-1/pull/21) se fusionó en `main` como `f3f5bab`. Incluye la actualización documental AB#35 y la corrección de `body-parser`. La [ejecución #30 de GitHub Actions](https://github.com/JorgeDanielAchijLopez/it-incident-hub-semana-1/actions/runs/40239671615) concluyó con éxito. El tag `v1.0.0` sigue señalando `f55a55f`, por lo que reproducir el tag y ejecutar el último `main` no son operaciones equivalentes.

## Interpretación

Los tres repositorios existen, contienen commits reales y presentan contenido diferenciado. La documentación de Semana 3 enlaza el release y las evidencias del repositorio principal. El historial y las fechas de GitHub deben consultarse directamente para comprobar la secuencia real; no se deben interpretar los nombres «Semana 1», «Semana 2» y «Semana 3» como prueba automática de que cada cambio ocurrió dentro de un intervalo determinado.

**Limitación:** el repositorio de Semana 3 es documental y depende del tag `v1.0.0` de Semana 1 para reproducir la aplicación. Esta verificación acredita existencia, historial y diferenciación de entregas, pero no prueba por sí sola tres builds independientes.

## Evidencias complementarias

- [Historial de PR](https://github.com/JorgeDanielAchijLopez/it-incident-hub-semana-1/pulls?q=is%3Apr+is%3Aclosed)
- [Release v1.0.0](https://github.com/JorgeDanielAchijLopez/it-incident-hub-semana-1/releases/tag/v1.0.0)
- [GitHub Actions](https://github.com/JorgeDanielAchijLopez/it-incident-hub-semana-1/actions)
- [Guía de reproducción](reproducir-v1.0.0.md)
- [Evidencias del lanzamiento](evidencias-release.md)

**Conclusión:** criterio 12 respaldado documentalmente respecto a los tres repositorios y su trazabilidad; la valoración de si se exige una entrega ejecutable independiente por semana corresponde al enunciado y a su evaluación.
