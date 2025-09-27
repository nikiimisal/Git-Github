+-------------------+     git add     +-------------------+    git commit    +----------------------+
|  Working Directory |  ------------>  | Staging Area (Index)|  ------------>  | Local Repository (HEAD) |
+-------------------+                  +-------------------+                   +----------------------+
                                                                                  |
                                                                                  | git push
                                                                                  v
                                                                           +----------------------+
                                                                           | Remote Repository    |
                                                                           +----------------------+



Working Directory    →   Staging Area (Index)    →   Local Repository (Commit)    →    Remote Repository (GitHub)
   (असलेली फाईल्स)          (git add)                   (git commit)                    (git push)
                                                                                      
[edit files here]   →   [git add file(s)]    →    [git commit -m "message"]    →    [git push origin main]
