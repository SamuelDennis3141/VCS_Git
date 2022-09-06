# Connectivity to GitHub

![image](https://user-images.githubusercontent.com/112982429/188737827-0cff88f4-a5a9-4700-b6e1-afc5091481bb.png)

SSH and HTTP Connection will be covered here.

## HTTPS Connection

The https method is the most simple to set up however is not as secure as 
```
echo "# test" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/SamuelDennis3141/test.git
git push -u origin main
```

## SSH Connection

In this case a key pair has to be set up and added to GitHub.

### Creating a key pair

- On your localhost navigate to your .ssh folder `cd ~/.ssh`
- Run the command `ssh-keygen -t rsa -b 4096 -C "github@email"`
- Set passphrases 
```
> Enter passphrase (empty for no passphrase): [Type a passphrase]
> Enter same passphrase again: [Type passphrase again]
```
Now you need to add to the SSH agent

- `$ eval "$(ssh-agent -s)"`
- `ssh-add ~/.ssh/key_name`

### Add the Public Key to Github

- `clip < ~/.ssh/key_name.pub` copies the public key to your keyboard
- Go to your github account settings and select SSH and GPG keys

![image](https://user-images.githubusercontent.com/112982429/188740052-1730076f-72cb-4162-ab30-8ba7b4924205.png)

- Now click add key and paste the .pub key into the key section. It is also good practice to use the name of the key in your localhost as the title of the key.

![image](https://user-images.githubusercontent.com/112982429/188740828-32678dab-a9a7-4c04-960c-3a4c90987ce0.png)


### Pushing to Github
```
echo "# test" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin git@github.com:SamuelDennis3141/test.git
git push -u origin main
```

