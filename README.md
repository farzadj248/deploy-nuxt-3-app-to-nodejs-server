deploy-nuxt-3-app-to-nodejs-server(cpanel)

If you want to deploy with SSR enabled on nodejs server:

1.go to project directory from cmd or editor terminal

2.You need to run:
    npm run build
    *after run this command in terminal added .output folder in main project directory.
    
3.go to cpanel > setup node.js app and create new app sample bellow:

    Application root: app
    Application URL: / 
    Application startup file: app.js or sample.js
    and in end of press create button.
    after some minute app created successfully.

![Untitled](https://github.com/farzadj248/deploy-nuxt-3-app-to-nodejs-server/assets/55263969/ae92c314-5a4b-40d2-97d2-e984de71a6f1)


4.go to cpanel File Manager > app folder and edit app.js or sample.js.
  add this code : import('./.output/server/index.mjs');
  then save and exit.

5.then compress .output folder and upload in cpanel app folder and extract it.

6.go to cpanel > setup node.js app and click start app button

7. run your domain(Application URL) in the browser

To deploy without SSR, you have to use the generate function, which only works if you do not use code that requires SSR.
