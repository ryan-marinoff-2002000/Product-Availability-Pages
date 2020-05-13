# Steps to follow to create a new service

1. Setup Repository - Do not initialize them, that will be done locally
    1. Github
    2. Gitlab
    3. Keybase (not required)
2. Get Spring Boot starter project from initializr
    1. Group: com.cogizant.rmarinoff
    2. Artifact: service-name
    3. Description: Application name service name
    4. Add dependencies
3. Setup local repository and push to remote repos
    1. extract starter project in the directory structure for the project
    2. Open PowerShell within this extracted directory
    3. Create README.md
        1. New-Item README.md
        2. Set-Content README.md '# Project Name'
    3. Run GIT commands:
        1. git init
        2. git remote add origin [github_repo_url]
        6. git remote set-url --add --push origin [github_repo_url]
        5. git remote add gitlab [gitlab_repo_url]
        7. git remote set-url --add --push origin [gitlab_repo_url]
        8. git add README.md
        9. git commit -m "Initialize with README.md"
        10. git push origin master
        8. git banch develop
        9. git checkout develop
        3. git add .
        4. git commit -m "Initial commit"
        12. git push origin develop
4. Setup gitlab branch protections (for CICD pipeline)
    1. Settings > Repository > Default Branch = develop
    2. Settings > Repository > Protected Branches
        1. Branch = develop
        2. Allowed to merge: Maintainers
        3. Allowed to push: No one
        4. click Protect button
        5. change master Allowed to push to No One
5. Set develop as main branch for github
    1. Settings > Branches > Default branch = develop
    2. click Update button
    3. Understand the warning

Now continue as you normally would, when new branches are created, pushing to origin will update both repositories. CICD will occur on GitLab, so you will need to update GitHub when feature merges occurs:

