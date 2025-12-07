# Página del festival
    https://maiteflm18.github.io/Festival_Urban_Fest_MaiteLoyarte/index.html
    
# <<< PROYECTO EVENTO MUSICAL - Nafarroa Urban Fest >>>

En este proyecto se realiza una página web para un festival musical, implementando **Bootstrap 4 compilado desde SASS**, con variables personalizadas, mapas de colores, tipografías locales y animaciones CSS3. No se utiliza el archivo CSS del CDN, siguiendo los requisitos del enunciado.

Toda la personalización se ha realizado mediante variables SASS, overrides, imports personalizados y archivos de estilos propios.

# 1- He personalizado mis propias globales dentro de :root para controlar los estilos del tema en el documento _custom-variables.scss

    - Colores generales del tema.
    - Colores de botones, enlaces y secciones.
    - Tipografías locales importadas (Bebas Neue y Raleway).
    - Tamaños de texto base.

    ```scss
        :root {
            --tamano-Fuente: 13px;
            --color-fondo: #0D0D0D;
            --color-fondo-seccion: #212038;
            --color-artistas: #7c2c60;
            --color-texto: #fff;
            --color-destacado: #ffc62e;
            --color-links: #F9833A;
            --color-btn: #E45C54;
            --color-btn2: #972A24;
            --estilo-fuente1: "BebasNeue", sans-serif;
            --estilo-fuente2: "Raleway", sans-serif;
        }
    ```
# 2- Se ha personalizado el HTML con Bootstrap mediante SASS, se importaron en el documento _custom-styles.scss

    ```scss
    @import "./node_modules/bootstrap/scss/bootstrap";
    @import "/SCSS/custom-variables";
    @import "../CSS/estilos.css";
    @import "/SCSS/custom-fonts";
    @import "~@fortawesome/fontawesome-free/css/all.css";
    @import "~bootstrap-icons/font/bootstrap-icons.css";
    ```
    Desde el archivo _custom-variables.scss se han sobreescrito los distintos estilos de Bootstrap.

# 3- Utilicé animaciones de CSS3 para las secciones de artistas, horario y sponsors.
    ```scss

        - Fondo de estrellas
        @keyframes estrellas {
        0% { background-position: 0 0; }
        100% { background-position: 800px 600px; }
        }

        - Fondo de fuegos artificiales
        @keyframes fuegosAnimados {
            0% { opacity: 0; transform: scale(0.8); }
            20% { opacity: .2; transform: scale(1.1); }
            100% { opacity: 0; transform: scale(1.3); }
        }
    ```
# 4- Personalicé varios componentes de Bootstrap:
    - Navbar
        Colores y efectos hover personalizados
        Uso de fuentes personalizadas
        Resalte del link activo

    - Botón de entradas
        Estilo 100% propio con sombras y stroke animado

    - Tablas, grid y tipografías
        Adaptación al sistema grid de Bootstrap 4
        Ajustes responsive manuales

    - Carrusel de sponsors
        No es un carrusel genérico
        Se añadió animación + hover scale + fondo animado

En este proyecto se han realizado modificaciones profundas tanto en Bootstrap como en los estilos personalizados, utilizando variables SASS, mapas, tipografías locales, animaciones y personalización de componentes.

El resultado es un sitio completamente adaptado a la identidad visual del festival Nafarroa Urban Fest, cumpliendo los requisitos del enunciado y demostrando el uso correcto de SASS y Bootstrap 4 personalizados.