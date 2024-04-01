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

4. **Navigate Back to the Parent Repository**
   - Return to the root directory of the parent repository.
     ```shell
     cd ../..
     ```

5. **Stage the Submodule Changes**
   - Add the submodule changes to be tracked by the parent repository. This action updates the parent to point to the latest commit of the submodule.
     ```shell
     git add path/to/submodule
     ```

6. **Commit the Submodule Changes in the Parent Repository**
   - Commit the update in the parent repository to record the change in the submodule reference.
     ```shell
     git commit -m "Update submodule to latest commit"
     ```

### Pushing the Updates

7. **Push the Changes to the Parent Repository**
   - Push the updates from the parent repository to the remote. This ensures that the parent repository correctly references the updated state of the submodule.
     ```shell
     git push origin main
     ```

### Note
- If the submodule itself has changes that need to be committed and pushed to its respective remote repository, do this before updating the parent repository. This involves committing any changes within the submodule (step 1 to 3) and pushing those changes to its remote (replacing step 3's `git pull` with `git push` after committing any changes).

- Always ensure you're on the correct branch in both the submodule and the parent repository before making or pulling changes. This prevents unexpected behavior and ensures changes are tracked correctly.