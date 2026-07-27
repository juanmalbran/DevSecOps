<h1 align="center">DevSecOps</h1>

<p align="center">
  <img src="https://img.shields.io/badge/CI%2FCD-2088FF?style=flat-square&logo=githubactions&logoColor=white" />
  <img src="https://img.shields.io/badge/SAST%2FDAST-3FB950?style=flat-square" />
  <img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white" />
  <img src="https://img.shields.io/badge/Trivy-1904DA?style=flat-square&logo=aqua&logoColor=white" />
</p>

---

## Sobre este módulo

Integrar la seguridad en cada fase del ciclo de vida del desarrollo, no como una auditoría al final. La filosofía **shift-left**: cuanto antes se detecta una vulnerabilidad, más barata es de corregir. Seguridad como responsabilidad compartida y automatizada.

**Temas cubiertos:** ciclo de vida de desarrollo seguro (SSDLC) · SAST, DAST y SCA · seguridad de contenedores e imágenes · gestión de secretos · seguridad en pipelines CI/CD · infraestructura como código (IaC) · modelado de amenazas.

---

## Pipeline DevSecOps

Cada fase incorpora su propio control de seguridad automatizado. Un hallazgo crítico rompe el build antes de llegar a producción: la seguridad deja de ser un cuello de botella manual.

![Pipeline DevSecOps](devsecops-pipeline.png)

---

## Temas destacados

- **Shift-left** — SAST sobre el código, SCA sobre las dependencias, gestión de secretos antes del commit.
- **Contenedores** — escaneo de imágenes (Trivy), imágenes mínimas, principio de menor privilegio.
- **Pipeline como código** — controles de seguridad como gates automáticos en CI/CD que rompen el build ante hallazgos críticos.
- **Modelado de amenazas** — STRIDE aplicado en fase de diseño.

---

## Stack

`GitHub Actions` · `Trivy` · `Semgrep` · `OWASP ZAP` · `Docker` · `Terraform` · `git-secrets`

---

## Módulo relacionado

- **[IA y Ciberseguridad](https://github.com/juanmalbran/IA-y-Ciberseguridad)** — asegurar pipelines de MLOps aplica los mismos principios de shift-left.

---

<div align="center">
  <sub>Parte del portfolio de <a href="https://github.com/juanmalbran">Juan Malbrán · M4LBYTE</a></sub>
</div>
