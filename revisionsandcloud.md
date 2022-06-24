# Revisions and the Cloud
**6/22/22** 
### Today, in Code 102 we learned about Git how to use it to transfer repositories from GitHub to our local database and vice versa. 

---

**Git** is a Distrubuted Version Control (allows clients to create mirrored repositories) that stores data in a file system made up of snapshots.
- **Snapshots**: When you change your project and save that version of it, Git creates a snapshot - called a commit - and stores a reference to it. 
- **Local operations**: Git mostly relies on local operations since most necessary information can be found in local resources. This allows expediency becausse a project's history is stored locally rather than having to be retrieved from the server. This allows you to continue working on the project even when offline. 
- **Tracking changes**: Every single change made to a file is tracked by Git. It will always detect file corruption or loss of information in transit. 
- **Loss of data**: Git prevents loss data and makes it extremely difficult for a commit of your file to be lost. 
- **States**: Files in Git reside in three main stages: Commited, modified, and staged. 
- **Commited**: Data securely stored in local database. 
- **Modified**: File has been changed but not commited to database. 
- **Staged**: Flagged a file's changed version to be commited into next snapshot. 

**Local Repository Structure**
<br> Local Git respository has three components:
1. Working Directory: Actual files reside here
2. Index: Area used for staging
3. Head: Points to the most recent commit 

**Saving Changes**
<br>All files in a checked out (or working) copy of a project file are either tracked or untracked. 
- **Tracked**: Can be modified, unmodified, or staged; a part of most recent file snapshot.
- **Untracked**: Not in last snapshot and do not currently reside in staging area. 
<br><br>
# A-C-P (Add, Commit, Push)

| **Command**            |          **Function** |
| :---: | :---: |
| `git clone {url}` | Clones GitHub repositories. |
| `git add` | Adds individual files changed to be tracked by Git. |
| `git add .` | Adds all the files changed to be tracked by Git. |
| `git commit -m "message here"` | Commits changes. |
| `git push origin main` | Send changes to GitHub. |
| `git status`| Determines status of file. |
| `touch file.html` | Creates a new html file name "File.html". |
| `mkdir myFolder` | Creates a new folder named "myFolder". |
| `cp file.html . ./myFolder`| Copies the file "File.html" into the folder <br>"myFolder" that is located one directory back. |
| `mv file.html . ./myFolder` | Move the file "File.html" into the folder <br> "myFolder" that is located one directory back. |
| `clear` | Clears terminal. |
| `cd ~` | Navigate to HOME directory. |
| `program name --version` | View lastest version of installed program. |

[Back to main page](README.md)