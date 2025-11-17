# Logi Actions Ring Plugin

Plugin per Logitech Actions Ring creat amb el Logi Actions SDK.

## Requisits

- .NET 8 SDK
- Logitech Options+ o Loupedeck software instal·lat
- LogiPluginTool instal·lat globalment

## Instal·lació

1. Instal·la .NET 8 SDK:
   ```bash
   brew install dotnet@8
   ```

2. Instal·la LogiPluginTool:
   ```bash
   dotnet tool install --global LogiPluginTool
   ```

3. Configura les variables d'entorn (afegir al `~/.zshrc`):
   ```bash
   export DOTNET_ROOT="/opt/homebrew/opt/dotnet@8/libexec"
   export PATH="/opt/homebrew/opt/dotnet@8/bin:$PATH"
   export PATH="$PATH:$HOME/.dotnet/tools"
   ```

## Desenvolupament

### Compilar el projecte

```bash
cd LogiActionsRingPlugin
dotnet build
```

### Hot Reload

Per activar el hot reload i reconstruir automàticament quan es guarden canvis:

```bash
cd LogiActionsRingPlugin/src
dotnet watch build
```

### Estructura del projecte

- `src/LogiActionsRingPlugin.cs` - Classe principal del plugin
- `src/Actions/` - Accions del plugin (comandes i ajustaments)
- `src/Helpers/` - Classes auxiliars
- `src/package/metadata/` - Metadades i recursos del plugin

## Testing

Després de compilar, el plugin es carrega automàticament al Logi Plugin Service. Per verificar:

1. Obre Logitech Options+ o Loupedeck software
2. A Logitech Options+, ves a 'All Actions' i verifica que 'LogiActionsRingPlugin' apareix a la secció 'Installed Plugins'
3. Si no apareix, ves a la configuració d'Options+ i selecciona 'Restart Logi Plugin Service'

## Recursos

- [Documentació Logi Actions SDK](https://logitech.github.io/actions-sdk-docs/)
- [Getting Started Guide](https://logitech.github.io/actions-sdk-docs/csharp/Getting-started/)

