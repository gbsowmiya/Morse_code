# Morse_code 
#!/bin/bash
index_array1=(.- -... -.-. -.. . ..-. --. .... .. .--- -.- .-.. -- -. --- .--. --.- .-. ... - ..- ...- .-- -..- -.-- --..)
index_array2=(a b c d e f g h i j k l m n o p q r s t u v w x y z )
echo "Enter the morse code file name"
read $file_name
while IFS= read -r line
do
       count=0
while [ $index_array1[$count] -ne $line  ]
do 
       count=$(expr $count + 1 )
done 
       echo "$index_array2[$count]"
 done < "morse.txt"
