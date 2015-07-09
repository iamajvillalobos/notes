# Creating a Github repo using terminal

* Go to your project directory
* Replace `USER` with your username, your password will be ask interactively
* Replace `REPO` with your repository name
* Run `curl -u 'USER:PASS' https://api.github.com/user/repos -d '{"name":
  "repo_name"}'
* Add a remote origin `git remote add origin git@github.com:USER/REPO.git`
* Push to origin master `git push origin master`
