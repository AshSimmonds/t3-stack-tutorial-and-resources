# T3 inspired stack resources  
  
Personal repo for documenting stuff as I go about learning and devving in the initial stack recommended by [t3-oss/create-t3-app](https://github.com/t3-oss/create-t3-app) as of July 2022 to cover most bases of almost any app. They all work well together, is intuitive to pick up, and really efficient to get going on actually creating useful stuff rather than spending hours boilerplating and trying to get disparate things playing nice. As time goes by I'll add other stack resources.  
  
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
  
## Quick start  
  
Initially a compression of a [proposed tutorial](https://github.com/t3-oss/create-t3-app/issues/166#create-t3-app) with more details for a newcomer, still evolving as of 2022-07-24 on [t3-oss/create-t3-app](https://github.com/t3-oss/create-t3-app). The following is more a quick refresher of just the hit points when you don't need explanations but just to follow the bouncing ball.  
  
## Mise en place  
  
Get stuff ready to go...  
  
### Railway

#TODO: railway instructions

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

### Setup Git  
  
>Initialize new git repo?  

### Setup project structure  
  
>Run NPM install?  
  
- scaffold: ~30 secs
- install packages: ~60 secs
- Git init: ~1 sec  


