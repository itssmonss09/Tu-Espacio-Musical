
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tu espacio Musical</title>

    <style>
        :root {
            --bg-dark: #121214;
            --bg-card: #1e1e22;
            --bg-card-hover: #2a2a30;
            --accent-mint: #a7f3d0;
            --accent-lavender: #ddd6fe;
            --accent-pink: #fbcfe8;
            --text-main: #f4f4f5;
            --text-muted: #a1a1aa;
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        body {
            background-color: var(--bg-dark);
            color: var(--text-main);
            font-family: system-ui, -apple-system, sans-serif;
            min-height: 100vh;
        }

        .spotify-nav {
            background-color: rgba(18, 18, 20, 0.95);
            position: sticky;
            top: 0;
            z-index: 1000;
            border-bottom: 1px solid rgba(255, 255, 255, 0.08);
            padding: 1rem 2rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .brand-logo {
            color: var(--accent-mint);
            font-size: 1.4rem;
            font-weight: 700;
            text-decoration: none;
        }

        .nav-menu {
            display: flex;
            list-style: none;
            gap: 1.5rem;
        }

        .nav-link {
            color: var(--text-muted);
            text-decoration: none;
            font-weight: 500;
            font-size: 0.95rem;
            padding: 8px 16px;
            border-radius: 20px;
            transition: all 0.25s ease;
        }

        .nav-link:hover,
        .nav-link.active {
            color: #09090b;
            background-color: var(--accent-mint);
        }

        .hero-header {
            background: linear-gradient(180deg, #1e1e22 0%, var(--bg-dark) 100%);
            padding: 3rem 1.5rem;
            text-align: center;
            border-bottom: 1px solid rgba(255, 255, 255, 0.05);
        }

        .hero-header h1 {
            color: var(--accent-mint);
            font-size: 2.5rem;
            margin-bottom: 0.5rem;
        }

        .hero-header p {
            color: var(--text-muted);
            font-size: 1.1rem;
        }

        .main-container {
            max-width: 1200px;
            margin: 2rem auto;
            padding: 0 1.5rem;
        }

        .section-title {
            color: var(--accent-lavender);
            font-size: 1.8rem;
            margin-bottom: 1.5rem;
            border-left: 4px solid var(--accent-mint);
            padding-left: 12px;
        }

        .song-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(320px, 1fr));
            gap: 1.5rem;
            margin-bottom: 3rem;
        }

        .song-card {
            background-color: var(--bg-card);
            border: 1px solid rgba(255, 255, 255, 0.05);
            border-radius: 16px;
            padding: 1.2rem;
            transition: transform 0.3s ease;
            display: flex;
            flex-direction: column;
            justify-content: space-between;
        }

        .song-card:hover {
            transform: translateY(-5px);
            background-color: var(--bg-card-hover);
        }

        .artist-img {
            width: 100%;
            height: 240px;
            object-fit: cover;
            border-radius: 12px;
            margin-bottom: 12px;
        }

        .song-title {
            color: var(--accent-mint);
            font-size: 1.2rem;
            font-weight: 600;
            margin-bottom: 4px;
        }

        .artist-name {
            color: var(--accent-lavender);
            font-size: 0.95rem;
            margin-bottom: 12px;
        }

        .genero-musical,
        .music-genre {
            color: var(--accent-lavender);
            font-size: 0.95rem;
            margin-bottom: 12px;
        }

        .spotify-embed {
            border-radius: 12px;
            width: 100%;
            height: 152px;
            border: none;
            margin-top: auto;
        }

        .page-section {
            scroll-margin-top: 75px;
        }

        #contacto input,
        #contacto textarea {
            width: 100%;
            padding: 10px;
            background: var(--bg-dark);
            border: 1px solid rgba(255,255,255,0.1);
            color: #fff;
            border-radius: 8px;
            font-family: inherit;
        }

        #contacto textarea {
            resize: vertical;
        }

        @media (max-width: 650px) {
            .spotify-nav {
                flex-direction: column;
                gap: 1rem;
                padding: 1rem;
            }

            .nav-menu {
                flex-wrap: wrap;
                justify-content: center;
                gap: 0.5rem;
            }

            .nav-link {
                font-size: 0.85rem;
                padding: 7px 10px;
            }

            .hero-header h1 {
                font-size: 2rem;
            }

            .song-grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>

<body>

    <nav class="spotify-nav">
        <a href="#inicio" class="brand-logo">Tu espacio Musical</a>
        <ul class="nav-menu">
            <li><a href="#inicio" class="nav-link active">Inicio</a></li>
            <li><a href="#artistas" class="nav-link">Artistas</a></li>
            <li><a href="#canciones" class="nav-link">Top Canciones</a></li>
            <li><a href="#contacto" class="nav-link">Contacto</a></li>
        </ul>
    </nav>

    <section id="inicio" class="page-section">

        <header class="hero-header">
            <h1>Tu espacio Musical</h1>
            <p>Explora a tus artistas destacados y escucha sus mejores temas directamente en esta página.</p>
        </header>

        <main class="main-container">

            <h2 class="section-title">Navega por el Sitio</h2>

            <div class="song-grid">

                <div class="song-card">
                    <div>
                        <div class="song-title">Artistas Destacados</div>
                        <div class="artist-name">Humbe, Alfredo Olivas, Calibre 50, Maluma, Los Titanes de Durango, Fuerza Regida y Jorge Cuellar.</div>
                    </div>
                    <a href="#artistas" class="nav-link" style="display:inline-block; margin-top:10px; background-color: var(--accent-mint); color:#000;">Ver Galería</a>
                </div>

                <div class="song-card">
                    <div>
                        <div class="song-title">Top Canciones</div>
                        <div class="artist-name">Escucha los mejores temas reproducibles en tiempo real.</div>
                    </div>
                    <a href="#canciones" class="nav-link" style="display:inline-block; margin-top:10px; background-color: var(--accent-lavender); color:#000;">Escuchar Ahora</a>
                </div>

                <div class="song-card">
                    <div>
                        <div class="song-title">Formulario de Contacto</div>
                        <div class="artist-name">Envía sugerencias de canciones o conéctate en redes sociales.</div>
                    </div>
                    <a href="#contacto" class="nav-link" style="display:inline-block; margin-top:10px; background-color: var(--accent-pink); color:#000;">Ir a Contacto</a>
                </div>

            </div>

            <h2 class="section-title">Canciones Destacadas</h2>

            <div class="song-grid">

                <div class="song-card">
                    <div class="song-title">Fantasmas</div>
                    <div class="artist-name">Humbe</div>
                    <iframe class="spotify-embed" src="https://open.spotify.com/embed/track/5rcnAHBclBs0OGV4rATEnR?utm_source=generator" allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture" loading="lazy"></iframe>
                </div>

                <div class="song-card">
                    <div class="song-title">Prestame un Beso</div>
                    <div class="artist-name">Jorge Cuellar</div>
                    <iframe class="spotify-embed" src="https://open.spotify.com/embed/track/7nDMD0rdJ0HutfgFzqkMWh?utm_source=generator" allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture" loading="lazy"></iframe>
                </div>

                <div class="song-card">
                    <div class="song-title">Doncellas 10/10</div>
                    <div class="artist-name">Chuyin</div>
                    <iframe class="spotify-embed" src="https://open.spotify.com/embed/track/1fuLuf6SKVdxlqxFnEN4PI?utm_source=generator" allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture" loading="lazy"></iframe>
                </div>

            </div>

        </main>
    </section>

    <section id="artistas" class="page-section">

        <header class="hero-header">
            <h1>Artistas Favorito</h1>
            <p>Aquí se reúnen las canciones más escuchadas de tus artistas favoritos: desde el corrido que retumba hasta el beat urbano que no te sacas de la cabeza.</p>
        </header>

        <main class="main-container">

            <div class="song-grid">

                <div class="song-card">
                    <img src="https://i.pinimg.com/736x/51/d5/2f/51d52f66291e590a4ab77fa0a0b833af.jpg" alt="Humbe" class="artist-img">
                    <div class="artist-name">Humbe</div>
                    <div class="music-genre">Pop Alternativo / Latin Pop</div>
                    <iframe class="spotify-embed" src="https://open.spotify.com/embed/track/5rcnAHBclBs0OGV4rATEnR?utm_source=generator" allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture" loading="lazy"></iframe>
                </div>

                <div class="song-card">
                    <img src="https://i.pinimg.com/736x/4c/c7/97/4cc797a84dba8d8e69c0065c6a3bb3f0.jpg" alt="Calibre 50" class="artist-img">
                    <div class="artist-name">Calibre 50</div>
                    <div class="music-genre">Norteño-Banda</div>
                    <iframe class="spotify-embed" src="https://open.spotify.com/embed/track/4a50ELsSeCF8HDDwSn51wK?utm_source=generator" allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture" loading="lazy"></iframe>
                </div>

                <div class="song-card">
                    <img src="https://i.pinimg.com/1200x/81/4a/a8/814aa86fff311477f26c89b75066f0bc.jpg" alt="Maluma" class="artist-img">
                    <div class="artist-name">Maluma</div>
                    <div class="music-genre">Reggaeton / Pop Urbano</div>
                    <iframe class="spotify-embed" src="https://open.spotify.com/embed/track/1iEwyiSLAunPR6uouANE0O?utm_source=generator" allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture" loading="lazy"></iframe>
                </div>

                <div class="song-card">
                    <img src="https://i.pinimg.com/736x/07/17/70/071770fb42af5676f548db7045f9fb53.jpg" alt="Alfredo Olivas" class="artist-img">
                    <div class="artist-name">Alfredo Olivas</div>
                    <div class="music-genre">Regional Mexicano / Norteño</div>
                    <iframe class="spotify-embed" src="https://open.spotify.com/embed/track/5tpoc6yo7yjxQEnAOPbs0B?utm_source=generator" allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture" loading="lazy"></iframe>
                </div>

                <div class="song-card">
                    <img src="https://i.pinimg.com/736x/d4/91/73/d491738c20e84246454f57d8df1ad1ae.jpg" alt="Fuerza Regida" class="artist-img">
                    <div class="artist-name">Fuerza Regida</div>
                    <div class="music-genre">Corridos Tumbados / Regional Urbano</div>
                    <iframe class="spotify-embed" src="https://open.spotify.com/embed/track/2VmeNiaRsq0Z2gcMcQvHb8?utm_source=generator" allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture" loading="lazy"></iframe>
                </div>

                <div class="song-card">
                    <img src="https://i.pinimg.com/736x/d1/ed/3e/d1ed3e1144bed22959b4d4f1908dd6f3.jpg" alt="Los Titanes de Durango" class="artist-img">
                    <div class="artist-name">Los Titanes de Durango</div>
                    <div class="music-genre">Norteño / Banda</div>
                    <iframe class="spotify-embed" src="https://open.spotify.com/embed/track/2w9v5V5Dpj4Cy7MWEP6Et9?utm_source=generator&amp;t=12" allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture" loading="lazy"></iframe>
                </div>

            </div>

        </main>
    </section>

    <section id="canciones" class="page-section">

        <header class="hero-header">
            <h1>Top Canciones Favoritas</h1>
            <p>Haz clic en el botón de reproducción para escuchar directamente en este sitio :).</p>
        </header>

        <main class="main-container">

            <h2 class="section-title">Humbe</h2>
            <div class="song-grid">

                <div class="song-card">
                    <div class="song-title">El Poeta</div>
                    <div class="artist-name">Humbe</div>
                    <iframe class="spotify-embed" src="https://open.spotify.com/embed/track/2fIPEgY8CJ4hh5UDZa2lB9?utm_source=generator" allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture" loading="lazy"></iframe>
                </div>

                <div class="song-card">
                    <div class="song-title">Dieznoches</div>
                    <div class="artist-name">Humbe</div>
                    <iframe class="spotify-embed" src="https://open.spotify.com/embed/track/3Z69GuyA1GwA14ccCXTV25?utm_source=generator" allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture" loading="lazy"></iframe>
                </div>

                <div class="song-card">
                    <div class="song-title">Amor de Cine</div>
                    <div class="artist-name">Humbe</div>
                    <iframe class="spotify-embed" src="https://open.spotify.com/embed/track/0v9UztY5A12cJUsWD7PZzS?utm_source=generator" allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture" loading="lazy"></iframe>
                </div>

            </div>

            <h2 class="section-title">Alfredo Olivas</h2>
            <div class="song-grid">

                <div class="song-card">
                    <div class="song-title">El Sillon</div>
                    <div class="artist-name">Alfredo Olivas</div>
                    <iframe class="spotify-embed" src="https://open.spotify.com/embed/track/4SHTLje9c6RLnx6kOPt9L6?utm_source=generator" allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture" loading="lazy"></iframe>
                </div>

                <div class="song-card">
                    <div class="song-title">Mayday</div>
                    <div class="artist-name">Alfredo Olivas</div>
                    <iframe class="spotify-embed" src="https://open.spotify.com/embed/track/5tpoc6yo7yjxQEnAOPbs0B?utm_source=generator" allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture" loading="lazy"></iframe>
                </div>

                <div class="song-card">
                    <div class="song-title">La Danza Del Venado</div>
                    <div class="artist-name">Alfredo Olivas</div>
                    <iframe class="spotify-embed" src="https://open.spotify.com/embed/track/468U6z141Dy1dVPikBwKfY?utm_source=generator" allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture" loading="lazy"></iframe>
                </div>

            </div>

            <h2 class="section-title">Fuerza Regida</h2>
            <div class="song-grid">

                <div class="song-card">
                    <div class="song-title">TQM</div>
                    <div class="artist-name">Fuerza Regida</div>
                    <iframe class="spotify-embed" src="https://open.spotify.com/embed/track/368eeEO3Y2uZUQ6S5oIjcu?utm_source=generator" allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture" loading="lazy"></iframe>
                </div>

                <div class="song-card">
                    <div class="song-title">Modo Maldito</div>
                    <div class="artist-name">Fuerza Regida</div>
                    <iframe class="spotify-embed" src="https://open.spotify.com/embed/track/2VmeNiaRsq0Z2gcMcQvHb8?utm_source=generator" allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture" loading="lazy"></iframe>
                </div>

                <div class="song-card">
                    <div class="song-title">Ansiedad</div>
                    <div class="artist-name">Fuerza Regida</div>
                    <iframe class="spotify-embed" src="https://open.spotify.com/embed/track/1a7onn7lPqqRWul5ogyMyX?utm_source=generator" allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture" loading="lazy"></iframe>
                </div>

            </div>

            <h2 class="section-title">Calibre 50</h2>
            <div class="song-grid">

                <div class="song-card">
                    <div class="song-title">El Niño Sicario</div>
                    <div class="artist-name">Calibre 50</div>
                    <iframe class="spotify-embed" src="https://open.spotify.com/embed/track/1sVNgN59IWB81LiT1Agz9e?utm_source=generator" allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture" loading="lazy"></iframe>
                </div>

                <div class="song-card">
                    <div class="song-title">Que Tiene De Malo</div>
                    <div class="artist-name">Calibre 50</div>
                    <iframe class="spotify-embed" src="https://open.spotify.com/embed/track/4VZ0UOLwnTnQSLZJme5lyQ?utm_source=generator" allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture" loading="lazy"></iframe>
                </div>

                <div class="song-card">
                    <div class="song-title">Te Estoy Engañando Con Otra</div>
                    <div class="artist-name">Calibre 50</div>
                    <iframe class="spotify-embed" src="https://open.spotify.com/embed/track/0Q2nlEy3j08AWwrum9BFmH?utm_source=generator" allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture" loading="lazy"></iframe>
                </div>

            </div>

            <h2 class="section-title">Chuyin</h2>
            <div class="song-grid">

                <div class="song-card">
                    <div class="song-title">Olvidate De Mi</div>
                    <div class="artist-name">Chuyin</div>
                    <iframe class="spotify-embed" src="https://open.spotify.com/embed/track/3obfgAGgAhrQ5IPNFbOgaN?utm_source=generator" allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture" loading="lazy"></iframe>
                </div>

                <div class="song-card">
                    <div class="song-title">Rehabilitado</div>
                    <div class="artist-name">Chuyin</div>
                    <iframe class="spotify-embed" src="https://open.spotify.com/embed/track/0yIeD98W17kQa4FdZzieiE?utm_source=generator" allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture" loading="lazy"></iframe>
                </div>

                <div class="song-card">
                    <div class="song-title">No es mi culpa</div>
                    <div class="artist-name">Chuyin</div>
                    <iframe class="spotify-embed" src="https://open.spotify.com/embed/track/3r5QtYeOFgZW9HU44PY5tB?utm_source=generator" allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture" loading="lazy"></iframe>
                </div>

            </div>

            <h2 class="section-title">La Arrolladora Banda El Limon</h2>
            <div class="song-grid">

                <div class="song-card">
                    <div class="song-title">Cabecita Dura</div>
                    <div class="artist-name">La Arrolladora Banda El Limon</div>
                    <iframe class="spotify-embed" src="https://open.spotify.com/embed/track/1y8vhYug05asslmpY8bFel?utm_source=generator" allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture" loading="lazy"></iframe>
                </div>

                <div class="song-card">
                    <div class="song-title">Ya te perdi la fe</div>
                    <div class="artist-name">La Arrolladora Banda El Limon</div>
                    <iframe class="spotify-embed" src="https://open.spotify.com/embed/track/0KHDthR0XvPoeJaqBc7Sg5?utm_source=generator" allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture" loading="lazy"></iframe>
                </div>

                <div class="song-card">
                    <div class="song-title">Mi segunda vida</div>
                    <div class="artist-name">La Arrolladora Banda El Limon</div>
                    <iframe class="spotify-embed" src="https://open.spotify.com/embed/track/6Z7f0BXDLI8k4CHR9KJdAD?utm_source=generator" allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture" loading="lazy"></iframe>
                </div>

            </div>

        </main>
    </section>

    <section id="contacto" class="page-section">

        <header class="hero-header">
            <h1>Contacto y Sugerencias</h1>
            <p>Escríbenos tu sugerencia de canción o artista favorito.</p>
        </header>

        <main class="main-container">

            <div class="song-grid">

                <div class="song-card">

                    <h2 class="song-title" style="margin-bottom: 1rem;">Envíanos un Mensaje</h2>

                    <form>
                        <div style="margin-bottom: 1rem;">
                            <label style="display: block; color: var(--text-muted); margin-bottom: 0.3rem;">Nombre Completo</label>
                            <input type="text" placeholder="Tu nombre">
                        </div>

                        <div style="margin-bottom: 1rem;">
                            <label style="display: block; color: var(--text-muted); margin-bottom: 0.3rem;">Correo Electrónico</label>
                            <input type="email" placeholder="correo@gmail.com">
                        </div>

                        <div style="margin-bottom: 1rem;">
                            <label style="display: block; color: var(--text-muted); margin-bottom: 0.3rem;">Mensaje</label>
                            <textarea rows="4" placeholder="Escribe tu sugerencia de canción..."></textarea>
                        </div>

                        <button type="button" class="nav-link" style="width: 100%; background: var(--accent-mint); color: #000; border: none; padding: 12px; font-weight: bold; cursor: pointer;">Enviar</button>
                    </form>

                </div>

                <div style="display: flex; flex-direction: column; gap: 1.5rem;">

                    <div class="song-card">
                        <div class="song-title">Correo Oficial</div>
                        <div class="artist-name" style="margin-top: 0.5rem;">TuEspacioMusical@gmail.com</div>
                    </div>

                    <div class="song-card" style="text-align: center; padding: 1.5rem;">

                        <img src="https://i.pinimg.com/736x/e7/ed/63/e7ed632c6e9c2bc5b7d6751f69f5c3d0.jpg" alt="Perfil de Spotify" class="artist-img" style="width: 110px; height: 110px; border-radius: 50%; object-fit: cover; margin: 0 auto 1rem auto; border: 2px solid var(--accent-mint);">

                        <div class="song-title">Perfil de Spotify</div>

                        <div class="artist-name" style="margin-top: 0.25rem; font-size: 0.95rem; color: var(--accent-lavender);">
                            @Tu Espacio Musical :)
                        </div>

                        <p style="margin: 0.8rem 0 1.2rem 0; font-size: 0.85rem; color: #b3b3b3;">
                            Sigue nuestras listas de reproducción oficiales y descubre lo que escuchamos en vivo.
                        </p>

                        <a href="https://open.spotify.com/user/31jer5ayi5p2fqxzxzsyywhl5ciq" target="_blank" rel="noopener noreferrer" class="nav-link" style="display: inline-block; background-color: var(--accent-mint); color: #000; font-weight: bold; padding: 10px 22px; border-radius: 25px; text-decoration: none; transition: transform 0.2s ease;">
                            ▶ Seguir en Spotify
                        </a>

                    </div>

                </div>

            </div>

        </main>
    </section>

    <script>
        const navLinks = document.querySelectorAll('.spotify-nav .nav-link');

        navLinks.forEach(link => {
            link.addEventListener('click', () => {
                navLinks.forEach(item => item.classList.remove('active'));
                link.classList.add('active');
            });
        });
    </script>

</body>
</html>
