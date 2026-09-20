# Eréndira & Enrique — Invitación virtual

## Producción
- Vercel project: `erendira-enrique-boda`
- Public URL: `https://erendira-enrique-boda-two.vercel.app`
- Vercel Root Directory: `wedding-site`
- Framework preset: Other / static HTML

## Rutas
- `/` — invitación pública
- `/novios` — galería privada de los novios
- `/album.html` — respaldo de la misma galería privada

## Fotos de invitados
Supabase project: `E&E Wedding` (`sznsbwizgjtetjnkgfzv`)

- Private Storage bucket: `wedding-photos`
- Guest upload Edge Function: `guest-photo-upload`
- Private gallery Edge Function: `wedding-album-admin`
- Upload metadata table: `photo_uploads`
- Allowed couple accounts table: `couple_admins`

The public invitation can upload photos but does not expose a Storage listing.
The private gallery requests time-limited signed URLs from the admin Edge Function.

## Deployment
The Vercel project should be connected to this GitHub repository:
`EnrikeDev/AmigosSectreto`

Use:
- Production branch: `main`
- Root Directory: `wedding-site`

Do not create a new Vercel project; deploying this folder from the existing
`erendira-enrique-boda` project keeps the public URL unchanged.
