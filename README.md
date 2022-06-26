# How to deploy React App on GitHub Pages?

Push your code to GitHub first!
```
git init
git remote add origin [YOUR-REPO-LINK]
git add -A
git commit -m "Initial commit"
git push -u origin main
```

> The following tutorial includes running commands in terminal, all those commands will be performed under your local react-app directory.
> <br>
> Therefore, please change your directory to your react-app in terminal before performing any commands.

### <a name="step-1"></a> Step 1
Go to `package.json` in the your react-app, and add the following new key value pair.
```
"homepage": "https://[USERNAME].github.io/[YOUR-REPO-NAME]"
```
<img width="722" alt="image" src="https://user-images.githubusercontent.com/69583542/175571008-a46366ff-5eb7-406f-826b-5e6d6a797637.png">

### Step 2
Go to the terminal and install the GitHub Pages npm package inside your react-app.
```
npm install gh-pages --save-dev
```

### Step 3
Go to `package.json` in the your react-app again, and add the following new key value pair ___inside "scripts"___ .

```
"predeploy": "npm run build",
"deploy": "gh-pages -d build",
```

<img width="426" alt="image" src="https://user-images.githubusercontent.com/69583542/175572241-549c1543-7c87-4146-a3e5-53977a2d9b1c.png">

### Step 4
Go to terminal and run the following command to deploy your react-app on GitHub Pages. 
```
npm run deploy
```
Also, if you made any changes and would like to publish the changes, you can run this command to update the changes!

### Conclusion
Congratulations! You have successfully deployed your React App on GitHub Pages!
<br>
Now your repository should have a new branch called `gh-pages` and you can access your React App via the URL in __[Step 1](#step-1)__!

Access via `https://[USERNAME].github.io/[YOUR-REPO-NAME]`

