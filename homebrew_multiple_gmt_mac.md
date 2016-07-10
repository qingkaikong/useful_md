## Multiple GMT versions with Homebrew

The following is quick summary how you can install multiple versions of GMT on mac using homebrew, and swtich back and forth between different versions. 

Install current GMT:  
 
```mardown
brew install gmt
```

Install older gmt version:  

```markdown   
brew search gmt
brew install homebrew/science/gmt4
```

Then to switch to the old version

```markdown
# Unlink the current version
brew unlink gmt

# Check the old version
ls /usr/local/Cellar/gmt4 # -> 4.5.14

# link the old version
brew switch gmt4 4.5.14
```

Switch back to the new version

```markdown
# Unlink the old version
brew unlink gmt4

# Check the new version
ls /usr/local/Cellar/gmt # -> 5.2.1

# link the new version
brew switch gmt 5.2.1
```