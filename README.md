This is a reproduction for https://github.com/dart-lang/sdk/issues/54957

Open the project in vscode:
```bash
code .
```

Click on pubspec.yaml and save it to make sure the dependencies are installed.
`dart pub get` probably works from the command line too.

Make sure all editors are closed.

Notice how the problems window is empty.

Use right-click to delete thd file "test/bar.dart".

Notice how the problems window now shows a single problem.

```
The name 'QueryParam' isn't a type, so it can't be used as a type argument.
Try correcting the name to an existing type, or defining a type named 'QueryParam'.
```

Click on the problem to open the file.  Notice how it goes away as soon as you save/close the file.

I believe this a problem with part commands and the way the analysis server does refreshes.