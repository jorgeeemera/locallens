# LocalLens (beta)

Búsqueda privada en tus documentos (PDF, Word, notas) para Mac: por palabras exactas y por significado, sin conexión. La app no tiene permiso de red y solo lee las carpetas que eliges.

Web: https://jorgeeemera.github.io/locallens/

## Instalar

Requisitos: Mac con Apple silicon y macOS 14 o posterior.

```sh
brew install --cask jorgeeemera/tap/locallens
```

O descarga `LocalLens-0.2.1-arm64.zip` de [Releases](https://github.com/jorgeeemera/locallens/releases/latest) y arrastra la app a Aplicaciones.

### ⚠️ macOS pedirá autorización la primera vez

Esta beta **no está notarizada por Apple** (firma ad hoc). La primera vez que la abras, macOS avisará de que no puede verificarla y no la abrirá. Para permitirla:

1. Ajustes del Sistema › Privacidad y seguridad.
2. Baja hasta el aviso de LocalLens y pulsa **Abrir igualmente**.

Solo hace falta una vez. Gatekeeper y el App Sandbox siguen activos: no desactives Gatekeeper.

### Búsqueda por significado

Viene incluida: el modelo se prepara solo la primera vez que abres la app, sin descargar nada. La app nunca usa la red.

Comprueba la descarga con `SHA256SUMS.txt` de la release:

```sh
shasum -a 256 -c SHA256SUMS.txt
```

## Qué esperar

- Formatos: PDF (también escaneados, con OCR local), Word (.docx, .doc), RTF, .odt, .txt y Markdown.
- Interfaz en español e inglés.
- macOS 14 y 15 aún no probados a fondo; no hay versión para Intel.
- Desinstalar: `brew uninstall --cask locallens`. El índice no se borra; puedes borrarlo antes desde Ajustes.

## Licencias de terceros

Modelo [intfloat/multilingual-e5-small](https://huggingface.co/intfloat/multilingual-e5-small) (rev. `614241f6`), licencia MIT; incluido en la app; el texto de la licencia está en `LocalLens.app/Contents/Resources/multilingual-e5-small.locallens-model/LICENSE.txt`.
