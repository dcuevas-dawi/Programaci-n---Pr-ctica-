# Programacion   Practica1
## Resolución del exámen de la primera evaluación del grupo presencial.

### Bloque 1

### Ejercicio 1

~~~
//Función para convertir un número decimal a binario.

void decimalBinario(int n){
	while(n != 0){
		print(n % 2)
		n = n / 2
	}
}
~~~

### Ejercicio 2

~~~
//Función para convertir un número de binario a decimal.

void binarioDecimal(long n){
	int i, n2, suma = 0
	while(n != 0){
		n2 = n % 10
		n = n / 10
		suma = suma + (n2*2^i)
		i++
	}
	print(suma)
}
~~~

### Ejercicio 3

~~~
//Función a la que le damos un número y devuelve true si es par y false si es impar.

boolean esPar(int n){
	if(n % 2 == 0){
		return true
	} else {
		return false
	}
}
~~~

### Ejercicio 4

~~~
//Función que nos muestra todos los numeros pares desde 0 (incluido) hasta n (incluido, si es par).

void primerosNumeroPrimos(int n){
	for (int i = 0; i <= n; i = i + 2){
		print(i)
	}
}
~~~

### Ejercicio 5

~~~
//Función que contiene un menú para llamar a una de las funciones de los anteriores 4 ejercicios.

 int menu(){
	print(1.Decimal a binario)
	print(2.Binario a decimal)
	print(3.¿Es par?)
	print(4.Calcula los pares de 0 a n)
	print(0.Salir)
	return (input)
}
~~~

### Ejercicio 6

~~~
//Main que contendrá las 5 funciones de los ejercicios anteriores e interactuar entre ellas.

main(){
	//Declaramos la variable decision, que variará según la elección del usuario
	int decision = -1
	//Hacemos un bucle para poder repetir el menú e interacturar con todas las funciones.
	while(decision == -1){
		decision = menu()
		/Condicional para llamar a decimalBinario()
		if(decision == 1){
			print(Has escogido la opcion + decision)
			print(¿Qué número quieres pasar de decimal a binario?)
			int n = input
			decimalBinario(n)
			decision = -1
		}
		//Condicional para llamar a binarioDecimal()
		if(decision == 2){
			print(Has escogido la opcion + decision)
			print(¿Qué número quieres pasar de binario a decimal?)
			long n = input
			binarioDecimal(n)
			decision = -1
		}
		//Condicional para llamar a la función esPar()
		if(decision == 3){
			print(Has escogido la opcion + decision)
			print(¿Qué número quieres saber si es par?)
			int n = input
			print (esPar(n))
			decision = -1
		}
		//Condicional para llamar a primerosNumerosPrimos()
		if(decision == 4){
			print(Has escogido la opcion + decision)
			print(¿Hasta qué número quieres que te muestre los pares?)
			int n = input
			primerosNumeroPrimos(n)
			decision = -1
		}
		//Condicional para finalizar el programa
		if(decision == 0){
			print(Has escogido la opcion + decision)
			exit
		} else {
			//Si no escogemos una opción válida, decision vuelve a ser -1 para que se repita el bucle.
			print(Has escogido la opcion + decision + y no es válida)
			decision = -1
		}
	}
}
~~~

### Bloque 2

### Ejercicio 7

~~~
//Funciones que nos permitirán calcular el volumen de un cilindo o un prisma a elección del usuario.

double volumenCilindro(int radio, int longitud){
	return (PI x radio^2 x longitud)
}

double volumenPrismaRectangular(int lado1, int lado2, int lado3){
	return (lado1 x lado2 x lado3)
}
~~~

### Ejercicio 8

~~~
main(){
	//Declaramos la variable decision para definir en ella la elección futura del usuario.
	int decision = -1
	//Este bucle permitirá repetirle las opciones al usuario si inserta un valor que no nos sirve.
	while (decision == -1){
		print (¿Qué se tiene que transportar? 1.Líquidos 2.Sólidos)
		decision = input
		if (decision == 1){ //Este condicional llamará la funcion para calcular el volumen para líquidos.
			print(Introduce el radio de la cisterna en centímetros)
			int radio = input
			print(Introduce la longitud de la cisterna en centímetros)
			int longitud = input
			double volumenCamion = volumenCilindro(radio, longitud)
		} else if (decision == 2){ //Este condicional llamará la funcion para calcular el volumen para sólidos.
			print(Introduce el primer lado de la caja del camión en centímetros)
			int lado1 = input
			print(Introduce el segundo lado de la caja del camión en centímetros)
			int lado2 = input
			print(Introduce el tercer lado de la caja del camión en centímetros)
			int lado3 = input
			double volumenCamion = volumenPrismaRectangular(lado1, lado2, lado3)
		} else { //Si el usuario no inserta un 1 o un 2, se le repetirá la pregunta.
			print(No es una opción válida)
			decision = -1
		}
	}
	//Finalmente resolvemos las preguntas de cuantos viajes harán falta hacer preguntando al usuario los metros cúbicos a transportar y haciendo las operaciones necesarias.
	print(¿Cuántos metros cúbicos se tienen que transportar?)
	int volumentTotal = input
	double volumenCamionMetrosCubicos = volumenCamion / 1000000
	print(El camion tiene una capacidad de  + volumenCamion +  centímetros cúbicos.
	print(Caben  + volumenCamionMetrosCubicos + metros cúbicos.
	double viajes = volumenTotal / volumenCamionMetrosCubicos
	viajes = roundUp(viajes)
	print( Se deberán hacer  + viajes +  viajes.)
}
~~~
