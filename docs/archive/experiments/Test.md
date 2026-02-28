Perfecto. Aquí tienes una lista amplia y práctica para README de GitHub (incluye profile README).

1. Markdown (GFM)

Encabezados # a ######
Párrafos y saltos de línea
Negrita, cursiva, tachado
Citas >
Listas ordenadas y no ordenadas
Checklists - [ ] / - [x]
Enlaces inline y de referencia
Imágenes Markdown ![alt](url)
Código inline `code`
Bloques de código con triple backtick
Resaltado por lenguaje en code fences
Tablas Markdown
Regla horizontal ---
Autolinks (URLs directas)
Menciones y referencias (@user, #issue, owner/repo)


2. HTML embebido (permitido en gran parte)

a, img, p, br, hr
table, thead, tbody, tr, th, td
details, summary
kbd, samp, sub, sup
code, pre
ul, ol, li
h1..h6
blockquote
em, strong
span, div (con restricciones)
picture, source (útil para fallback de imágenes)
3. Formatos de imagen útiles en README

.png
.jpg
.jpeg
.gif (animado)
.svg
.webp
.ico (menos común)


4. Archivos que puedes enlazar

.pdf
.zip, .tar.gz
.docx, .pptx, .xlsx
Cualquier archivo del repo vía enlace relativo
Releases, assets y páginas externas


5. Componentes visuales muy usados

Badges (shields.io)
Stats cards por URL (GitHub stats, streak, etc.)
Activity graphs por URL
Typing SVG por URL
Imágenes clickeables (thumbnail -> link)
Secciones colapsables (details)


6. Código en bloques (lenguajes comunes)

bash, sh, zsh
js, ts, tsx
python
json, yaml, toml
html, css, scss
sql
go, rust, java, c, cpp, csharp
dockerfile
powershell
diff
plaintext


7. Elementos especiales de GitHub

Emoji Unicode
Emoji shortcode :rocket:
Referencias automáticas a PR/issues/commits
Footnotes (en GFM moderno)
Anchors de encabezados para navegación interna


8. Qué no funciona o está restringido

script JavaScript embebido
iframe (YouTube/otros embeds directos)
<video> funcional como player nativo en README
CSS avanzado o externo completo
HTML potencialmente inseguro (sanitizado por GitHub)


9. Recomendación para tu caso

Usa Markdown + tablas HTML para layout
Imágenes locales en ./assets/
GIF solo donde aporte
Widgets por URL como apoyo, no como base total
Mantén alturas y espaciados consistentes (como ya hicimos)



> [!NOTE]  
> Highlights information that users should take into account, even when skimming.

> [!TIP]
> Optional information to help a user be more successful.

> [!IMPORTANT]  
> Crucial information necessary for users to succeed.

> [!WARNING]  
> Critical content demanding immediate user attention due to potential risks.

> [!CAUTION]
> Negative potential consequences of an action.