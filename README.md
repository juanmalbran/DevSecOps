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

La masterclass recorre un pipeline **DevSecOps de extremo a extremo** sobre una aplicación Python: de los controles de seguridad automáticos en el CI al despliegue continuo en Kubernetes con GitOps, la firma de artefactos y la observabilidad en producción.

---

## Pipeline S-SDLC — un control de seguridad en cada fase

![Pipeline DevSecOps](devsecops-pipeline.png)

| Fase | Qué se hace | Herramientas |
|---|---|---|
| **Plan** | Modelado de amenazas y requisitos de seguridad desde el diseño | **STRIDE**, Threat Modeling |
| **Code** | Análisis estático del código y controles previos al commit | **SonarCloud (SAST)**, Conventional Commits, pre-commit hooks |
| **Build** | Construcción de la imagen, firma y bill of materials | **Docker**, **cosign / Sigstore** (firma), **SBOM** |
| **Test** | Escaneo de dependencias, dinámico y de secretos | **Snyk (SCA)**, DAST, secret scanning |
| **Release** | Versionado y actualización automática de dependencias | semantic-release, **Renovate** |
| **Deploy** | Despliegue declarativo por GitOps sobre Kubernetes | **Argo CD**, Sealed Secrets, Image Updater, **Helm** |
| **Monitor** | Observabilidad y autoescalado en producción | **Prometheus**, **KEDA**, Grafana, AlertManager |

Un hallazgo crítico en cualquier gate **rompe el build** antes de llegar a producción: la seguridad deja de ser un cuello de botella manual.

---

## Conceptos clave

- **Shift-left** — mover los controles (SAST, SCA, gestión de dependencias, secret scanning) lo más temprano posible, idealmente en el PR.
- **Pipeline como código** — los *gates* de seguridad viven en el repositorio y se ejecutan solos, de forma reproducible y auditable.
- **GitOps** — Git como única fuente de verdad del estado del clúster; **Argo CD** reconcilia lo declarado en producción.
- **Cadena de suministro segura** — firmar imágenes con **cosign/Sigstore** y generar el **SBOM** permite verificar qué se despliega y de dónde viene.
- **Seguridad hasta el runtime** — la observabilidad (Prometheus/Grafana) y el autoescalado por eventos (**KEDA**) extienden la mirada de seguridad y disponibilidad a producción.

---

## Stack

`GitHub Actions` · `SonarCloud` · `Snyk` · `Renovate` · `cosign / Sigstore` · `SBOM` · `Argo CD` · `Kubernetes` · `Helm` · `Prometheus` · `KEDA` · `Grafana` · `Docker`

---

## Módulo relacionado

- **[IA y Ciberseguridad](https://github.com/juanmalbran/IA-y-Ciberseguridad)** — asegurar pipelines de MLOps aplica los mismos principios de shift-left.

---

<div align="center">
  <sub>Parte del portfolio de <a href="https://github.com/juanmalbran">Juan Malbrán · M4LBYTE</a></sub>
</div>
