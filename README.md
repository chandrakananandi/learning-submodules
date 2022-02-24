# learning-submodules

## Basics

Git submodules are hard to understand. I made this repo and [another one](https://github.com/chandrakananandi/submodule) to learn the basics. Here's what you do to get started.

- First make two repos, one is the "parent" and the other is the "submodule". The latter will be used from inside the former.
- Clone the parent repo and then add the submodule to it by running 
```
git submodule add git@github.com:chandrakananandi/submodule.git
```

- Then commit that from the parent directory. This will add the submodule to the parent. Push the changes. Now you have a submodule inside your parent repo!
- Now you may want to edit the submodule. To do that, navigate to the submodule by running `cd submodule`.
- Make a change in say the `README.md` and commit and push that.
- If you go to the repo for the submodule, you will find this commit.
- Now you also want to make sure the parent repo has been updated to use this change in the submodule.
- For that, navigate back up to the parent repo's directory (in this case, `learning-submodules`) and see the diff using `git status`.
- You will see that the `submodule` has changed.
- Simply commit and push like you normally do from the parent repo's directory.

## Additional notes

- One thing you may often find yourself doing, especially if you clone an existing project with submodules is recursively cloning the submodules. For example:

```
git clone --recurse-submodules git@github.com:chandrakananandi/learning-submodules.git
```
