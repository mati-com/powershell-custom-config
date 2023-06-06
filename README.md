# PowerShell Custom

Personalización de PowerShell con Oh-My-Posh, Nerd Font y Terminal Icons


## Instalación y Guia

Primero Instalar OhMyPosh:
```bash
  winget install JanDeDobbeleer.OhMyPosh -s winget
```
Creamos el perfil:
```bash
  New-Item -Path $PROFILE -Type File -Force
```
Ingresamos con un editor de texto a nuestro $PROFILE script de powershell:
```
  notepad $PROFILE
```
Añadimos la siguiente linea dentro de nuestro $PROFILE:
```
  oh-my-posh init pwsh | Invoke-Expression
```
Luego tenemos que descargar de Nerd Fonts una fuente, instalar y agregarla como default en la Terminal de PowerShell: https://www.nerdfonts.com/font-downloads

## Temas

Temas para nuestra terminal : 
```
  Get-PoshThemes
```
Agregamos la siguiente linea en nuestro $PROFILE, y modificamos el "ejemplo" por el nombre del tema que nos gusta guardar, cerrar y abrir nuevamente la terminal:
```
oh-my-posh init pwsh --config "$env:POSH_THEMES_PATH\Ejemplo.omp.json" | Invoke-Expression
```
## Iconos
Para instalar iconos en la terminal:
```
Install-Module -Name Terminal-Icons -Repository PSGallery
```
Por ultimo agregamos la siguiente linea a nuestro $PROFILE:
```
Import-Module -Name Terminal-Icons
```
