# 🧭 Comandos esenciales de terminal (zsh)
Guía práctica y limpia para navegación y manipulación básica de archivos desde la terminal.

## 📂 Navegación básica

```bash
cd ~/Documentos
ls -lh
tree
pwd
open .
```

## 🔁 Rutas relativas y navegación avanzada

```bash
cd ..
cd ../..
cd ../../..
cd -
echo ~
echo ~+
echo ~-
```

### 📌 Ejemplo práctico

`cd ../src` desde `/usr/local/share` te lleva a `/usr/local/src`.

## 👥 Navegación multiusuario

```bash
cd ~username
```

## 🗂️ Manejo de archivos y carpetas

```bash
mkdir nueva_carpeta
touch archivo.txt
mv archivo.txt carpeta/
cp archivo.txt copia.txt
rm archivo.txt
rm -rf carpeta
```

## 📄 Lectura rápida de archivos de texto

```bash
cat archivo.txt
head archivo.txt
head -n 20 archivo.txt
tail archivo.txt
tail -n 15 archivo.txt
```

## 🎯 Wildcards (comodines)

```bash
ls *.txt
ls datos*
ls datos?
ls datos???
ls [[:upper:]]*
ls -d [[:upper:]]*
ls [[:lower:]]*
ls [ad]*
```

## 🔍 Búsqueda de archivos

```bash
which python
find . -name "*.ipynb"
find . -type f -name "*.csv"
find . -size +20M
```

## 👑 grep y wc — Búsqueda de texto y conteo

```bash
grep "cadena" archivo.txt
grep -i "texto" archivo.txt
grep -v "error" archivo.txt
grep -c "hola" archivo.txt
cat archivo.txt | grep "algo"
ls -al | grep "archivo"
grep "Imagina .* algo" test.txt

wc archivo.txt
wc -l archivo.txt
wc -w archivo.txt
wc -c archivo.txt
```

## 🧮 Contar coincidencias en múltiples archivos

```bash
grep -c "hola" archivo1.txt archivo2.txt
grep -o "hola" archivo*.txt | wc -l
grep -ro "hola" . | wc -l
```

## 🎛️ Manejo de procesos (foreground / background)

```bash
Ctrl + C
Ctrl + Z
bg %1
fg %1
jobs
```

## ⌨️ Edición rápida en el prompt (bash/zsh)

| Atajo              | Acción                                                    |
|--------------------|-----------------------------------------------------------|
| `Ctrl + U`         | Borra desde el cursor hasta el inicio de la línea        |
| `Ctrl + K`         | Borra desde el cursor hasta el final de la línea         |
| `Ctrl + W`         | Borra la palabra anterior                                 |
| `Ctrl + A`         | Va al inicio de la línea                                  |
| `Ctrl + E`         | Va al final de la línea                                   |
| `Ctrl + L`         | Limpia toda la pantalla                                   |
| `Alt + Backspace`  | Borra una palabra hacia atrás                             |
| `Ctrl + C`         | Cancela el comando actual                                 |