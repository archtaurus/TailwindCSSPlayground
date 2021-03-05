# TailwindCSS Playground

This repository is a playground for TailwindCSS. `code . & npm start` and have fun.

## Use this repository

``` shell
git clone git@github.com:archtaurus/TailwindCSSPlayground.git
cd TailwindCSSPlayground
npm i -D
code . & npm start
```

## Build it by yourself

``` shell
mkdir TailwindCSSPlayground
cd TailwindCSSPlayground
echo '{
    "name": "tailwindcss_playground",
    "scripts": {
        "start": "vite --open"
    },
    "author": "Zhao Xin <7176466@qq.com>",
    "license": "MIT",
    "devDependencies": {
        "autoprefixer": "^10.2.4",
        "postcss": "^8.2.7",
        "tailwindcss": "^2.0.3",
        "vite": "^2.0.5"
    }
}' > package.json
npm i -D
npx tailwindcss init -p
echo "export default {
    root: 'src',
    server: {
        port: 8000,
        host: 'localhost',
    },
}" > vite.config.js
mkdir src
curl "https://tailwindcss.com/favicon-32x32.png" -o src/tailwindcss.png
echo "@tailwind base;
@tailwind components;
@tailwind utilities;" > src/style.css
echo '<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="UTF-8" />
        <meta name="viewport" content="width=device-width, initial-scale=1.0" />
        <title>TailwindCSS Playground</title>
        <link rel="icon" type="image/png" sizes="32x32" href="tailwindcss.png" />
        <link rel="stylesheet" href="style.css" />
    </head>
    <body class="antialiased text-gray-800 select-none">
        <div class="flex items-center justify-center min-h-screen bg-green-900">
            <h1
                class="flex items-center justify-center gap-4 px-16 py-8 font-sans text-4xl font-bold bg-green-500 border-2 border-green-600 rounded-full shadow-md text-green-50"
            >
                <img class="inline-block p-2 border border-green-400 rounded-full bg-green-50" src="tailwindcss.png" alt="TailwindCSS" /> TailwindCSS Playground
            </h1>
        </div>
    </body>
</html>' > src/index.html
code . & npm start
```
