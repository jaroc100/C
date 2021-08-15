## Strings / Chars
- es gibt **"keine"** Strings. 
	- Strings werden als `char` abgespeichert und nach dem Variablennamen mit einem `[]` beendet.
```C
char buchstabe = 'A';
char name[] = "Dennis";
```

## Zahlen
- wie gewohnt aus java.
```C
int age = 69;
double weight = 70,34;
float favNum  = 3,14;
```

## Print Befehle
- mit `\n` wird die Zeile beendet und in die nächste gesprungen.
- `%s` wird benutzt um einen anderen String in den printbefehl einzugeben, `%c bei einem char`.
```C
printf("There once was a man named %s\n", name);
```
- `%d` funktionniert genau so wie `%s` nur mit integern.
```C
printf("There once was a man named %s\n", name);

printf("he was %d years old.\n", age);

printf("he was %d years old and his name was %s.\n", age, name);
```
- Dezimalzahlen werden mit `%f ausgegeben`.
```C
printf("There once was a man named %s\n", name);

printf("he was %d years old.\n", age);

printf("he was %d years old and his name was %s.\n", age, name);

printf("his favourite number was %f.\n", favNum);
```
