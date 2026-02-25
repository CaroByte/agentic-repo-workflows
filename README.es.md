# 🤖 Agentic Repo

<div align="center">

[![YouTube Channel Subscribers](https://img.shields.io/youtube/channel/subscribers/UC140iBrEZbOtvxWsJ-Tb0lQ?style=for-the-badge&logo=youtube&logoColor=white&color=red)](https://www.youtube.com/c/GiselaTorres?sub_confirmation=1)
[![GitHub followers](https://img.shields.io/github/followers/CaroByte?style=for-the-badge&logo=github&logoColor=white)](https://github.com/CaroByte)
[![LinkedIn Follow](https://img.shields.io/badge/LinkedIn-Sígueme-blue?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/giselatorresbuitrago/)
[![X Follow](https://img.shields.io/badge/X-Sígueme-black?style=for-the-badge&logo=x&logoColor=white)](https://twitter.com/0GiS0)

**🇬🇧 [Read in English](README.md)**

</div>

---

¡Hola developer 👋🏻! Este repositorio contiene una colección de **workflows de GitHub reutilizables** potenciados por **GitHub Copilot CLI** para automatización inteligente de tus repositorios.

## ✨ Características

- **✍️ Issue Quality Enhancer** — Mejora automáticamente títulos y cuerpos de issues, traduce a inglés, añade estructura y referencias al código
- **🏷️ Smart Labeler** — Analiza issues y PRs para asignar las etiquetas más apropiadas
- **💡 Copilot Suggester** — Escanea tu código y crea discusiones con ideas de mejora (seguridad, rendimiento, UX, etc.)
- **🏷️✨ Label Beautifier** — Moderniza todas tus etiquetas con emojis, descripciones y colores consistentes
- **� Continuous Documentation** — Mejora fragmentos del README y docs de API conforme el código evoluciona; avisa a los autores de PR cuando las explicaciones se desvían de la implementación real
- **�🚀 Workflow Installer** — Despliega estos workflows a múltiples repos con un solo click

## 🛠️ Tecnologías

- GitHub Actions
- GitHub Copilot CLI
- GitHub MCP Server
- Playwright MCP Server (para análisis de UI)

## 📋 Requisitos Previos

- Cuenta de GitHub con **acceso a Copilot**
- Un **Personal Access Token (PAT)** con permisos de Copilot guardado como secreto `COPILOT_PAT`

## 🚀 Instalación

### Opción 1: Usar como Workflows Reutilizables (Recomendado)

Copia los caller workflows de `caller-workflows/` a `.github/workflows/` de tu repo:

```bash
# Clona este repo
git clone https://github.com/CaroByte/agentic-repo-workflows.git

# Copia los caller workflows que quieras
cp agentic-repo-workflows/caller-workflows/*.yml tu-repo/.github/workflows/
```

Cada caller tiene ~15 líneas y referencia la lógica principal aquí, así siempre tienes la última versión.

### Opción 2: Usar el Workflow Installer

1. Ve a **Actions** → **🚀 Workflow Installer**
2. Introduce los repos destino (separados por coma): `repo1, repo2, org/repo3`
3. Elige qué workflows instalar
4. Selecciona si crear un PR o pushear directamente
5. ¡Ejecuta!

### Opción 3: Copiar Workflows Completos

Copia los workflows directamente de `.github/workflows/` si prefieres control total.

## 💻 Uso

### Issue Quality Enhancer
Se activa automáticamente cuando se abre un issue. Mejora título, cuerpo y añade etiquetas.

### Smart Labeler
Se activa al abrir/editar issues o PRs. Analiza el contenido y asigna etiquetas apropiadas.

### Copilot Suggester
Ejecución manual desde la pestaña Actions. Analiza tu código y crea discusiones con ideas.

### Label Beautifier
Ejecución manual. Usa `dry_run: true` primero para previsualizar cambios.

### Continuous Documentation
Se activa automáticamente en PRs que modifican archivos de código. Compara los cambios con las secciones existentes del README y la documentación de API, sugiere actualizaciones y deja un comentario de revisión cuando la documentación se desvía de la implementación.

## 📁 Estructura del Proyecto

```
agentic-repo-workflows/
├── .github/
│   └── workflows/
│       ├── issue-quality-enhancer.yml    # Workflow reutilizable
│       ├── smart-labeler.yml             # Workflow reutilizable
│       ├── the-suggester-discussion-mode.yml  # Workflow reutilizable
│       ├── label-beautifier.yml          # Workflow reutilizable
│       ├── continuous-docs.yml            # Workflow reutilizable
│       └── workflow-installer.yml        # Utilidad de instalación
├── caller-workflows/                     # Callers ligeros para otros repos
│   ├── issue-quality-enhancer.yml
│   ├── smart-labeler.yml
│   ├── the-suggester-discussion-mode.yml
│   ├── label-beautifier.yml
│   └── continuous-docs.yml
├── README.md                             # Documentación en inglés
└── README.es.md                          # Documentación en español
```

## ⚙️ Configuración Requerida en Repos Destino

Añade este secreto a cualquier repo que use estos workflows:
- `COPILOT_PAT` — GitHub PAT con acceso a Copilot

---

## 🌐 Sígueme

<div align="center">

[![YouTube Channel Subscribers](https://img.shields.io/youtube/channel/subscribers/UC140iBrEZbOtvxWsJ-Tb0lQ?style=for-the-badge&logo=youtube&logoColor=white&color=red)](https://www.youtube.com/c/GiselaTorres?sub_confirmation=1)
[![GitHub followers](https://img.shields.io/github/followers/CaroByte?style=for-the-badge&logo=github&logoColor=white)](https://github.com/CaroByte)
[![LinkedIn Follow](https://img.shields.io/badge/LinkedIn-Sígueme-blue?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/giselatorresbuitrago/)
[![X Follow](https://img.shields.io/badge/X-Sígueme-black?style=for-the-badge&logo=x&logoColor=white)](https://twitter.com/0GiS0)

</div>
