
---

## Entrega 2 - Integracion continua con Jenkins

Se agrega Jenkins como gestor de operaciones. Jenkins corre en su propio contenedor y ejecuta el `Jenkinsfile` del repositorio: construye las imagenes, levanta `app` y `nginx` y verifica que se comunican.

| Archivo | Funcion |
|---|---|
| `Jenkinsfile` | Pipeline: checkout, build, up, verificacion, limpieza |
| `docker-compose.jenkins.yml` | Levanta Jenkins en el puerto 8081 |
| `jenkins/Dockerfile` | Jenkins LTS con Docker CLI y Compose |
| `jenkins/plugins.txt` | Plugins preinstalados |
| `docs/ENTREGA2-JENKINS.md` | Guia paso a paso y solucion de problemas |
| `docs/evidencias/` | Capturas de la ejecucion |

Para ejecutarlo:

```bash
docker compose -f docker-compose.jenkins.yml up -d --build
```

Luego abrir http://localhost:8081 y seguir `docs/ENTREGA2-JENKINS.md`.
