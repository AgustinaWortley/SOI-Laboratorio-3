### SOI-Laboratorio-Nº 3
# GNU gdb

## Objetivo
Dar al alumno herramientas de debugging de programas en C. Obtener práctica en el manejo de archivos core dumps.

## Duración
Los temas presentados a continuación son básicos de programación. Este laboratorio está diseñado para resolverse entre 2 y 3 horas.

## Actividades

### Debug con gdb

Utilizando gdb arregle el siguiente programa:
``` C
#include <iostream>
#include <cmath>

using namespace std;

int factorial(int number) {
  int fact;

  for (int j = 1; j < number; j++) {
    fact = fact * j;
  }

  return fact;
}

double compute_series_value(double x, int n) {
  double series_value = 0.0;
  double xpow = 1;

  for (int k = 0; k <= n; k++) {
    series_value += xpow / factorial(k);
    xpow = xpow * x;
  }

  return seriesValue;
}

int main() {
  cout << "This program is used to compute the value of the following series : " << endl;

  cout << "(x^0)/0! + (x^1)/1! + (x^2)/2! + (x^3)/3! + (x^4)/4! + ........ + (x^n)/n! " << endl;

  cout << "Please enter the value of x : " ;
  
  double x;
  cin >> x;

  int n;
  cout << endl << "Please enter an integer value for n : " ;
  cin >> n;
  cout << endl;

  double series_value = compute_series_value(x, n);
  cout << "The value of the series for the values entered is " 
    << series_value << endl;

  return 0;
}
```
### Debug con core dumps
Utilizando gdb arregle el siguiente programa que genera un core dump

```C
#include <stdio.h>

void main()
{
    char *temp = "Paras";

    int i;
    i=0;

    temp[3]='F';

    for (i =0 ; i < 5 ; i++ )
        printf("%c\n", temp[i]);

    
} ```
