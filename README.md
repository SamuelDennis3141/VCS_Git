# Git
![image](https://user-images.githubusercontent.com/112982429/188729339-bc6b7e47-64d6-4c01-a101-68fc33c0a4fc.png)

## What is Git?

Version control, also known as source control, is the practice of tracking and managing changes to software code. Version control systems are software tools that help software teams manage changes to source code over time. As development environments have accelerated, version control systems help software teams work faster and smarter. They are especially useful for DevOps teams since they help them to reduce development time and increase successful deployments.

Git is an open source version software for distributed version control. This means that it tracks and manages changes to software code (over time). Version control systems generally help teams work faster as they increase successful deployments. 

Git also can give each developer a local copy of the full development history, and changes are copied from one such repository to another.

Git handles content in snapshots, one for each commit, and knows how to apply or roll back the changes between two snapshots.

### Benefits of Git over other Version Control Systems?

- It is open source (free)
- Faster to commit than other VCS
- Available offline
- No single point of failure

## How does Git work?

![image](https://user-images.githubusercontent.com/112982429/188729841-f6fa8a8b-2e8c-4a57-89ab-482d4fbebdee.png)

As can be seen above, the git workflow includes 4 elements.

- Working directory
- Staging area
- Commited files
- Remote repository

The first three are all located on the localhost.

### Pushing from LocalHost to Remote Repository

So, the developer finishes writing his code and wishes to push his changes to a remote repository where it can be accessed by others.

The first thing they must do is stage their changes to be commited. This can be done with `git add`.

- `git add .` adds all altered files to be staged 
- `git add file.txt` adds just that specific file to be staged

The developer can check the status of staged and tracked files through `git status`.

To then commit these changes (to be snapshotted) the developer can use:

`git commit -m "message"`

The -m "message" will attach a brief message to the commit which allows others to understand what the change has done to the code.

From here the code can then be pushed to a remote repository such as git hub using `git push -u origin main` where it can be accessed by fellow developers with access.

### Pulling from Remote Repository to LocalHost

Sometimes changes are made to the remote repository from other developers and you may need access to these changes.

This can be done with `git pull`.

This pulls from the remote repository onto your current branch.

### Branching

Git branches are effectively a pointer to a snapshot of your changes. When you want to add a new feature or fix a bug—no matter how big or how small—you spawn a new branch to encapsulate your changes. This makes it harder for unstable code to get merged into the main code base, and it gives you the chance to clean up your future's history before merging it into the main branch.

![image](https://user-images.githubusercontent.com/112982429/188734273-d92dedc6-8e30-4f01-8021-7e8c6b1f15dc.png)

You can change branches by using `git checkout <branchname>`. 
