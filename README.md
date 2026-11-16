# StreamMate · Vikbeing
Sitio estático (HTML/CSS/JS). Sin Supabase configurado funciona en modo demo con localStorage.

## Supabase
1. Crea un proyecto y ejecuta `schema.sql` en el SQL Editor.
2. Authentication → Providers → Twitch: pega Client ID y Secret de tu app en dev.twitch.tv. Añade como Redirect URI la que muestra Supabase.
3. Authentication → URL Configuration: pon la URL de tu GitHub Pages (`https://USUARIO.github.io/REPO/`).
4. En `index.html` rellena `SUPABASE_URL` y `SUPABASE_ANON_KEY` (la clave **anon** es pública; la seguridad la dan las políticas RLS). Nunca subas la `service_role` ni el Client Secret de Twitch.

## GitHub Pages
Sube los archivos → Settings → Pages → rama `main`, carpeta `/ (root)`.

## Pendiente (necesita backend)
Moderar chat, cambiar título/categoría y Spotify reales requieren tokens de API: usa Supabase Edge Functions para guardarlos y llamarlas. Hoy esas acciones son demo y la app lo indica.
