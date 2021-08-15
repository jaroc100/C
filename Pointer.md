- Ein Pointer ist eine [[Memory Address]]
- Kann als Datentyp gesehen werden (zum leichteren Verständnis)
	- Also: Pointer sind Memory Addresses, genauso wie double eine Kommazahl ist, oder int eine Natürliche Zahl. Man kann also Pointer Variablen erstellen!
- um eine Pointer Variable zu erstellen muss erst eine "richtige" Variable davor erstellt worden sein, wie im Beispiel.
	- dazu wird die Variable mit einem `*` gekennzeichnet. 
```C
int age = 30;
int * pAge = &age; //<-- Pointer variable speichert die memory address der Age variable
double gpa = 3.4;
double * pGpa = &gpa;
char grade = 'A';
char * pGrade = &grade;


printf("age's memory address: %p", &age); //gibt memory address von age aus.
printf("age's memory address: %p", pAge); //macht das gleiche.
```

---

## Dereferencing Pointers
mit Dereferencing kann man die Memory Address nehmen und schauen, was in diesem Pointer gespeichert ist.
```C
int age = 30;
int * pAge = &age;

printf("%d", *pAge); //gibt aus: 30
printf("%d", &*pAge); //gibt Memory Adress aus.
printf("%d", *&*pAge); //gibt aus: 30
```