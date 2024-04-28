# Practica-Collections

En aquest readme trobarem les respostes a diferents cuestions relacionades amb el codi i l'implementacio de diferents mecanismes sobre altres.

- Ens demanen treballar amb la **Collection List**, sabem que tant Stack com a Vector funcionen correctament per a processos multithreading però en principi no ens cal dins del nostre context, per tant valoreu, escolliu i justifiqueu quin dels altres dos casos faríeu servir i a on?
	> En aquest projcte el mes adecuat es treballar amb "arraylist" ja que a l'hora d'accedir a productes especifics es mes practic.
	I trobarem els arraylist implementats en les diferents llistes dels diferents productes:
	>
	>"public **Compra**() {  
   **llista_ali** = new ArrayList<Alimentacio>();  
  **llista_elec** = new ArrayList<Electronica>();  
  **llista_textil** = new ArrayList<Textil>();  
} "
---
- Per a poder-lo integrar amb la impressió del carret de la compra d’altres aplicacions ja desplegades, ens demanen treballar amb la Collection Map, i ens diuen que serà necessari treballar amb mètodes propis com ara containsKey o containsValue (valoreu quin dels dos casos us serà necessari). El recorregut de les dades s’haurà de fer amb lambda expressions.
	> En aquest projcte el mes adecuat es treballar amb "containsKey" ja que ens permet cercar les dades de manera mes rapida i eficient ja que a diferencie del "containsValue" no necessitem recorre tot el contingut fins trobar el producte esperat ja que treballem sobre "keys" per tant agafarem directament el producte de la llista o "Map".
	Implementacio de "containsKey" i "Map" al projecte:
	>
	>"public void **printCarret**() {  
   Map<String,Integer> llista = new **HashMap**<>();  
   > 
  >**for**(Alimentacio a : **llista_ali**) {  
      **if**(!llista.containsKey(a.getCodibarres()))     llista.put(a.getCodibarres(),1);  
 **else** llista.put(a.getCodibarres(),llista.get(a.getCodibarres()) + 1);  
  }  
   llista.forEach((k,v)-> System.out.println(getNomProducte(k) + " -> " + (Integer) v));  
  llista.clear(); "
...
---
