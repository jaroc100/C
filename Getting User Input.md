- Bespiel Altersabfrage:
```C
int age; // age bekommt absichtlich keinen wert.
printf("Enter your age: "); // abfrage mach alter an User.
scanf("%d", &age); // user gibt Alter an und es wird hier gespeichert.
printf("Your are %d years old", age); // ausgabe des eingegebenen alters.
```
Um den User nach seinem Alter zu fragen muss eine Varaible erstellt werden, die keinen Wert zugewiesen bekommt, da dieser später mit `scanf()` einen Wert von dem User bekommt. Damit man mit Scan einen Wert von dem User speichern kann muss ein `&` vor den Variablennamen geschrieben werden. `&age` ist ein [[Pointer]].
- Bei Strings muss in den Klammern definiert werden wie groß der String sein darf:
```C
char name[20]; // maximal 19 chars.
printf("Enter your name: ");
scanf("%d", &name);
printf("Your name is %s", name);
```
- Bei `scanf()` wird alles eingegeben **nach** einem Leerzeichen nicht betrachtet !
```C
char name[20]; // maximal 19 chars.
printf("Enter your name: ");
scanf("%d", &name);	// <-- User gibt ein: John Smith.
printf("Your name is %s", name);
// Ausgabe --> Your name is John.
```
- `fgets()` wird benutzt um mehrer Wörter vom User nutzen zu können.
```C
char name[20];
printf("Enter your name: ");
fgets(name, 20, stdin);	// stdin = Standard Input.
printf("Your name is %s", name);
// Ausgabe --> Your name is John Smith.
```
- Wenn `fgets()` benutzt wird, dann wird nach der Benutzung der Variable ein Zeilenumbruch gemacht. 
```C
char name[20];
printf("Enter your name: ");
fgets(name, 20, stdin);	// <-- Eingabe: John Smith.
printf("Your name is %s WOOOW", name);
/* Ausgabe --> 	Your name is John Smith
		   -->	WOOW
*/
```
