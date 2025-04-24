
# 🧾 Comandos Git – Flujo básico y Cheat Sheet

## ✅ Flujo básico
```bash
git status                 # Ver qué cambió
git add archivo.md         # Añadir archivo al staging
git commit -m "Mensaje"    # Crear commit
git push                   # Subir a GitHub
```

## 🌿 Ramas
```bash
git branch                 # Lista las ramas locales existentes
git branch nueva-rama     # Crea una nueva rama llamada 'nueva-rama'
git switch nueva-rama     # Cambia a la rama 'nueva-rama'
git merge nombre-rama     # Fusiona 'nombre-rama' a la rama actual
```

## 🔍 Inspección
```bash
git log                   # Muestra el historial de commits
git diff                  # Muestra los cambios no preparados (unstaged)
git diff --staged         # Muestra los cambios preparados (staged)
git blame archivo         # Muestra quién modificó cada línea del archivo
```

## ⏪ Deshacer y recuperar
```bash
git restore archivo           # Revierte cambios no guardados en 'archivo'
git checkout <commit>         # Cambia el estado del repo a un commit anterior
git reset --soft HEAD~1       # Elimina el último commit pero conserva los cambios
git reflog                    # Muestra el historial de movimientos de HEAD (útil para recuperar)
```

## 🚀 Push, pull y remoto
```bash
git remote -v                     # Muestra las URLs de los repositorios remotos
git remote add origin <url>      # Conecta tu repositorio local con uno remoto
git push -u origin main          # Sube tu rama principal al repositorio remoto
git pull origin main             # Trae cambios del remoto y los fusiona con tu rama actual
```

## ⚙️ Configuración
```bash
git config --global user.name "TuNombre"       # Define tu nombre de usuario globalmente
git config --global user.email "tu@correo.com" # Define tu correo global para Git
```

## 🪄 Alias útil (opcional)
```bash
git config --global alias.lg "log --oneline --graph --all --decorate"
# Crea un alias 'lg' para ver el historial en una línea por commit con grafo de ramas
```

## 🧪 GitHub CLI (gh)
```bash
gh auth login
# Inicia sesión con GitHub desde la terminal (elige SSH si ya tienes clave configurada)

gh repo create proyecto_sismos --public --source=. --remote=origin --push
# Crea y sube un repositorio desde tu carpeta actual en un solo paso

gh repo clone usuario/repositorio
# Clona un repositorio desde GitHub usando gh

gh repo view --web
# Abre el repositorio actual en tu navegador
```

✅ La GitHub CLI (`gh`) es ideal para automatizar flujos desde la terminal sin entrar al navegador.
