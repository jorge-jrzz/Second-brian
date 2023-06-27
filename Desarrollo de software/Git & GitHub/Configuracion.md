---
banner_icon: ⚙️
banner: "![[gemini-vi_31191744012_o.jpg]]"
banner_y: 0.444
---

# Configuración inicial de Git 

Configuración del nombre:
```bash
git config --global user.name "Jorge Juarez"
```

Configuración del correo electrónico:
```bash
git config --global user.email jorgeang33@gmail.com
```

Configuración del editor de código (VS Code):
```bash
git config --global core.editor "code --wait"
```

##### Configuración de autocrlf (el formato de fin de línea):
+ Configuración en Windows:
	```bash
	git config --global core.autocrlf true
	```

+ Configuración en MacOS y Linux:
	```bash
	git config --global core.autocrlf input
	```

Confirmación de la configuración inicial:
```bash
git config --global -e
```

Ayuda con la configuración inicial de git:
```bash
git config -h
```

## Configuración opcional del Git

Configurar alias para comandos frecuentemente utilizados o para abreviar comandos largos.

```bash
git config --global alias.st status
```

Así, podrías usar `git st` en lugar de `git status`.
