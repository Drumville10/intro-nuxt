import { Link, Navbar } from '../.nuxt/components';
<template>
    <div>
        <Navbar/>

        <main>
            <slot></slot> //cargar contenido en el layout
        </main>

        <footer>
            &copy; Jorge Zegarra - {{ currentYear }}
        </footer>
    </div>
</template>

<script setup>

    useHead({
        link: [
            {
                rel: "stylesheet",
                href: "https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css",
                integrity: "sha384-QWTKZyjpPEjISv5WaRU9OFeRpok6YctnYmDr5pNlyT2bRjXh0JMhjY6hW+ALEwIH",
                crossorigin: "anonymous"
            }
        ],
        script: [
            {
                src: "https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js",
                // body: true
            }
        ],
    })

    const currentYear = new Date().getUTCFullYear();
</script>