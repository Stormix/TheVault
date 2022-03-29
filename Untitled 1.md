## Question:  Create a shell script that displays the ids of the last 5 scripts

- Create a shell script = "make a file called whatever.sh and put some code inside of it to do stuff" 

- The `sh` extension is short for `shell`
- so a shell script is a file with an extension `.sh


```
touch git_commit.sh
```


```
sh git_commit.sh
bash git_commit.sh
```

To make a file an executable: 
```
chmod +x git_commit.sh
```



## How to use nano

To make a file or edit a file: 

```
nano filename.whatever
```

for example to make a file called git_commit.sh

```
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

To change the output of git log you need to add

```
git log --pretty="format:%H"
```

  
[](https://git-scm.com/docs/git-log#Documentation/git-log.txt-emHem)_%H_

    commit hash is the commit ID ("The long text you saw in the example ")

[](https://git-scm.com/docs/git-log#Documentation/git-log.txt-emhem)

```
❯ cat git_commit.sh
git log --pretty='format:%H' -n 5
```

```
❯ bash git_commit.sh | cat -e
bf059518c4567db4d3676043f75f262fe9d646ac$
3b0dbe391162219430423010ae72cf1dd4a2554b$
53c35816c777d332ad48d23cbeeebfa790dad3a0$
00c47212419627372592e54c7a08886241334dfe$
438d2b0d931e9aee8e321079fd7511f1a94a2b11%
```

![[Pasted image 20220329194247.png]]



find . -type f -name "#*~" | rm 