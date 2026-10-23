# Escaneo de secretos — Gitleaks AB#34

**Proyecto:** IT Incident Hub  
**Repositorio analizado:** [it-incident-hub-semana-1](https://github.com/JorgeDanielAchijLopez/it-incident-hub-semana-1)  
**Herramienta:** Gitleaks 8.30.1  
**Entorno:** Windows PowerShell  
**Fuente de evidencia:** salida de terminal facilitada por el responsable del proyecto.

## Comando ejecutado

```powershell
& $gitleaks git --redact --report-format json --report-path "$env:TEMP\it-incident-hub-gitleaks.json" .
Write-Host "Codigo de salida: $LASTEXITCODE"
```

## Resultado observado

| Indicador | Resultado |
| --- | --- |
| Commits escaneados | 81 |
| Volumen escaneado | Aproximadamente 514.08 KB |
| Duración | 1.12 segundos |
| Mensaje | `no leaks found` |
| Código de salida | `0` |
| Hallazgos detectados | 0 |

**Interpretación:** Gitleaks no identificó secretos con sus reglas de detección en el historial Git accesible desde la copia local analizada. Esto respalda el control de escaneo de historial solicitado para AB#34 y el Epic AB#7.

## Alcance y límites

- El escaneo se ejecutó sobre el repositorio local de Semana 1; no constituye automáticamente un escaneo independiente de los repositorios de Semanas 2 y 3.
- No se ha acreditado un escaneo de archivos ignorados o no versionados, de capturas, artefactos descargados, entornos externos o gestores de secretos.
- Un resultado sin hallazgos no prueba ausencia absoluta de credenciales.
- El informe JSON se generó en la carpeta temporal del equipo; **no se subió a GitHub**. No publicar credenciales ni reportes sin revisarlos.
- La evidencia primaria para la entrega es la captura de terminal donde se ven versión, comando, `81 commits scanned`, `no leaks found` y `Codigo de salida: 0`.

## Seguimiento

Conservar la captura en las evidencias de la entrega final. Ejecutar Gitleaks periódicamente y repetir el análisis si se incorpora historial adicional. Revisar separadamente archivos locales ignorados y artefactos antes de distribuirlos.
