Help: java -jar sfrc.jar help
Help commit: java -jar sfrc.jar help commit
Help merge: java -jar sfrc.jar help merge
Help init: java -jar sfrc.jar help init
Help checkout: java -jar sfrc.jar help checkout
Help branch: java -jar sfrc.jar help branch

Init: java -jar sfrc.jar init -f A.txt

Our Commit method will automatically generate version number. The initialized version is 1.0, then every commit make the value behind dot increment by one, like 1.0 -> 1.1 then 1.1 -> 1.2. If doing branch, we make it from 1.2 to 1.2.1, adding another dot. And our default and main branch is 1, while a new branch will automatically increment by one, like 1 -> 2.

Commit: sfrc.jar commit -f A.txt -m "string"

Our Checkout will go back to the revision determined by the user, but the revision needs to be commited before.

Checkout: sfrc -jar checkout -rev revision -f A.txt

Our Merge will ONLY merge from a non-main branch to our main branch(1) and add the result to the main branch, so we only have one revision parameter which is not in main branch for users to choose. User also needs to checkout the current file to the latest version in main branch to do the merge.

Merge: sfrc -jar merge -f A.txt -rev revision -m "String"

Our Branch is to list all branches we have. The first one is the current used branch.

Branch: sfrc -jar branch -list A.txt

If you have some further questions, please contact tailin-lyu@uiowa.edu. I would respond ASAP.

