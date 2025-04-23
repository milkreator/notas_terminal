# 🧾 Comandos Git – Flujo básico y Cheat Sheet

```bash
git init
git status
git add archivo.py
git commit -m "Mensaje"
git push
git branch rama
git switch rama
ssh-keygen -t ed25519 -C "tucorreo@example.com"
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_ed25519
cat ~/.ssh/id_ed25519.pub
```

## 🧠 Git Cheat Sheet – Comandos clave

### 🟢 Inicio rápido

```bash
git init
git clone <url>
```

### 🧱 Commit y staging



## ✅ Flujo básico (recordatorio)

```bash
git status                 # Ver qué cambió
git add archivo.md         # Añadir archivo al staging
git commit -m "Mensaje"    # Crear commit
git push                   # Subir a GitHub
```

### 🌿 Ramas

```bash
git branch
git branch nueva-rama
git switch nueva-rama
git merge nombre-rama
```

### 🔍 Inspección

```bash
git log
git diff
git diff --staged
git blame archivo
```

### ⏪ Deshacer y recuperar

```bash
git restore archivo
git checkout <commit>
git reset --soft HEAD~1
git reflog
```

### 🚀 Push, pull y remoto

```bash
git remote -v
git remote add origin <url>
git push -u origin main
git pull origin main
```

### ⚙️ Configuración

```bash
git config --global user.name "TuNombre"
git config --global user.email "tu@correo.com"
```

### 🪄 Alias útil (opcional)

```bash
git config --global alias.lg "log --oneline --graph --all --decorate"
```
