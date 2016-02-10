# really-long
I just wanted to see how the UI would handle a branch with the maximum amount of characters for HFS Plus.

I'm using the branch name:
```
abcdefghijklmnopqrstuvwxyzabcdefghijklmnopqrstuvwxyzabcdefghijklmnopqrstuvwxyzabcdefghijklmnopqrstuvwxyzabcdefghijklmnopqrstuvwxyzabcdefghijklmnopqrstuvwxyzabcdefghijklmnopqrstuvwxyzabcdefghijklmnopqrstuvwxyzabcdefghijklmnopqrstuvwxyzabcdefghijklmnopqrstu
```

---

In order to get the file name in under the 255 character limit, we need to subtract the last 5 letters so that
git can create the ```.lock``` file that's apparently associated with creating a branch. Additionally, this
branch name is several characters shorter as I was unable to reliably switch to it on OSX 10.11.2 -- upon
attempting a checkout, I'd simply check out this branch name regardless of the given string. The full branch
name was visible as a separate branch when I did ```git branch -v``` but I was simply unable to check it out.
