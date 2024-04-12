# scoop-bucket

Manage your scripts using scoop.
Add the scripts you would like to install on scoop to the `scripts` folder. For example:

```pwsh
scripts/hello.ps1
```

And then publish the changes.

Github Workflow will:

1. Detect changes on `scripts` folder.
2. Create an app manifest for you on bucket using the name of the script. For example `hello.ps1` will become `hello.json`.
3. Publish the changes.

Add the bucket to scoop by running

```pwsh
scoop bucket add myscripts <url>
```

To install the new script as an app you can use Scoop by running:

```pwsh
scoop update
scoop install myscripts/hello
```
