## Question:  Create a shell script that displays the ids of the last 5 scripts

- Create a shell script = "make a file called whatever.sh and put some code inside of it to do stuff" 

- The `sh` extension is short for `shell`
- so a shell script is a file with an extension `.sh


```bash
touch git_commit.sh
```


```bash
sh git_commit.sh
bash git_commit.sh
```

To make a file an executable: 
```bash
chmod +x git_commit.sh
```



## How to use nano

To make a file or edit a file: 

```bash
nano filename.whatever
```

for example to make a file called git_commit.sh

```bash
nano git_commit.sh
```

## How to save, quit ..etc?
`CTRL + X`
![[Pasted image 20220329190305.png]]
Than you click on `Y` to save or `N` to discard the file
![[Pasted image 20220329190315.png]]
And than press `Enter`.


# Git


## To start a new git repository aka a new project
`git init`
To make a commit you need to do:
`git add (filename)` or `git add .` 
`git commit -m "<a message here>"`
And then to push the changes:
`git remote add origin <url>` - you only need to do this if you're making a new git repo that you want to upload
`git push`


## Using an exisitng repository
`git clone <url>/project.git` - you download a repository
^ this will make a folder called `project/` and with the downloaded stuff in it

`cd project/`
`touch newfile`
`git add .`
`git commit -m "horray I added a new hoe"`
`git push`



## Exo 05
### STUPID EXO
They ask you to make a file called git_commit.sh
and then to run it using ```

```
bash git_commit.sh | cat -e

lkgdfsjgdfjmklgùmdfs$
fkdsgjmlkfdskjglkùmj$
gdfkjlsgjpdsfjmgjdfk$
fkdsgjmlkfdskjglkùmj$
gdfkjlsgjpdsfjmgjdfk$
```

This has 2 parts, it first
Runs the script: `bash git_commit.sh`
And then pipes the output to `cat -e`

## Some operators: 
- A | B : take whatever `A` outputs and run `B` with it
- A > B : take whatever `A` outputs and puts it in `B` (! it will overwrite the file)