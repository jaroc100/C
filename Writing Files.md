Man kann verschieden Files erstellen und schreiben in C. Dazu muss man ein `FILE *` erstellen und z.B sagen, dass eine Datei geöffnet wird mit `fopen(Filename, ausführung);`. Die ausführung ist ähnlich wie in RDB, `"W"` ist schreiben, `"R"` ist lesen und `"A"` ist append (hinzufügen).`FILE` kann zum einfachen verständnis als Datentyp angesehen werden. 
```C
int main () {
	
	FILE * fpointer = fopen("employees.txt", "w"); //textfile mit dem namen employees wird erstellt.
	
	fprintf(fpointer, "Jim, Salesman\n Pam, Receptionist"); //File wird mit text gefüllt.
	
	fclose(fpointer); //File wird geschlossen.
	return 0;
}
```
Wenn man hier einen neuen `fprintf` befehl einfügt, dann wird die Datei **überschrieben**, da wir nur `"w"` bei `fopen()` benutzt haben.
```C
int main () {
	
	FILE * fpointer = fopen("employees.txt", "a");
	
	fprintf(fpointer, "\n Kelly, Customer Service"); //Kelly wird hinzugefügt
	
	fclose(fpointer); //File wird geschlossen.
	return 0;
}
```
In diesem Beispiel würde die Datei **nicht** überschrieben werden. Kelly wird in der emplyees Textdatei **hinzugefügt**.

---

## read

```C
int main () {
	
	char line[255];
	FILE * fpointer = fopen("employees.txt", "r");
	
	fgets(line, 255, fpointer); //erste Zeile wird gespeichert und der Pointer wird um eine stelle verschoben
	printf("%s", line) // erste Zeile von employees wird ausgegeben
	
	fclose(fpointer); //File wird geschlossen.
	return 0;
}
```

```C
int main () {
	
	char line[255];
	FILE * fpointer = fopen("employees.txt", "r");
	
	fgets(line, 255, fpointer); //erste Zeile wird gespeichert und der Pointer wird um eine stelle verschoben
	fgets(line, 255, fpointer); //zweite Zeile wird gespeichert und der Pointer wird um eine stelle verschoben
	printf("%s", line) // zweite Zeile von employees wird ausgegeben
	
	fclose(fpointer); //File wird geschlossen.
	return 0;
}
```
`fgets()` wird benutzt um ein Zeile der Datei zu lesen. in `fgets()` wird zuerst geschrieben, wo das gelesene abgespeichert werden soll, dann die max. größe (meistens gleich mit der ersten Nummer von `fgets()`), als letztes muss angegeben werden, was gelesen werden soll.
