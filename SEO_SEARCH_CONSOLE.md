# Google Search Console — nataciontrujillo.pe

## 1. Crear la propiedad correcta

1. Entra a https://search.google.com/search-console con la cuenta de Google que administrará el sitio.
2. Pulsa **Añadir propiedad**.
3. Elige **Dominio** e introduce exactamente `nataciontrujillo.pe` (sin `https://`, sin `www` y sin `/`).
4. Copia el registro TXT que entrega Google. Tendrá esta forma:

   `google-site-verification=CODIGO_UNICO_DE_GOOGLE`

## 2. Verificar desde Vercel DNS

1. En Vercel abre **Domains → nataciontrujillo.pe → DNS Records**.
2. Añade un registro **TXT**.
3. Usa `@` como nombre/host y pega como valor el código completo entregado por Google.
4. Guarda el registro, vuelve a Search Console y pulsa **Verificar**.
5. Conserva el TXT después de verificarlo: Google puede comprobarlo nuevamente.

La propiedad de dominio es preferible porque reúne `http`, `https`, el dominio raíz y cualquier subdominio como `www`.

## 3. Enviar el sitemap e indexar

1. En Search Console abre **Sitemaps**.
2. Envía `https://nataciontrujillo.pe/sitemap.xml`.
3. Abre **Inspección de URLs**, consulta `https://nataciontrujillo.pe/` y pulsa **Solicitar indexación**.
4. Revisa en los días siguientes **Indexación → Páginas**, **Rendimiento** y **Mejoras**.

## 4. SEO local

Crea o reclama también el Perfil de Empresa de Google de AXT Trujillo. Mantén exactamente el mismo nombre, teléfono, dirección, horario, web e Instagram que aparecen en el sitio.

## Comprobaciones después de cada despliegue

- La URL principal responde sin errores y redirige `www` hacia `https://nataciontrujillo.pe/`.
- `https://nataciontrujillo.pe/robots.txt` es accesible.
- `https://nataciontrujillo.pe/sitemap.xml` es accesible.
- Los datos estructurados pasan la prueba de resultados enriquecidos de Google.
- Los cambios de precios, horarios o preguntas frecuentes se actualizan también en el JSON-LD de `web/index.html`.
