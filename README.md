A simple rust project that uses RustEmbed to package a Vite+Svelte project, which can serve as a template for starting a new rust + Svelte project.

To run it, first build the web project:
```bash
cd web
npm install
npm run build
```

Then run the rust project:
```bash
cd ..
cargo run
```

The web project will be served at `http://localhost:3030/myapp`.
