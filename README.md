# ghost-inspector-github-action
A Ghost Inspector GitHub action for CI/CD workflows to automate test suites on pull requests. 

![alt text]([http://url/to/img.png](https://www.google.com/url?sa=i&url=https%3A%2F%2Fghostinspector.com%2Fabout%2F&psig=AOvVaw2ZHC1jq9MY5lygc0Ouol2C&ust=1686644796127000&source=images&cd=vfe&ved=0CBAQjRxqFwoTCNjts9Gnvf8CFQAAAAAdAAAAABAE))

##Installation
- Copy .github into your local repo 
- Change the branch to the staging branch/the branch you want to watch - any PRs into this branch will trigger the action
- Add GI_SUITE/GI_API_KEY to GitHub settings as a secret key
- Add the URL to startUrl parameter

##How to get the GI_SUITE ID
- Login to GI
- Navigate to the project folder and test suite
- Copy the string ID from the URL when on the suite page

##How to get the GI_TEST ID
- Login to GI
- Navigate to the project folder and test suite
- Click on the test you want to user
- Copy the string ID from the URL when on the test page

##Configure by branch on pull request
```
  pull_request:
    branches:
      - "main"
```

##Run test suites or indicidual tests
Run Suites:
```
  args: suite execute ${{ secrets.GI_SUITE }} \
```

Run an Individual Test
```
  args: test execute ${{ secrets.GI_TEST }} \
```

##Documentation
GI: https://docs.ghostinspector.com/integration/github-actions/ 
