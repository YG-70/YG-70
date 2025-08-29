## Lab 01

- Name:Yoel Tareke
- Email:

## Part 1 - GitHub Profile

1. [YG-70](https://github.com/YG-70/YG-70/blob/main/Lab01.md)

## Part 2 - Research

| Windows | Linux / Mac | Action |
| ---     | ---         | ---    |
| help    | man         |Gives you a few information on how to get help  |
| Get-Location | pwd    | Tells you where you are currently at       |
| Get-ChildItem | ls    | Gives you a list of sources that you currently have   |
| mkdir   | mkdir       | Allows you to make a directory       |
| Set-Location | cd     | Allows you to change your location       |
| New-Item | touch      | Allows you to creat a new file       |
| Move-Item | mv        | allows you to move files and folders       |
| Copy-Item | cp        | allows you to copy files and folders        |
| Remove-Item | rm      | Allows you to remove files and folders       |
| notepad.exe | vim     | allows to write into your file        |

## Part 3 - Command Line Navigation

My OS is:
- [x] Windows
- [] Linux
- [] Mac

My Command Line Shell is: Powershell

### Navigating My OS on the Command Line

1. Full / absolute path to your user's home directory:Get-Location
2. Create a directory named `DirA`:mkdir DirA
3. Create a directory named `Dir B`:mkdir "Dir B"
4. Go into `DirA`:Set-Location DirA
5. Go into `Dir B` from `DirA`:set-location 'C:\Users\yoelt\Dir B'
6. Return to your user's home directory: Set-Location ..
7. Create a file named `test.txt`:New-Item test.txt
8. Move the file named `test.txt` into `DirA`:Move-Item test.txt DirA
9. Contents of `test.txt`: cat test.txt
```
Hi there
```
10. Make a copy of `test.txt` named `copy.txt` in `DirA`:Copy-Item "C:\Users\yoelt\DirA\test.txt" "C:\Users\yoelt\DirA\copy.txt"
11. View the contents of `DirA`: ls DirA
12. Make a copy of `test.txt` in `Dir B` named `fodder.txt`:Copy-Item "C:\Users\yoelt\DirA\test.txt" "C:\Users\yoelt\Dir B\fodder.txt" 
13. Delete / remove both `fodder.txt` AND `Dir B`:Remove-Item "fodder.txt", "Dir B"

## Citations

To add citations, provide the site and a summary of what it assisted you with.  If generative AI was used, include which generative AI system was used and what prompt(s) you fed it.



