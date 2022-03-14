# Git and Github Commands for beginners
### 1. Git status
The **git status** command lists all the files that have been modified recently and has not been added to the local repository. In the below case the Two Sum.md file has not yet been added to the local repository
```
PS C:\Users\ERICA WANJA\Desktop\coding problems> git status
On branch main
Your branch is up to date with 'origin/main'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        leetcode/Two Sum.md

nothing added to commit but untracked files present (use "git add" to track)
PS C:\Users\ERICA WANJA\Desktop\coding problems>
```
### 2. Git add
**git add** command is used to move the files to the staging area for committing. To stage your files use the commands below;
**git add filename**- to add a specific file

`git add -all` which is shortened to `git add -A`  stages all the files, that is the new, modified and deleted files. On the other hand the `git add .` command stages only the new and modified files excluding the deleted files.

### 3. Git commit
`git commit` moves the repository from the staging area to the local repository. In other words, it stores the snapshots of the changes made to the local repository instead of blindly copying the entire repository one more time. 
Every time you are making a commit you must give a brief message explaining the changes made.
For example;
```
git commit –m “solved the two sum problem”
```
### 4. Git pull 
The pull command helps to keep your local repo up-to-date with the remote repository. It up streams any change made by another contributor in the remote repository to your local repository.
To pull the changes, you need to set the origin or parent remote repository
Command:
```
git remote add origin LinkToTheRemoteRepo
```
After setting the origin remote repository, you can now pull the changes using the below command;
```
git pull origin master
```
**Note:** it is a good practice that you pull the changes before the push command when working on a team’s project.
### 5. Git push
`git push` command transfers the commits changes from the local repository to the remote repository(GitHub). Thus, the changes you have made will be published on the central repository and made available online. 
Commands
`git push  origin main ` pushes the commits to the main or the master branch
`git push origin branchName` pushes the commits to the named branch.(you will learn about branches shortly)

If you have just started learning Reactjs or you need to keep abreast with jsx concepts you are in the right place. Here we go!

## What is reactjs JSX?

JSX in react stands for JavaScript XML. It is basically a JavaScript extension that allows us to write normal HTML code in JavaScript without appending elements. Look at the example below;

```
const element = <h1>Hello, world!</h1>;
```

The example above is not a normal JavaScript declaration neither the usual HTML, but JSX. Using create-react-app comes with an inbuilt compiler or transpiler known as babel that translates the above example to a normal Html code. 
 Let us trying outputting the complete code
```
import React from 'react';
import ReactDOM from 'react-dom';
	
const element= <h1>Understanding Jsx in reactJs</h1>

ReactDOM.render( element,
  document.getElementById('root')
);

```

Explanation: When executing the code above, the reactDom.render () function receives the first argument, which is named ‘element.’ However, this function expects an HTML element which is not the case. Thus, the babel compiler is called and translates the JavaScript object to a pure HTML element. Lastly, the render function displays the Html element to the root node. Thus it outputs a heading 1.

## Embedding Expressions in JSX?
Take a situation where you are receiving a JavaScript variable and you want to concatenate it with a jsx expression. Be warned! If you try the normal concatenation in JavaScript, you will get an error. So, how do you do that?
To pass a JavaScript expression in JavaScript you should pass it in curly brackets. Below is an example. 

```
import React from 'react';
import ReactDOM from 'react-dom';
	
const framework='Reactjs'
const element= <h1>We are learning {framework}</h1>

ReactDOM.render( element,
  document.getElementById('root')
);
```
You can also pass JavaScript expressions as attributes in jsx.

```
const element= <img src={userImage.user1} alt='person'></img>;

```

## JSX children
JSX expressions can also contain children. However, when you have more than one jsx expression, you should enclose them in curly brackets inside a code block.  For instance

```
import React from 'react';
import ReactDOM from 'react-dom';

const element= (
  <div>
    <h1>This is the first heading enclosed in a div</h1>
    <p>A paragraph in a div</p>
  </div>
)
ReactDOM.render( element,
  document.getElementById('root')
);
```
## Final Words
Jsx is among the main components of reactjs. We have looked at how to write a simple jsx, multiple jsx and even embedding JavaScript expression in jsx.





