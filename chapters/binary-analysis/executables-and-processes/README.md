01:

La challenge-ul 1 doar am dat
gcc -m32 p1 p2 /p4 -o executabil
./executabil


02:
 
Acesta nu am stiut sa il fac dar am vazut la rezovlare cane folosim de LD_LIBRARY_PATH


04:

Doar am dat make si  s-au format 2 executabile caller-no-pie si caller-pie care ambele au acelasi flag
deci presupun ca e corect: SSS_CTF{if_only_it_were_so_simple}

05:

Am dat nm get_message | grep " main" si mi a aparut ca asta e adresa mainului:08049211 T main 
Apoi am dat nm get_message | grep " _start" si am gasit ca asta e adresa _start: 08049090 T _start
Dar totusi dupa nu am stiut cum sa le scimb asa ca m-am oprit aici si am intrat in ghidra si am gasit 
ca flagul este ahCeshuiKuch7Ah7ehahhahha0du2Oof

06:

Aici am folositt ghidra si am observat ca main-ul are doar un printf si return..deci am folosit xxd pe executabil
si am observat faptul ca acesta defapt are un executabil in executabil(a fost de ajutor si numele
matrioshka) 
si apoi am folosit dd if=matryoshka of=out.bin bs=1 skip=$((0x2020)) si dupa in out.bin avem flagul 
xorat cu \x7fELF si da: SSS_CTF{in_space_no_one_can_hear_you_belch}

07:
Nu am stiut sa il fac
