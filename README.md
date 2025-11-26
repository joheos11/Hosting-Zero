🚀 Arquitecturas de Despliegue 2025

Guía Visual de Alojamiento Gratuito para Desarrolladores

Contexto 2025: El "Gratis para siempre" ha evolucionado. Ya no se trata solo de subir archivos, sino de orquestar Cold Starts, límites de Edge Computing y arquitecturas distribuidas. Esta guía te ayuda a navegar el laberinto.

🧭 1. El Nuevo Paradigma (Post-Heroku)

El mercado se ha fragmentado. Para desplegar gratis hoy, necesitas entender estos cuatro conceptos clave:

|

| Concepto | Impacto en tu Proyecto |
| ❄️ Cold Start | Tu API puede tardar 30-60s en responder si nadie la usa. |
| 🌐 Edge Computing | Tu código corre cerca del usuario, pero con límites de CPU estrictos. |
| 📉 Scale-to-Zero | Si no hay tráfico, el servidor se apaga para ahorrar costes. |
| 👮 Uso Comercial | Muchas capas gratuitas prohíben ganar dinero con ellas. |

🎨 2. Frontend: El Reino del Jamstack

El alojamiento de sitios estáticos es la categoría más madura. Aquí tienes a los grandes jugadores:

🏆 Los 3 Grandes

▲ Vercel (El Estándar DX)

Ideal para: Next.js, React.

Lo bueno: 6,000 min de build, optimización de imágenes, Edge Network.

⚠️ La Trampa: Prohibido uso comercial en plan Hobby. Límite de funciones serverless (10s).

💠 Netlify (El Pionero)

Ideal para: Cualquier sitio estático, formularios.

Lo bueno: Permisivo con el uso comercial. Formularios y Auth integrados.

⚠️ La Trampa: Pocos minutos de build (300 min/mes).

☁️ Cloudflare Pages (La Bestia)

Ideal para: Alto tráfico, escalabilidad pura.

Lo bueno: Ancho de banda ILIMITADO. Infraestructura global propia.

⚠️ La Trampa: Lógica backend muy limitada (Workers con 10ms CPU).

📊 Comparativa Rápida Frontend

| Característica | Vercel (Hobby) | Netlify (Starter) | Cloudflare Pages |
| Bandwidth | 100 GB | 100 GB | ♾️ Ilimitado |
| Build Time | ⚡ 6,000 min | 🐢 300 min | 500 builds |
| Comercial | ❌ NO | ✅ SÍ | ✅ SÍ |

⚙️ 3. Backend (PaaS): Donde Vive la Lógica

Aquí es donde "gratis" suele significar "lento al arrancar".

🥊 Render vs. El Resto

🟣 Render (El Sucesor de Heroku)

Recursos: 512 MB RAM / 0.1 CPU.

La Realidad: Se duerme tras 15 min de inactividad.

Cold Start: 30s - 1 min de espera para el primer usuario.

Límite: 750 horas/mes (Da justo para un servicio 24/7).

🚂 Railway (El Modelo de Crédito)

Modelo: Crédito único de $5 USD (Trial).

Veredicto: 🛑 No es gratis para siempre. Genial para demos, malo para proyectos a largo plazo sin tarjeta.

🦅 Fly.io (Micro-VMs)

Tecnología: Firecracker micro-VMs.

Estado: Sin capa gratuita automática para cuentas nuevas. Requiere tarjeta.

Ventaja: Vuela... si consigues configurarlo.

🚀 Koyeb (La Innovación)

Ventaja: "Light Sleep". Escala a cero pero despierta en milisegundos (<200ms).

Recursos: 512 MB RAM / 0.1 vCPU.

Veredicto: Posiblemente la mejor experiencia PaaS gratuita actual.

🏗️ 4. Infraestructura (IaaS): Potencia Bruta

Para los valientes que saben configurar Linux.

👑 La Joya de la Corona: Oracle Cloud

🚨 Alerta de Mejor Valor: Ningún otro proveedor se acerca a esto.

Hardware: Instancias ARM Ampere A1.

RAM: ¡Hasta 24 GB de RAM gratis!

CPU: 4 OCPUs.

Disco: 200 GB.

El Problema: El registro es difícil (rechazan muchas tarjetas) y a veces no hay stock de servidores.

☁️ Los Otros Gigantes

GCP (e2-micro): 2 vCPUs, 1 GB RAM. Cuidado: Solo 1GB de tráfico de red al mes.

AWS (Free Tier): Solo 12 meses. No sirve para proyectos perpetuos.

💾 5. Bases de Datos: Persistencia

No pierdas tus datos. Elige sabiamente según tu inactividad.

| Proveedor | Tipo | Capacidad | 💤 Política de Sueño |
| Turso | SQLite | 9 GB 🏆 | Nunca (Serverless) |
| Supabase | Postgres | 500 MB | Pausa tras 7 días sin uso |
| Neon | Postgres | 0.5 GB | Escala a cero (Cold start) |
| MongoDB | NoSQL | 512 MB | Siempre activo (M0 Sandbox) |

🛠️ 6. Recetas de Arquitectura ("The Franken-stack")

Combina lo mejor de cada casa para crear la infraestructura perfecta.

🟢 Opción A: La App Web Moderna (SPA)

Para Portafolios, SaaS pequeños, Blogs.

Frontend: ☁️ Cloudflare Pages (SSL, CDN Global, Ilimitado).

Backend: 🚀 Koyeb (Docker container, despierta rápido).

Base de Datos: 🗄️ Turso (9GB espacio, rapidísima).

🟡 Opción B: El Bot 24/7

Para Bots de Discord, Telegram, Scrapers.

Infraestructura: 👑 Oracle Cloud (VM ARM).

Despliegue: Docker Compose en la propia VM.

Ventaja: Tienes 24GB de RAM para ti solo. Nada se duerme.

🔵 Opción C: Desarrollo Rápido

Para Hackathons, Prototipos.

Fullstack: ▲ Vercel (Next.js con API Routes).

Base de Datos: ⚡ Supabase (Auth + DB + Storage todo en uno).

Nota: Cuidado con los límites comerciales si el proyecto crece.

Conclusión: En 2025, el desarrollador inteligente no busca un solo proveedor "gratis para todo", sino que construye un puzzle arquitectónico conectando los mejores servicios especializados.
