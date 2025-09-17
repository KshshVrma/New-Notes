[[Git]]

git pull is noramally a combination of 2 git commands which are git fetch and gti merge.

git fetch check the remoter repository for  any new branch additions, etc and fetches the latest commits which git merge add those change to the local repository which allowes peopele to work together.

some ide's provide additionaly features so for example git update project is normally not a git command but a featrue from the gui wh9ich allows the user to either enable the option to perform the normal git pull which is nothing but the combination of git fetch and git pull however if we make use of the other otption made availble by intellij that is fetch + rebase in thast ase:

it runs th git fetch as usuall but however istead of runnng the git merge which combines te commits history and makes everything non linear and even messier depending on the situaltions, however the git rebase moves all the commits on top the the branch from which we are rebasing so for example if in the current rep we have made a few commits then after putting the git rebase command then the commits will be moved at then end of the commit history and thre branch history will look clean lineary history which mean no branching out and easeier to debug , however this losses the timline of acutall event and incase of any actuall discrepency then it makes itto take longerto find which commit actually cased the issue in some scenarios.