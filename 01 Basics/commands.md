#Terminal

pwd => shows where are we

cd / cd .. => navigate

ls => similar to dir in msdos. Una versión guay es "ls -aF"

man "X" => change "X" to get info about a command, to quit press Q

source activate ENVIROMENT_NAME => change enviroment name for the python enviroment that you want to use

Control + a => move to the first position of the current line

Control + e => move to the last position of the current line

# GIT

## 1. Setup your repo
- On Github, go to: https://github.com/felipeam86/clue_hackathon_code and
fork the repo. The fork icon is on the top right corner of the screen

- Clone your own repo to your machine, e.g.,

```bash
git clone git@github.com:GregVial/clue_hackathon_code.git
```

- On your machine, create a link with the central upstream repo:

```bash
git remote add upstream git@github.com:felipeam86/clue_hackathon_code.git
```

To this point, your master should be pointing to your github fork and the
upstream should be pointing to Felipe's version

## 2. Workflow

- Push: always to your github
```bash
git add model.py data.py
git commit -m "description of change"
git push origin master
```

- When you want to propose changes, go to your github and make a pull
 request (merge) that will be discussed and accepted on Felipe's repo

- Refresh your repo with new contributions from the team by pulling from
upstream

```bash
git pull upstream master
```
