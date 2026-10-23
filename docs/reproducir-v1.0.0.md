# Reproducir la versión v1.0.0 — Entrega Semana 3

**Proyecto:** IT Incident Hub  
**Responsable:** Jorge Daniel Achij López  
**Fuente de código:** [repositorio principal](https://github.com/JorgeDanielAchijLopez/it-incident-hub-semana-1)  
**Versión:** [v1.0.0](https://github.com/JorgeDanielAchijLopez/it-incident-hub-semana-1/releases/tag/v1.0.0)

> Este repositorio de Semana 3 conserva documentación y evidencias. **El código ejecutable está en el repositorio principal**, fijado mediante la etiqueta de lanzamiento. No se presenta como una copia independiente del programa.

## Requisitos locales

Windows con PowerShell, Git, Node.js 24, npm y Docker Desktop con contenedores Linux. Verificar que los puertos 5433, 3000 y 5173 estén libres.

## Obtener exactamente el código publicado

En PowerShell, desde una carpeta de trabajo:

```powershell
git clone --branch v1.0.0 --single-branch https://github.com/JorgeDanielAchijLopez/it-incident-hub-semana-1.git it-incident-hub-v1.0.0
cd it-incident-hub-v1.0.0
git describe --tags --exact-match
git rev-parse HEAD
git status --short
```

El primer comando selecciona el tag y deja HEAD desacoplado; esto es normal para reproducir una versión publicada. Comparar el SHA obtenido con el commit indicado en la página del release; **no dar por válida una versión solo por su nombre**.

## Instalar y comprobar

```powershell
npm ci
npm ci --prefix backend
npm ci --prefix frontend
npm run check
node scripts/auditar-dependencias.cjs --self-test
node scripts/auditar-dependencias.cjs auditorias
```

Estas comprobaciones necesitan acceso a npm. Si falla una auditoría por indisponibilidad de red, registrar el error y repetir; no interpretarlo como cero vulnerabilidades.

## Preparar base de datos local

```powershell
Copy-Item database/.env.example database/.env
notepad database/.env
```

Sustituir el marcador por una contraseña local privada. Crear `backend/.env` con los nombres `DB_HOST`, `DB_PORT`, `DB_NAME`, `DB_USER`, `DB_PASSWORD` y `PORT`, usando la misma contraseña y los valores documentados en el [README del código fuente](https://github.com/JorgeDanielAchijLopez/it-incident-hub-semana-1/blob/main/README.md). **No publicar estos archivos ni sus valores.**

```powershell
docker compose --env-file database/.env -f database/compose.yaml up -d --wait
```

En una base nueva, aplicar las migraciones SQL **una sola vez** y en orden, siguiendo el README de la versión descargada. No ejecutar migraciones a ciegas sobre datos existentes.

## Ejecutar

```powershell
npm run dev
```

- Interfaz: http://localhost:5173
- API: http://127.0.0.1:3000/api
- Salud: http://127.0.0.1:3000/api/health

Con API y PostgreSQL iniciados, ejecutar pruebas de integración:

```powershell
powershell -NoProfile -ExecutionPolicy Bypass -File .\tests\ab21-pruebas-indicadores.ps1
```

## Evidencias y alcance

- [GitHub Actions](https://github.com/JorgeDanielAchijLopez/it-incident-hub-semana-1/actions)
- [Pull Requests revisados](https://github.com/JorgeDanielAchijLopez/it-incident-hub-semana-1/blob/main/docs/ab29-evidencia-pull-requests.md)
- [Pipeline Azure y correcciones](https://github.com/JorgeDanielAchijLopez/it-incident-hub-semana-1/blob/main/docs/ci-azure-agente-windows.md)
- [Release y artefactos](https://github.com/JorgeDanielAchijLopez/it-incident-hub-semana-1/releases/tag/v1.0.0)
- [Trazabilidad de las tres semanas](trazabilidad-entregas.md)

**Limitación:** esta guía es reproducible a partir del repositorio principal y su tag; no acredita que los comandos se hayan ejecutado de nuevo desde esta entrega ni constituye despliegue a producción. Conservar capturas de resultados locales y Azure DevOps para el PDF final.
