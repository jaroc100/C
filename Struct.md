- Structs sind wie Konstruktoren in Java
```C
struct Student{
	char name[50];
	char major[50];
	int age;
	double gpa;
};

int main () {
	
	struct Student student1;
	student1.age = 22;
	student1.gpa = 3.2;
	strcpy(student1.name, "Jim"); //Stringcopy um String nutzen zu können.
	strcpy(student1.major, "Business");
	
	printf("%f", student1.gpa);
	
	return 0;
}
```