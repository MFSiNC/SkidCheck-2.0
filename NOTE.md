Hey, have saw you're recently back on GitHub, glad to see it!

Is it worth me working on a PR that would compress the SkidCheck database? Seems extremely wasteful and even util.compress/LZMA would reduce the size of the reasons massively. I can also host it rather than using GitHub - the previous SkidCheck addon will no longer work as the GitHub repository ID has changed due to your account being recreated.

Also, a backend server which takes a nonce value could easily send just the difference rather than redownloading entire Lua files, happy to do some recreational programming since I've stopped playing Garry's Mod/started working. Again, happy to host the DB and backend server on AWS at my expense to give something back to the GMod community.


```➜  ~/Projects/SkidCheck-2.0/lua/skidcheck git:(main) du -h .
7.5M	.
➜  ~/Projects/SkidCheck-2.0/lua/skidcheck git:(main) xz -c * > skidcheck-db-test.xz
➜  ~/Projects/SkidCheck-2.0/lua/skidcheck git:(main) ✗ ls -alh skidcheck-db-test.xz
-rw-r--r--  1 jack  staff   1.1M  7 Oct 14:14 skidcheck-db-test.xz
➜  ~/Projects/SkidCheck-2.0/lua/skidcheck git:(main) ✗ 
```
Which is approx 14.6% of it's original size without any modifications to the functionality of SkidCheck just by compressing the files all together for an initial download. As for syncing, I have other ideas on how to improve efficiency of that too.
