#These are my notes and here I will keep track of all the thing that I have been doing thoroughout the project

Day one:
We will be making a youtube backend, and it will have everything that we need.

1. create a folder, open that folder in vs code, run npm init command that will create "package.json" file in the folder
2. create a repo in the github in your browser.
3. run git init in your vs code terminal - it will initialize the git for tracking and all the stuff.
4. run git add . - this will add all files to git, in the local system
5. runb git commit -m "your message",
6. change the root branch to main using git branch -M main
7. now run, git remote add origin your_repo_link, and, git push -u origin main
8. Voila, your all the current files will be uploaded to github
9. git status - to check the status and condition of the local commits and tree
10. -+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-
    There are senarios when the file is uploaded, it might firstly get uploaded to a local server by that commany, then to the main server or companies cloud storage
    this is because sometimes, while uploading directly to the main server and the intenet "goes off" or anything else happening, it will not raise some serious issues.
    Also, uploadeing to a local server will be faster and the further process can continuein the backend.

+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+- 11. while we create folder that are empty currently but we might need them in the future and are must, such folders are not recognized by git.
So, in order to make git to create those folders recognized, we add .gitkeep file. It still can be empty, but because of its presence, the git will recognize it.

Note: you can create a text file or any other file for the same task also.

12. create a .gitignore file in the outmost folder
    The project we will be creating, will have files and something that are crucial & sensitive and should not be pushed to the github, such files names can be added in this file, and git will ignore them will commits and adding of files

You can use gitigne generators for creating such file, dont need to type eac and every name of the file

best: mrkandreev.name - git ignore generator

13. Env file:
    this creates environment variables that are required to run system locally and on the server.
    These are passed as environmnet files while hosting them on server.
    And they must not be uploaded to github, now a days github gives warning about uploading such thing, but it should be kept out from github.

14. create a src folder and the required files in it app.js, constants.js, index.js.

15. keep the type in the package.json file as module, this defines the module format that Node.js uses

16. we can start and stop server manually, but while testing stuff for a large project, this might turn out to be consuming large amount of time,

so, we will be using a utility name "NodeMon", it automatically restarts the server when a file is saved.

In nodemon, we usually install the devdepencies nodemon, because the is used in the development of the project, not after the product has gone to production level.

we also have option to install main dependency.
As of now , install dev dependency using command npm install -D nodemon

17. in the script tage in the package.json, add "dev": "nodemon src/index.js" inside the scripts

18. as we are using the dev dependencies of the nodemon, we have to use require syntax for the dot env file,
    just seach it in the nodemon website
    more on this later on

Day 2:

1. make folders inside teh src folder only, using mkdir controllers db middlewares models routes utils

Controllers have the functionality, db will have how to connect to database, no matter what is the database, database logic is writtn in here

Middlewares are codes that executes in between the server and the client are called middlewares. They are usually for checking what is files or request while a request is made to the server.
During an request, we can ask for the cokkies to verify the request and the data passing through.

Utils are utilities of the system, like file upload is utility, it is seen for both photos videos etc, so it is good to create an utility for the same.
Same can be done for sending mail or like taking tokens etcs,
So the things or functionality that will repeat is kept in a single folder and it is called utility

2. install prettier's dev dependency using npm install -D prettier,
   we will be using this to define spacing and other formatting thing so that when mulitple people are working on same project and if all the diffrent system on which people are working have diff. configuration of formatting it will arrise collisions while deploying the creating pull or push requests.

So, the formatting is usually decided by the project manager for the project,and it remain same throughout the project for each and every system.

It is defined in .prettierrc file

we can define the tabwidth, we want semi colons or not, want singlequote or not, etc etc.
In a nutshell all the formatting related things can be defined in this file.

3. similar to gitignore we have prettier ignore,
   in this file, we define which files should not be formatted by prettier.

the wierd syntax of .env files or the vscode setting files should be mentioned in it, along with other files of your choise.

-------video ends , move to the next node Notes2.md file-------
