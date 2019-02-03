# GIt-Command
######Basic Commands of Git
<HR>
<html>

<font color="white" face="Lucida Handwriting">
<h1 align="center">BASIC CODES OF GIT BASH </h1>
</font>

<HR>

[#####To intiliaze the the Local Repo](#To-intiliaze-the-the-Local-Repo)

<p>1:) git init  #to initialize the .git track folder or to start tracking</p> 
<hr>

<p>2:) git status #use to check the status of the current Branch...</p>

<p>3:) git add #is use for staging the files. </p>
         
   <p>&emsp;&emsp;&emsp;#*Before commiting Staging is necessary*</p>

<p>4:) git add . #Staging all the file exist in Repo but only the Tracked files. </p>

<p>5:) git add *.extension #for particular file.</p>
 
<p>6:) git commit ('i' commit 'esc;wq') #use to commiting but it is complex.</p>

<p>7:) git commit -m'commit' #use to commiting and easyway.</p>

<p>8:) git log #To check the commit history.</p>

<p>9:) touch filename.extension #used to create a new file.</p>

<p>10:) touch .gitignore #for creating a ignor file. </p>

<p>11:) git branch BranchName #use to create a new branch of Repo.</p>

<p>12:) git checkout BranchName #use to change branch.</p>

<p>13:) git merge Branch/sourceName  #use command in Destiny where to merge the Branch.</p>

<p>14:) git commit -a -m'commit'  #use to skip the stageing step.</p>

<p>15:) git stash #unfinished changes that can be reapply any time.</p>

<p>16:) git stash apply #for applying the changes.</p>

<p>17:) git clone URL #use to cloneing the remote Repo in the local Repo.</p>

<p>18:) git remote #to check the remote repo in the local. </p>

<p>19:) git remote -v #use to check the URL.</p>

<p>20:) git fetch origin #use to fetch the data from Remote Repo But not merge it we have to merge manually.</p>

<p>21:) git pull origin #use to same as fetching the data and it merge the data automatically.  </p>

<p>22:) git push origin master #use to pushing the data from local Repo to Remote Repo.</p>


create a new repository on the command line
echo "# Menu-Project" >> README.md
git init
git add README.md
git commit -m "first commit"
git remote add origin https://github.com/Imsatis/Menu-Project.git
git push -u origin master

push an existing repository from the command line
git remote add origin https://github.com/Imsatis/Menu-Project.git
git push -u origin master

</body>
</html>
