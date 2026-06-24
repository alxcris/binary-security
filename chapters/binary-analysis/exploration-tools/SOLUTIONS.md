
# SOLUTIONS

07 perfect-answer:

Am folosit strance si am observat ca la 42 se schimba ceea ce se cere asa ca l-am redirectionat in standard output

./perfect-answer 42>&1
Generating the 2nd flag
LCBIjOkF\Zv
Generated! Can you guess it this time?
LCBIjOkF\Zv
L33t $killz bro!



08 lots-of-strings:

Am folosit nm pe executabil si am obervat ca avem o variabila in .data numita password.Apoi am folosit gdb, am dat run si am printat ce se afla la adresa variabilei password..si ne-a afisat _34qx9RlP2BWtEIJ.Apoi am rulat programul, am pus parola si am primit congrats!

10 hidden:

Am folosit strace pe executabil si am vazut ca executabilul cauta /tmp/graybox1234.
Asa ca l-am creat, am facut un symbolic link cu ln pentru un fisier in /tmp/salvare_flag.In alt terminal am rulat executabilul si inainte sa bag flagul am dat cat la /tmp/salvare_flag si ne-a afisat flagul.Apoi l-am bagat in input si a afisat Congrats! Hostages released.
