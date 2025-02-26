# classified

## Instructions on how to update the parent repository

Updating a submodule and then reflecting those updates in the parent repository.

### Updating the Submodule

1. **Navigate to the Submodule Directory**
   - Change into the submodule's directory from the root of the parent repository.
     ```shell
     cd path/to/submodule
     ```

2. **Check Out the Desired Branch**
   - Ensure you're on the branch you want to update.
     ```shell
     git checkout main  # Or another branch you're updating
     ```

3. **Pull the Latest Changes**
   - Fetch and merge the latest changes for the branch from the remote.
     ```shell
     git pull origin main
     ```

### Committing Changes in the Submodule to the Parent Repository

5. **Stage the Submodule Changes**
   - Add the submodule changes to be tracked by the parent repository. This action updates the parent to point to the latest commit of the submodule.
     ```shell
     git add .
     ```

6. **Commit the Submodule Changes**
   - Commit the update in the parent repository to record the change in the submodule reference.
     ```shell
     git commit -m "Update submodule to latest commit"
     git push
     ```

### Pushing the Updates to the Parent Repository

7. **Push the Changes to the Parent Repository**
   - Push the updates from the parent repository to the remote. This ensures that the parent repository correctly references the updated state of the submodule.
     ```shell
     cd ..
     git checkout update-submodule-branch
     git add .
     git commit -m "message"
     git push
     ```
8. **Create pull request and merge changes**
   - Visit GitHub website, create the pull request and merge the changes.