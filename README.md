<h1 align="center">DevSecOps</h1>

<p align="center">
  <img src="https://img.shields.io/badge/GitHub%20Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white" />
  <img src="https://img.shields.io/badge/SonarCloud-F3702A?style=flat-square&logo=sonarcloud&logoColor=white" />
  <img src="https://img.shields.io/badge/Snyk-4C4A73?style=flat-square&logo=snyk&logoColor=white" />
  <img src="https://img.shields.io/badge/Argo%20CD-EF7B4D?style=flat-square&logo=argo&logoColor=white" />
  <img src="https://img.shields.io/badge/Sigstore%20cosign-2088FF?style=flat-square" />
</p>

---

## Sobre este módulo

Integrar la seguridad en cada fase del ciclo de vida del desarrollo, no como una auditoría al final. La filosofía **shift-left**: cuanto antes se detecta una vulnerabilidad, más barata es de corregir. Seguridad como **responsabilidad compartida y automatizada** dentro del pipeline.

La masterclass recorre un pipeline **DevSecOps de extremo a extremo** sobre una aplicación Python: desde los controles de seguridad automáticos en el CI hasta el despliegue continuo en Kubernetes con GitOps, la firma de artefactos y la observabilidad en producción.

---

## Pipeline DevSecOps

Cada fase incorpora su propio control de seguridad automatizado. Un hallazgo crítico rompe el build antes de llegar a producción: la seguridad deja de ser un cuello de botella manual.

![Pipeline DevSecOps](devsecops-pipeline.png)

---

## Stack y qué resuelve cada pieza

| Fase | Herramienta | Qué aporta |
|---|---|---|
| **CI / Pipelines** | **GitHub Actions** | Orquesta el pipeline: cada push dispara build, tests y los controles de seguridad como *gates* automáticos |
| **SAST** | **SonarCloud** | Análisis estático del código en cada PR: bugs, code smells y vulnerabilidades antes del merge |
| **SCA** | **Snyk** | Escaneo de dependencias de terceros en busca de CVEs conocidos |
| **Dependencias** | **Renovate** | Pull requests automáticos para mantener las dependencias actualizadas (reduce la superficie de ataque) |
| **Firma de artefactos** | **cosign / Sigstore** | Firma criptográfica de las imágenes de contenedor para garantizar su integridad y procedencia |
| **GitOps / CD** | **Argo CD** | Despliegue continuo declarativo: el estado deseado vive en Git y Argo CD lo reconcilia en el clúster |
| **Orquestación** | **Kubernetes · Helm** | Despliegue y empaquetado de la aplicación en el clúster |
| **Observabilidad** | **Prometheus · KEDA** | Métricas en producción y **autoescalado** dirigido por eventos según la carga |

---

## Conceptos clave

- **Shift-left** — mover los controles (SAST, SCA, gestión de dependencias) lo más temprano posible, idealmente en el PR, no al final.
- **Pipeline como código** — los *gates* de seguridad viven en el repositorio y rompen el build ante hallazgos críticos, de forma reproducible y auditable.
- **GitOps** — Git como única fuente de verdad del estado de la infraestructura; Argo CD reconcilia el clúster con lo declarado.
- **Cadena de suministro segura** — firmar las imágenes (cosign/Sigstore) para poder verificar qué se despliega y de dónde viene.
- **Seguridad hasta producción** — la observabilidad (Prometheus) y el autoescalado (KEDA) extienden la mirada de seguridad y disponibilidad al runtime.

---

## Stack

`GitHub Actions` · `SonarCloud` · `Snyk` · `Renovate` · `cosign / Sigstore` · `Argo CD` · `Kubernetes` · `Helm` · `Prometheus` · `KEDA` · `Docker`

---

## Módulo relacionado

- **[IA y Ciberseguridad](https://github.com/juanmalbran/IA-y-Ciberseguridad)** — asegurar pipelines de MLOps aplica los mismos principios de shift-left.

---

<div align="center">
  <sub>Parte del portfolio de <a href="https://github.com/juanmalbran">Juan Malbrán · M4LBYTE</a></sub>
</div>
