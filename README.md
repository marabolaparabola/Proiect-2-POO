# Proiect-2-POO

- separarea codului din clase în fișiere header (.h sau.hpp) și surse (.cpp)  
      - clasele mici și legate între ele se pot afla în aceeași pereche de fișiere header-sursă 
      - FĂRĂ using namespace std  
- moșteniri: 
      o minim o clasă de bază și 3 clase derivate din aceeași ierarhie 
      o ierarhia trebuie să fie cu bază proprie, nu derivată dintr-o clasă predefinită
- funcții virtuale (pure): 
  o minim o funcție virtuală va fi specifică temei (i.e. nu simple citiri/afișări sau preluate din 
biblioteci i.e. draw/update/render) 
  o funcțiile virtuale vor fi apelate prin pointeri la clasa de bază 
  o pointerii la clasa de bază vor fi atribute ale altei clase, nu doar niște pointeri/referințe în 
main 
- constructori virtuali (clone) - sunt necesari, dar nu se consideră funcții specifice temei 
- apelarea constructorului din clasa de bază din constructori din derivate 
- clasă cu atribut de tip pointer la o clasă de bază cu derivate; aici apelați funcțiile virtuale prin 
pointer de bază, eventual prin interfața non-virtuală din bază  
      - suprascriere cc/op= pentru copieri/atribuiri corecte, copy and swap 
      - dynamic_cast/std::dynamic_pointer_cast pentru downcast cu sens 
      - smart pointers (recomandat)   
- excepții  
      - ierarhie proprie cu baza std::exception sau derivată din std::exception 
      - minim 3 clase pentru erori specifice distincte. Clasele de excepții trebuie să trateze 
      categorii de erori distincte (exemplu de erori echivalente: citire fișiere cu diverse extensii) 
      - utilizare cu sens: de exemplu, throw în constructor, try/catch în main 
- funcții și atribute statice 
- STL  
- cât mai multe const  
- funcții de nivel înalt, de eliminat cât mai mulți getters/setters/funcții low-level
