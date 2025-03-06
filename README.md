## Personalización de la terminal de ArchLinux

Este es el repositorio con instrucciones del video de YouTube: [API REST con Laravel 11 y JWT: Auth, Roles y Railway](https://youtu.be/xPR0p2DY9JM?si=nM0RvIQ8tsIxY18T) 

## Apóyanos

[Suscríbete](https://www.youtube.com/@CesarSebastianDev?sub_confirmation=1) a nuestro canal de YouTube

Donaciones por Paypal: [https://www.paypal.com/donate/?hosted_button_id=UNLT89FVZF6TE](https://www.paypal.com/donate/?hosted_button_id=UNLT89FVZF6TE)

## Instrucciones paso a paso:

## Actualizar el repositorio oficial de ArchLinux

```
sudo pacman -Sy
```
---

## Actualizar los paquetes ya instalados en ArchLinux

```
sudo pacman -Syu
```
---

## Instalar el shell Zsh
```
sudo pacman -S zsh
```
---

## Poner zsh como shell predeterminado
```
chsh -s $(which zsh)
```
---

## Instalar git en ArchLinux solo en caso de que no lo tengas instalado
```
sudo pacman -S git
```
---

## Instalar el framework Oh My Zsh para poder personalizar el shell
```
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```
---

## Zsh plugins

```
cd ~

git clone https://github.com/zsh-users/zsh-completions ${ZSH_CUSTOM:-${ZSH:-~/.oh-my-zsh}/custom}/plugins/zsh-completions

git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions

git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting

git clone https://github.com/zdharma-continuum/fast-syntax-highlighting.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/plugins/fast-syntax-highlighting

git clone --depth 1 -- https://github.com/marlonrichert/zsh-autocomplete.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/plugins/zsh-autocomplete
```
---
## Abre el archivo de configuración de zsh

```
nano ~/.zshrc
```
`Pega lo siguiente`

```
plugins=(git zsh-autosuggestions zsh-syntax-highlighting fast-syntax-highlighting zsh-autocomplete)

fpath+=${ZSH_CUSTOM:-${ZSH:-~/.oh-my-zsh}/custom}/plugins/zsh-completions/src

```
---
## Guardas los cambios 
```
source ~/.zshrc
```
---
## DATE UN BREAK DE UN MINUTO Y ENSEGUIDA CONTINUAMOS CON LA INSTALACIÓN DE KITTY

## Instalar neofetch
```
sudo pacman -S neofetch
```
---
## Instalar kitty
```
sudo pacman -S kitty
```
---
## Instalar este paquete para que nos cargue las imagenes
```
sudo pacman -S imagemagick
```
---

## Editamos el archivo y agregamos la ruta de nuestra imagen y le podemos cambiar el tamano
```
nano ~/.config/neofetch/config.conf
```
### Sustityues ascii por kitty en esta variable

`image_backend="kitty"`

### Escribes la ruta de tu imagen en esta variable

`image_source="/ruta/de/tu/image/imagen.png"`

### Le cambias el size a tu imagen en esta variable

`image_sizee="300px"`

### Guardas los cambios presionando ctrl + o

`image_sizee="300px"`

---

## Abre el archivo de configuración de zsh

```
nano ~/.zshrc
```
`Pega esta function`

```
clear() {
  command clear
  neofetch
}
alias neofetch='neofetch'

```
---
## Guardas los cambios 
```
source ~/.zshrc
```
## FIN

