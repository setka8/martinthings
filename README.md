# martinthings
Lahe
WOW so cool..!!!!:
#!/bin/bash
#Special variables
echo $1 #Prints the first variable

#Create folder, 
mkdir $2
touch $2/test.txt
echo Folder $2 created
cd $2
ls -l

#$0 name of the script
echo $0
#$# how many args
echo $#
#$@ all passed args
echo $@
#System variables
sleep 3

echo $USER
echo $HOSTNAME
echo $SECONDS #number of secs since script started
echo $RANDOM
echo $LINENO #current line number in the script
#this is awesome..!
#!/bin/bash
#Kommand, mis küsib kasutajalt andmed ja kohe salvestab need muutuja sisse
read -p "Mis nimega kausta kontrollin? " dir 
#echo $dir 
if [ -d $dir ]
then
echo "Selline kaust on süsteemis juba olemas"
else
echo "Kaust nimega $dir on loodud."
mkdir $dir
fi
echo "Nüüd saame tõsta loodud kausta sisse mingi faili"
#
#
#
#
#
read -p "Kas soovid mingi faili kausta sisse liigutada? (1/0) " check
if [ $check -eq 1 ]
then
movefile $dir 
else
echo "Bye then!"
exit 0
fi


#Loome eraldi funktsiooni faili liigutamise loogikaga
function moveFile () {
read -p "Mis faili? " file
echo $file
if mv $file $dir 
then
echo "Fail on kausta sisse liigutatud"
else
echo "Midagi läks valesti"
fi
}

moveFileCreateIfNotExists () {
read -p "Mis faili? " file
echo $file

if mv $file $1
them
echo "Fail on kausta sisse liigutatud"
else
echo "Midagi läks valesti"
fi
}
