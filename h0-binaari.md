# h0 - Compile and analyze

Aloitin tehtävän avaamalla visual studio code sovelluksen. Loin tiedoston nimeltä main.cpp ja lisäsin ohjelman aloituspisteen. Ohjelmassa on yksi funktio, joka lisää kaksi kokonaislukua ja palauttaa uuden kokonaisluvun takaisin. Tämän jälkeen suoritin Microsoftin compiler options työkalun, joka kääntää ja yhdistää objektitiedostot yhteen suoritettavaan tiedostoon. Ohjelma loi tiedoston nimeltä main.exe kansioon. Analysoin binaari tiedostoa komennolla dumpbin. Komento dumpbin /headers tuottaa suoritettavan tiedoston ylätunnisteet, jotka sisältävät tietoa ohjelman konekoodin ja datan sijainnista sekä niiden ominaisuuksista. 

Alla on esimerkki syötteestä:

SECTION HEADER #1
.textbss name
   10000 virtual size
    1000 virtual address (0000000140001000 to 0000000140010FFF)
       0 size of raw data
       0 file pointer to raw data
       0 file pointer to relocation table
       0 file pointer to line numbers
       0 number of relocations
       0 number of line numbers
E00000A0 flags
         Code
         Uninitialized Data
         Execute Read Write

SECTION HEADER #2
   .text name
    7A1A virtual size
   11000 virtual address (0000000140011000 to 0000000140018A19)
    7C00 size of raw data
     400 file pointer to raw data (00000400 to 00007FFF)
       0 file pointer to relocation table
       0 file pointer to line numbers
       0 number of relocations
       0 number of line numbers
60000020 flags
         Code
         Execute Read


int add(int a, int b)
{
  return a + b;
}
 
int main()
 {
   int numero = 100;
   int testi = 3000;
   int vastaus = add(numero, testi);
 }
 
## Reference
https://en.wikipedia.org/wiki/Portable_Executable

https://learn.microsoft.com/fi-fi/cpp/build/reference/dumpbin-command-line?view=msvc-170

 

