
Aloitin tehtävän avaamalla visual studio code sovelluksen. Loin tiedoston nimeltä main.cpp ja lisäsin ohjelman aloituspisteen. Ohjelmassa on yksi funktio, joka lisää kaksi kokonaislukua ja palauttaa uuden arvon takaisin. Tämän jälkeen käänsin ohjelman Microsoftin compiler options työkalulla, joka kääntää ja yhdistää objektitiedostot yhteen suoritettavaan tiedostoon. Ohjelma lisäsi ohjelman nimeltä main.exe kansioon. Binaarin analyysia varten, latasin Ghidra ohjelman GitHub-palvelusta ja loin uuden projektin. 


int add(int a, int b)
{
  return a + b;
}
int main()
{
  int numero = 100;
  int testi = 3000;
  add(numero, testi);
}
