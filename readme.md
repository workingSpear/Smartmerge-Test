# SETUP
> note: make sure you can see hidden files, search `show hidden files [your OS]`
- after cloning the repo, open the `.git\config` file in any text editor, notepad works, and copy paste the following at the bottom and change the file path to be the file path of UnityYAMLMerge.exe
```
 [merge]
    tool = unityyamlmerge
[mergetool "unityyamlmerge"]
    trustExitCode = false
    cmd = '[Path to UnityYAMLMerge]' merge -p "$BASE" "$REMOTE" "$LOCAL" "$MERGED"
```
 - The exe should be with your unity install and is commonly found in `C:/Program Files/Unity/Hub/Editor/2022.3.5f1/Editor/Data/Tools/UnityYAMLMerge.exe` for windows although make sure to check that this is the correct file path

# USAGE
- If a merge conflict arises due to two people working in the same scene then simply merge your branch to main.
- This will cause an error, however, run `git mergetool` afterwords and if you followed the setup correctly, it should take care of any conflicts within the `[scene name].unity` and other miscellaneous associated files.
