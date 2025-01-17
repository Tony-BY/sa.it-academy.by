## 03.GIT.HOSTING

[GitHub](https://github.com/EvgeniErmakov/yes-i-still-love-you)
-
[GitLab](https://gitlab.com/EvgeniErmakov/yes_i_still_love_you)
-
[Bitbucket](https://bitbucket.org/evgeniermakov/yes-i-still-love-you)
-

## Slack

![slack's notifications](slack.png)

## Script

```bash
#!/bin/bash
count=$#
if [ $count != 0 ]; 
then
  for text in "$@"; 
  do
    if [[ $text == -h || $text == --help ]]; 
    then
      echo "This script allows you to push commits from the current branch of the local repository to remote repositories.
            Specify the names of the repositories as options or the -all flag to push changes to ALL remote repositories.
    	gitpush -all
    	gitpush [your repository name]"
    elif [[ $text = --all ]]; 
    then
      git remote | while read -r repositoryName; 
      do
        git push -f $repositoryName
        echo "$repositoryName was updated."
      done
    else
      git push -f $text
      echo "$text was updated."
    fi
  done
else
  echo "Pass at least one parameter. Use the --help or the -h flag for details."
  exit 1
fi
```
