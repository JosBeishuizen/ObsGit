# Desktop integratie AppImage
Create a .desktop file that points to the application -- here is an example of a .desktop for minecraft:

```
[Desktop Entry]
Type=Application
Name=Minecraft
Comment=Minecraft
Icon=/home/bram/Applications/Minecraft/icon.png
Exec=/home/bram/Applications/Minecraft/minecraft
Terminal=false
Categories=Minecraft;game
```

Put that file in ~/.local/share/applications