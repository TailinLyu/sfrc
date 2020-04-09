# Single File Version Control System

CS:2820 **Object-Oriented Development** Final Project. You can understand it as a very naive version of **Git**

## Quick Start

Before you do any changes in *sfrc*, you need to init it:
```
Init: java -jar sfrc.jar init -f A.txt
```

## Commit


Our Commit method will automatically generate version number. The initialized version is 1.0, then every commit make the value behind dot increment by one, like 1.0 -> 1.1 then 1.1 -> 1.2. If doing branch, we make it from 1.2 to 1.2.1, adding another dot. And our default and main branch is 1, while a new branch will automatically increment by one, like 1 -> 2:

```
sfrc.jar commit -f A.txt -m "string"
```

## Checkout

Our Checkout will go back to the revision determined by the user, but the revision needs to be commited before:

```
sfrc -jar checkout -rev revision -f A.txt
```

## Merge

Our Merge will ONLY merge from a non-main branch to our main branch(1) and add the result to the main branch, so we only have one revision parameter which is not in main branch for users to choose. User also needs to checkout the current file to the latest version in main branch to do the merge:

```
sfrc -jar merge -f A.txt -rev revision -m "String"
```

## Branch

Our Branch is to list all branches we have. The first one is the current used branch:

```
sfrc -jar branch -list A.txt
```

## Help

If you needs help with any above method, try use help commands below:

```
java -jar sfrc.jar help
java -jar sfrc.jar help commit
java -jar sfrc.jar help merge
java -jar sfrc.jar help init
java -jar sfrc.jar help checkout
java -jar sfrc.jar help branch
```

## License

The project is completed by @Tailin.If you have some further questions, please contact tailin-lyu@uiowa.edu. I would respond ASAP.

