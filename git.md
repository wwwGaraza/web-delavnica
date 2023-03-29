# GIT

## Osnovni workflow

    # Najprej narediš fork repozitorija, če je to potrebno.

    # Kloniraš repo
    git clone git@github.com:<username>/<repo>.git
    cd <repo>

    # Narediš nov branch in zamenjaš nanj

    git branch <nek-branch>
    git checkout <nek-branch>
    # ali pa
    git checkout -b <nek-branch>

    # Spremeniš datoteke, ki jih želiš in jih dodaš v staging area:
    nano <datoteka>
    git add <datoteka>

    # Commit in push
    git commit -m "Fixed a bug"
    git push --set-upstream origin <nek-branch>
