-- Para usar typescript con node
npm i typescript ts-node-dev @types/node -D

-- Para configurar typescript
npx tsc --init
-- Luego configurar en tsconfig:
"rootDir": "./src"
"outDir": "./dist"
-- Luego en el package.json en el apartadod e scripts colocar lo siguiente:
"dev": "ts-node-dev --respawn src/index.ts"

-- Crear una dependencia de desarrollo de prisma
npm i prisma -D

-- Para inicializar la configuración de prisma
npx prisma init

-- Para decirle con que base de datos se hará
npx prisma init --datasource-provider sqlite

✔ Your Prisma schema was created at prisma/schema.prisma
You can now open it in your favorite editor.

Next steps:

1. Set the DATABASE_URL in the .env file to point to your existing database. If your database has no tables yet, read https://pris.ly/d/getting-started
2. Run prisma db pull to turn your database schema into a Prisma schema.
3. Run prisma generate to generate the Prisma Client. You can then start querying your database.

More information in our documentation:
https://pris.ly/d/getting-started

-- Una vez creado la sintaxis, se debe hacer una migración, lo cual es convertir la sintaxis de de prisma a la base de datos específica como desarrollo
npx prisma migrate dev

-- Para hacer alguna alteración de tablas que se hagan en el proceso
-- Para hacer despliegue de la base de datos a producción
npx prisma [command]

-- Para acceder a la interfaz gráfica de prisma (prisma studio), se abre en el puerto 5555.
npx prisma studio

-- Para deployar migraciones directamente a la base de datos
prisma migrate deploy
