# Programacion---Practica1
## Resolución del exámen de la primera evaluación del grupo presencial.

### Bloque 1

### Ejercicio 1

~~~
void decimalBinario(int n){
	while(n != 0){
		print(n % 2)
		n = n / 2
	}
}
~~~

### Ejercicio 2

~~~
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
void primerosNumeroPrimos(int n){
	for (int i = 0; i <= n; i = i + 2){
		print(i)
	}
}
~~~

### Ejercicio 5

~~~
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
main(){
	int decision = -1
	while(decision == -1){
		decision = menu()
		if(decision == 1){
			print(Has escogido la opcion + decision)
			print(¿Qué número quieres pasar de decimal a binario?)
			int n = input
			decimalBinario(n)
			decision = -1
		}
		if(decision == 2){
			print(Has escogido la opcion + decision)
			print(¿Qué número quieres pasar de binario a decimal?)
			long n = input
			binarioDecimal(n)
			decision = -1
		}
		if(decision == 3){
			print(Has escogido la opcion + decision)
			print(¿Qué número quieres saber si es par?)
			int n = input
			print (esPar(n))
			decision = -1
		}
		if(decision == 4){
			print(Has escogido la opcion + decision)
			print(¿Hasta qué número quieres que te muestre los pares?)
			int n = input
			primerosNumeroPrimos(n)
			decision = -1
		}
		if(decision == 0){
			print(Has escogido la opcion + decision)
			exit
		} else {
			print(Has escogido la opcion + decision + y no es válida)
			decision = -1
		}
	}
}
~~~

### Bloque 2

### Ejercicio 7

~~~
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
	int decision = -1
	while (decision == -1){
		print (¿Qué se tiene que transportar? 1.Líquidos 2.Sólidos)
		decision = input
		if (decision == 1){
			print(Introduce el radio de la cisterna en centímetros)
			int radio = input
			print(Introduce la longitud de la cisterna en centímetros)
			int longitud = input
			double volumenCamion = volumenCilindro(radio, longitud)
		} else if (decision == 2){
			print(Introduce el primer lado de la caja del camión en centímetros)
			int lado1 = input
			print(Introduce el segundo lado de la caja del camión en centímetros)
			int lado2 = input
			print(Introduce el tercer lado de la caja del camión en centímetros)
			int lado3 = input
			double volumenCamion = volumenPrismaRectangular(lado1, lado2, lado3)
		} else {
			print(No es una opción válida)
			decision = -1
		}
	}
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
