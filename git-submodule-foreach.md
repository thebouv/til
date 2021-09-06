# Update all git submodules

I needed to update all the submodules to the most recent main versions. And that's easy to do if you only have a couple, and I did, but I wanted to know the best way.

```sh
git submodule foreach git pull
```

The `foreach` bit for submodules is pretty cool.

And per [the documentation]() you can even create a great unified diff for your main project and its submodules:

```sh
git diff; git submodule foreach 'git diff'
```