#Github Terminal Tricks
- installation
  ```
  sudo apt install gh
  ```
- authentication
  ```
  gh auth login
  ```
- see your repos
  ```
  gh repo list
  ```
- clone repo
  ```
  gh repo clone <username>/reponame
  ```
- delete repo
  if inside the repo
  ```
  gh repo delete --confirm 
  ```
  if outside the repo
  ```
  gh repo delete username/reponame -- confirm
  ```
