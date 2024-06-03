

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
  <img src="https://github.com/cindi-sf/nextjs-web-app-test2/assets/171067216/fd7284ee-f562-4b13-acb3-0410a0074142" alt="Captura de tela 2024-06-03 113920" width="200"/>
</p>

### 3. Add firebase to your web app

- On the project root, execute the following command in the terminal:

```bash
npm install firebase
```

```bash
npm install -g firebase-tools
```

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
- In which region would you like to host server-side content, if applicable? - Select the region where your application will be hosted 
- Set up automatic builds and deploys with GitHub? - **No** (**Yes** is not covered in this tutorial)
- You should get a message “Firebase initialization complete!” 

```bash
firebase deploy
```

Here is the URL generated for the project hosted by Firebase: [https://nextjs-web-app-test2.web.app](https://nextjs-web-app-test2.web.app)
