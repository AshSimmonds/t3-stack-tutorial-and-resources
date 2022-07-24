# T3 inspired stack resources  
  
Personal repo for documenting stuff as I go about learning and devving in the initial stack recommended by [t3-oss/create-t3-app](https://github.com/t3-oss/create-t3-app) as of July 2022 to cover most bases of almost any app. They all work well together, is intuitive to pick up, and really efficient to get going on actually creating useful stuff rather than spending hours boilerplating and trying to get disparate things playing nice. As time goes by I'll add other stack resources.  
  
Initially a compression of a [proposed tutorial](https://github.com/t3-oss/create-t3-app/issues/166#create-t3-app) which has more details for a newcomer. The following is more a quick refresher of just the hit points when you don't need explanations but just to follow the bouncing ball.  
  
This is not exhaustive nor definitive, just the way I've honed my routine for setting up a full-stack deployed environment within 5-10 mins which includes a front-end, styling, a database, an API, server routing, ~authentication~ (soon), and deployment.  
  
## Stack  

- NextJS
- Typescript
- tRPC
- TailwindCSS  
- Postgres  
- Prisma  
- Railway  
- Vercel 
- nextAuth  
  
## Products:  
  
Will only include stuff which fits my efficiency paradigm and which I've tested personally, so if you want Yarn or Linux or Vim or all-CLI etc seek elsewhere. But if you're just a regular schmoe dev this is all the stuff you need:  
  
- Windows 11  
- PowerShell  
- NPM/NPX  
- VSCode Insiders  
- GitHub Desktop  
  
## Mise en place  
  
Get stuff ready to go...  
  
### Railway

#TODO: railway instructions  
  
- https://railway.app/dashboard

### Vercel

#TODO: vercel instructions

## Initialise project
  
Powershell:  
```bash
cd \your-repo-parent-folder
npx create-t3-app@latest
```
  
### Name project  
  
>What will your project be called? `(my-t3-app)`  
  
### Illusion of choice  
  
>Will you be using JavaScript or TypeScript?  
  
### Select dev stack  
  
>Which packages would you like to enable?  
>
>`( ) nextAuth`  
>`( ) Prisma`  
>`( ) TailwindCSS`  
>`( ) tRPC`    

### Git gud  
  
>Initialize new git repo?  
  
Yup.  
  
### Setup project structure  
  
>Run NPM install?  
  
Sure.  
  
- scaffold: ~30 secs
- install packages: ~60 secs
- Git init: ~1 sec  
  
### Publish repo  
  
GitHub Desktop:  
  
```
Add existing repository
```
  
Select new repo folder that was just set up (already has git stuff in it).  
  
### Test project works  
  
Open in VSCode.  
  
Terminal:  
```bash
run npm dev
```

Navigate to `http://localhost:3000`, should see the landing page.  
  
## Setup database  
  
Terminal:  
```bash
railway login
```

Hit `enter` and it should open a browser and log you into your [Railway account](https://railway.app/dashboard). Can close that window when done.  
  
Terminal:
```bash
railway init
```
  
>Starting point:  
  
Select `Empty Project`. (I haven't tried other options yet)  
  
>Enter project name:  
  
Just use same name as current project, unless reasons.  
  
>Import (.env) environment variables?  
  
No need right now.  
  
It should auto-open a browser window to the Railway project.  
  
Terminal:  
```bash
railway add
```

Select database (postgresql).  
  
It should populate the Railway project browser window with new empty database.  
  
### Populate db credentials  
  
Railway browser:  
- select the database  
- click `Connect`  
- copy `Postgres Connection URL`  

VSCode:  
- open `.env` file  
- set `DATABASE_URL=postgresql://postgres:{password}@containers-blah-69.railway.app:7594/railway`  
- open `prisma/schema.prisma`  
- set  
```
generator client {
    provider = "prisma-client-js"
}

datasource db {
    provider = "postgresql"
    url      = env("DATABASE_URL")
}
```
  
### Create database tables/schema/client  
  
Terminal:
```bash
npx prisma migrate dev --name init
```

Migration takes about 30secs.  
  
Check back in Railway browser to see that the tables have been generated.  
  
Terminal:
```bash
npx prisma generate
```
  
Can now use `npx prisma studio` as a direct interface to the database on `http://localhost:5555`.  
  

  





