# Development setup

Pasos rápidos para trabajar con este proyecto localmente.

1) Crear y activar el entorno virtual

```bash
# Crear (ya puede existir en `.venv` si ya lo creaste)
python3 -m venv .venv

# Activar (bash / zsh)
source .venv/bin/activate

# Actualizar pip y herramientas
pip install -U pip setuptools wheel
```

2) Instalar el paquete (usa `pyproject.toml`)

```bash
# Instalación editable (instala dependencias listadas en pyproject.toml)
pip install -e .
```

3) Activar y verificar

```bash
source .venv/bin/activate
python -V
pip list
```

4) Preparar repo Git local (si aún no existe)

```bash
# Inicializar, añadir y commitear
git init
git add .
# Ajusta user/email si es necesario
git -c user.name="MiguelBarriosAl" -c user.email="miguel@example.com" commit -m "Initial commit"
```

5) Conectar con GitHub y pushear

Opción A — usando GitHub CLI (`gh`, recomendado):

```bash
# Instala y autentica (sigue las instrucciones interactivas)
gh auth login
# Crear repositorio remoto privado y hacer push
gh repo create MiguelBarriosAl/REPO_NAME --private --source=. --remote=origin --push
```

Opción B — usando GitHub web y HTTPS/SSH:

1. Crea un repo nuevo en https://github.com/new (nombre: `REPO_NAME`).
2. Luego en tu terminal (reemplaza la URL por la de tu repositorio):

```bash
git remote add origin https://github.com/MiguelBarriosAl/REPO_NAME.git
git push -u origin main
```

Si usas SSH, añade tu clave SSH a GitHub y usa la URL SSH en `git remote add`.

Notas:
- Reemplaza `REPO_NAME` por el nombre que quieras darle.
- El commit inicial aquí se hizo usando un nombre/email temporal; si prefieres, configura tu usuario real con:
  `git config --local user.name "Tu Nombre"` y `git config --local user.email "tu@correo"`.
