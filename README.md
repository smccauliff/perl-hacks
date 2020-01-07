# perl-hacks
A place to store perl one liners

# Get a line out of the diceware file.
perl -e ' open(R, "/dev/urandom"); $n=""; for ($i=0; $i < 5; $i++) {  read(R, $raw, 4);  $x = unpack("s", $raw); $d = $x % 6 + 1; $n .= $d; } print `grep $n diceware.wordlist.asc.txt`; ' 
