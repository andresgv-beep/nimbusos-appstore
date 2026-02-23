# NimbusOS App Store

Catálogo oficial de aplicaciones para NimbusOS.

## Estructura

```
├── catalog.yaml    # Definiciones de apps
└── icons/          # Iconos SVG
    ├── jellyfin.svg
    ├── plex.svg
    └── ...
```

## Uso

NimbusOS descarga automáticamente el catálogo desde:
```
https://raw.githubusercontent.com/andresgv-beep/nimbusos-appstore/main/catalog.yaml
```

## Añadir una app

1. Añade la definición en `catalog.yaml`
2. Añade el icono SVG en `icons/`
3. Haz PR

## Formato de app

```yaml
mi-app:
  name: Mi App
  description: Descripción de la app
  icon: https://raw.githubusercontent.com/andresgv-beep/nimbusos-appstore/main/icons/mi-app.svg
  category: media|cloud|downloads|homelab|development|security|monitoring
  port: 8080
  image: usuario/imagen:latest
  official: true
  volumes:
    config: /config
  env:
    VARIABLE: "valor"
```

## Categorías

- `media` - Multimedia (Jellyfin, Plex, etc.)
- `cloud` - Cloud & Sync (Nextcloud, Syncthing, etc.)
- `downloads` - Descargas (Transmission, Sonarr, etc.)
- `homelab` - Home Lab (Home Assistant, Pi-hole, etc.)
- `development` - Desarrollo (Gitea, VS Code, etc.)
- `security` - Seguridad (Vaultwarden, etc.)
- `monitoring` - Monitorización (Grafana, Prometheus, etc.)
