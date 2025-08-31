#video lecture 7, connecting database to the application
Day 2 continues --

1. We are using online mongo db to connect to out application.

steps: login to mongodb atlas
setup project, give network access as peryour need, for now 0.0.0.0/0 means allow to all.
setup .env file by setting required variable like port no, mongodb_url etc. (all the required environment variables)

2. we can store db_name in constants file or in the env file.
   It ispersonal choice, but db_name might or might not be enviroment dependent, so we are keeping it in constants file.

3. There are two ways to connect to database.
   First:
   as we are executing the index.js file using the nodemon or automatic server starter, we can add the database connection code inside this file only, which means when the file executes, it will connect to the database first and then do the other stuff.

Second:
or we can keep the whole code in seprate file named db, and export the function and call it inthe index.js file

Both have there pros and cons
following the second approach, it will keep the code modular and clean, which is best suited for professional use cases
So, use this only....

4. install packages mongoose, express and dotenv.
   all these will be used in the development...mongoose and express are somethings with which we are familier but, dotenv is something new.

5. SOME POINTS TO PONDER:
   A. while talking to db, problems may arise - so always wrap the code(for DB talking) in try-catch
   B. Or you can take promises also
   C. Always remember, Database is in another continent,
   it doesnt means litrally, but it means that while talking to database, it will take time - so also use async-await

6. acc to mongoose documentation the database can be connected in a single line of code.
   But its not the professional approach, so always the above methods by creating function.

7. we willbe using iffies. They are nothing but codes that executes immediatly. it is written in following way:
   ;(()=> {})()
   always start with semi colon, as while using iffies, if the formatter or you forgets to add semicolon in the last line, it might arise and error.
   So, it a good practise followed by everyone in the community to add semicolon in the starting of a iffi

8. after imorting the mongoose and db_name into the file, we sometimes see something else also.
   Importing express and creating a const app = express()
   and after that we add listeners afte the mongoose.connet line

these listners are used to know that after connection of the mongodb code line, the app might not be able to talk to the application, so to check that we add listners.

Like app.on("error", (error) => {
//listner
console.log("ERRRR", error);
throw error;
})

this is our first approach.

9. Now we will see our next approach.
   It is nothing, just abit more professional apporoach, we will crete a function inside the db/connection/or some other folder of our liking, and we will import this in to our main index.js file

10. Inside you db folder in src, create a index.js file.

11. import mongoose in it
