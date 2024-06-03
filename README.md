

# How to deploy a Next.js application on Firebase Hosting

### 1. Create a new Next.js app or use an existing one
I used the following command to create the latest version of the Next.js web app:

```bash
npx create-next-app@latest .
```
### 2. Set up a Firebase project and a web application

- Click on 'add project' in the Firebase Console:

<p align="left">
  <img src="https://github.com/cindi-sf/nextjs-web-app-test2/assets/171067216/f6ff7f62-38db-4872-8538-1ae2c6bf153c" alt="Captura de tela 2024-06-03 113920" width="300"/>
</p>

- Type a name to your project:

<p align="left">
  <img src="https://github.com/cindi-sf/nextjs-web-app-test2/assets/171067216/8fab5ab5-da5b-4894-b08a-09fac2ca001b" alt="Captura de tela 2024-06-03 113920" width="300"/>
</p>

- Follow the next step and click on the 'Create project' button:

<p align="left">
  <img src="https://github.com/cindi-sf/nextjs-web-app-test2/assets/171067216/df022cd9-98bf-4214-aac3-9ba39b4248fb" alt="Captura de tela 2024-06-03 113920" width="200"/>
</p>

- After creating the project, add web app to your project by clicking on it:

<p align="left">
  <img src="https://github.com/cindi-sf/nextjs-web-app-test2/assets/171067216/6f11b320-d099-430e-ab9d-e87a2df4e456" alt="Captura de tela 2024-06-03 113920" width="200"/>
</p>

- Choose app’s name;
- Check the box for "Also set up Firebase Hosting for this app";
- Select the project on the dropdown menu.
- Click on "Register app".

<p align="left">
  <img src="https://github.com/cindi-sf/nextjs-web-app-test2/assets/171067216/9d8959ce-1ccd-448d-94b6-ce34ad648ffb" alt="Captura de tela 2024-06-03 113920" width="200"/>
</p>

### 3. Add firebase to your web app

- Copy the code below from Firebase:

<p align="left">
  <img src="https://github.com/cindi-sf/nextjs-web-app-test2/assets/171067216/623bcd8c-08a3-4c82-88ac-a6b596ef2a15" alt="Captura de tela 2024-06-03 113920" width="200"/>
</p>

- Manually create a firebase.js file inside the app folder and paste the code into your project:

<p align="left">
  <img src="https://github.com/cindi-sf/nextjs-web-app-test2/assets/171067216/87ec4eed-b115-4067-a4b3-2a20c9c5a1be" width="500"/>
</p>

- On the project root, execute the following command in the terminal:

```bash
npm install firebase
```

```bash
npm install -g firebase-tools
```

<p align="left">
  <img src="https://github.com/cindi-sf/nextjs-web-app-test2/assets/171067216/8cd400c7-78e1-4b31-9411-313298474ef7" width="500"/>
</p>

```bash
firebase login
```
- Click on a URL in the terminal and sign in using your Google Account.

- To ensure that you completed it correctly, run firebase projects:list and confirm that the project you created is visible in the terminal.

<p align="left">
  <img src="https://github.com/cindi-sf/nextjs-web-app-test2/assets/171067216/5e8a8118-890b-4c1b-b4b4-688e2e35f171" alt="Captura de tela 2024-06-03 113920" width="500"/>
</p>

### 4.  Integrate Firebase with your Next.js app

Link to docs: [https://firebase.google.com/docs/hosting/frameworks/nextjs](https://firebase.google.com/docs/hosting/frameworks/nextjs)

Run in the terminal:

```bash
firebase experiments:enable webframeworks
```

```bash
firebase init hosting
```

Answer to questions in terminal by **Y** or **N**

- You are initializing within an existing Firebase project directory? - **Yes** 
- Detected an existing Next.js codebase in the current directory, should we use this? - **Yes** 

<p align="left">
  <img src="https://github.com/cindi-sf/nextjs-web-app-test2/assets/171067216/1bdd7df1-101c-4692-9eb8-3c867fa7f37e" alt="Captura de tela 2024-06-03 113920" width="500"/>
</p>

<p align="left">
  <img src="https://github.com/cindi-sf/nextjs-web-app-test2/assets/171067216/c6d94048-a06d-48e4-bf69-f8482b5f1bea" alt="Captura de tela 2024-06-03 113920" width="500"/>
</p>

- In which region would you like to host server-side content, if applicable? - Select the region where your application will be hosted 

<p align="left">
  <img src="https://github.com/cindi-sf/nextjs-web-app-test2/assets/171067216/0fcfe6f8-4e25-430a-b91a-cfbf5867dea6" alt="Captura de tela 2024-06-03 113920" width="500"/>
</p>

- Set up automatic builds and deploys with GitHub? - **No**

<p align="left">
  <img src="https://github.com/cindi-sf/nextjs-web-app-test2/assets/171067216/cfb2ffc1-c108-4477-8e49-f205acb1231e" alt="Captura de tela 2024-06-03 113920" width="500"/>
</p>

- For **Yes** option for automatic deploys with GitHub: [https://adelpro.medium.com/how-to-deploy-your-website-to-firebase-hosting-for-free](https://adelpro.medium.com/how-to-deploy-your-website-to-firebase-hosting-for-free-be5e5ff58796)
- You should get a message “Firebase initialization complete!”

<p align="left">
  <img src="https://github.com/cindi-sf/nextjs-web-app-test2/assets/171067216/ad330380-cd0a-40cd-9e69-4594dd22099b" alt="Captura de tela 2024-06-03 113920" width="500"/>
</p>

- A firebase.json file will be created:

<p align="left">
  <img src="https://github.com/cindi-sf/nextjs-web-app-test2/assets/171067216/5f8d1506-8263-4bd1-a3ca-e6b869ef1ea5" alt="Captura de tela 2024-06-03 113920" width="500"/>
</p>


```bash
firebase deploy
```

Here is the URL generated for the project hosted by Firebase: [https://nextjs-web-app-test2.web.app](https://nextjs-web-app-test2.web.app)

### Other useful links:

[https://adelpro.medium.com/how-to-deploy-your-website-to-firebase-hosting-for-free](https://adelpro.medium.com/how-to-deploy-your-website-to-firebase-hosting-for-free-be5e5ff58796)

[https://levelup.gitconnected.com/deploying-your-website-to-firebase](https://levelup.gitconnected.com/deploying-your-website-to-firebase-ddfc97d0bdb7)

