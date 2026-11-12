# LocalLens (beta)

Búsqueda privada en tus documentos para Mac: por palabras exactas y por significado, sin conexión. La app no tiene permiso de red y solo lee las carpetas que eliges.

Web: https://jorgeeemera.github.io/locallens/

## Instalar

Requisitos: Mac con Apple silicon y macOS 14 o posterior.

```sh
brew install --cask jorgeeemera/tap/locallens
```

O descarga `LocalLens-0.1.0-arm64.zip` de [Releases](https://github.com/jorgeeemera/locallens/releases/latest) y arrastra la app a Aplicaciones.

### ⚠️ macOS pedirá autorización la primera vez

Esta beta **no está notarizada por Apple** (firma ad hoc). La primera vez que la abras, macOS avisará de que no puede verificarla y no la abrirá. Para permitirla:

1. Ajustes del Sistema › Privacidad y seguridad.
2. Baja hasta el aviso de LocalLens y pulsa **Abrir igualmente**.

Solo hace falta una vez. Gatekeeper y el App Sandbox siguen activos: no desactives Gatekeeper.

### Búsqueda por significado

El modelo va aparte: descarga `LocalLens-model-multilingual-e5-small.zip` de la misma release, descomprímelo y en LocalLens elige **Ajustes › Importar paquete de modelo…**. Sin el modelo, la búsqueda por palabras funciona igual. La app nunca descarga nada por sí misma.

Comprueba las descargas con `SHA256SUMS.txt` de la release:

```sh
shasum -a 256 -c SHA256SUMS.txt
```

## Qué esperar

- Formatos: PDF, .txt y Markdown.
- Interfaz en español e inglés.
- macOS 14 y 15 aún no probados a fondo; no hay versión para Intel.
- Desinstalar: `brew uninstall --cask locallens`. El índice no se borra; puedes borrarlo antes desde Ajustes.

## Licencias de terceros

Modelo [intfloat/multilingual-e5-small](https://huggingface.co/intfloat/multilingual-e5-small) (rev. `614241f6`), licencia MIT; el texto de la licencia va dentro del paquete del modelo (`LICENSE.txt`).
