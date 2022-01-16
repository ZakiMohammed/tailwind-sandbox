# TailwindCSS Sandbox

The sandbox project for learning TailwindCSS for the berry first time!

## Initial Setup

Doing setup as per TailwindCSS official docs: https://tailwindcss.com/docs/installation

#### Install TailwindCSS
```
npm i -D tailwindcss
npx tailwindcss init
```

#### Configure the source
```
module.exports = {
  content: ["./src/**/*.{html,js}"],
  theme: {
    extend: {},
  },
  plugins: [],
}
```

#### Create source folder and input file
```
src/input.css

@tailwind base;
@tailwind components;
@tailwind utilities;
```

#### Run watch command
```
npx tailwindcss -i ./src/input.css -o ./dist/output.css --watch
```

#### Create index file and include output.css
```
<!DOCTYPE html>
<html lang="en">

<head>

    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <link rel="stylesheet" href="./../dist/output.css">

    <title>TailwindCSS Sandbox</title>
</head>

<body class="bg-slate-200">
    <h1 class="text-4xl text-purple-500 font-bold text-center my-4">
        TailwindCSS Sandbox
    </h1>
</body>

</html>
```