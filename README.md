# shredding
Script which can able to do file shredding on windows and the file will not be recovered. We can create and delete the file multiple times through the script minimum input required 100 times.

@ECHO OFF 
SET /P Input=Please Enter the Number of times you want file to be created and deleted: 
echo %Input%
FOR /L %%X IN (1,1,%Input%) DO (
echo "Hello">C:\Desktop\TESTNEW.txt
echo "%%X File Created"
del C:\Desktop\TESTNEW.txt
echo "%%X File Deleted"
)
echo "%Input% times file created and deleted"
pause
