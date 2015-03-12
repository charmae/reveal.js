
**For Gatekeepers:**


1. Clone the main repo https://github.com/xxxx/video-player.git. <br>
   `git clone https://github.com/xxxx/video-player.git` <br>

2. Add individual remote repository of developers<br>
   `git remote add charmae-stream https://github.com/charmae/video-player.git` <br>
   `git remote add panut-stream https://github.com/nakautot/video-player.git` <br>
   `git remote add yami-stream https://github.com/yamii/video-player.git` <br>
   `git remote add chad-stream https://github.com/chaddoy/video-player.git` <br>
   `git remote add jes-stream https://github.com/iammary/video-player.git` <br>
   `git remote add shinji-stream https://github.com/shinjiescorido/video-player.git` <br><br>
   `git remote add local-stream pi@192.168.42.1:/media/zubu/tz/video-player` <br>
 

3. Create individual branches for each dev for code testing before pushing to upstream. <br>
   ` git checkout -b charmae-dev charmae-stream/dev ` <br>
   ` git checkout -b panut-dev panut-stream/dev ` <br>
   ` git checkout -b yami-dev yami-stream/dev ` <br>
    ` git checkout -b chad-dev chad-stream/dev ` <br>
    ` git checkout -b jes-dev jes-stream/dev ` <br>
    ` git checkout -b shinji-dev shinji-stream/dev ` <br>


4. Process pull request. <br>
   
   a.  Fetch changes from developers remote repository.<br>
      `git fetch charmae-stream`<br>
   b. Checkout developer’s branch<br>
   `git checkout charmae-dev`<br>
   c. Pull changes from developers remote repository<br>
   `git pull charmae-stream dev`<br>
   d. Rebase developers branch. If there are conflicts, proceed to (A).<br>
   `git pull —rebase origin dev`<br>
   e. Test environment <br>
       check coding convention <br>
       check number of commits( should only be 1 commit)<br>
       check commit message format. <br>
   f. if Test environment and coding convention is ok. <br>
         Merge developers changes to main dev branch.<br>
   `git checkout dev`<br>
   `git merge charmae-dev`<br>
    g. Push to dev branch.<br>
   `git push origin dev`<br>

(A). Merge confilicts.<br>
  1. Inform developer to pull the latest changes. <br>
  2. To reset changes from developers branch.<br>
       a.  `git reset --hard charmae-stream/dev`<br>
       b.  `git clean -f`<br>

(B). Change last commit message.<br>
       `git commit --amend -m “new-commit-message-here”`<br>

(C). Combine multiple commits <br>
    `git rebase -i HEAD~n`<br>
    a. pick first in the list<br>
    b. squash others.<br>
