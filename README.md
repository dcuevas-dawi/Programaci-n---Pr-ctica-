# Programacion---Practica1
## Resolución del exámen de la primera evaluación del grupo presencial.

### Bloque 1

### Ejercicio 1

~~~
decimalBinario(int n){
	while(n != 0){
		print(n % 2)
		n = n / 2
	}
}
~~~

### Ejercicio 2

~~~
binarioDecimal(long n){
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
esPar(int n){
	if(n % 2 == 0){
		return true
	} else {
		return false
	}
}
~~~

### Ejercicio 4

~~~
primerosNumeroPrimos(int n){
	for (int i = 0; i <= n; i = i + 2){
		print(i)
	}
}
~~~

### Ejercicio 5

~~~
menu(){
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



~~~
