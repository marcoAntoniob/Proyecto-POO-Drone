// Proyecto-POO-Drone
//Avance del proyecto de gráfica de trayectoria de un drone
//Usando matrices estáticos
//--------------------------
#include <cmath>
#include <cstdio>
#include <vector>
#include <iostream>
#include <algorithm>
using namespace std;
int determinante(int x1,int y1, int x2, int y2){
   return x1*y2-y1*x2;   
}
int main() {
   int puntos=0, izq=0,der=0;
   cin>>puntos;
   int matrix[puntos][2]; //Recuerde el tamaño no puede ser variable
   //creando la matriz y poblando
   for(int i=0; i < puntos ; i++) {
       cin>>matrix[i][0];
       cin>>matrix[i][1];
   }
 //calculando los giros
   for(int i=0; i <puntos-2; i++){
       int x1=matrix[i+1][0]-matrix[i][0];
       int y1=matrix[i+1][1]-matrix[i][1];
       int x2=matrix[i+2][0]-matrix[i+1][0];
       int y2=matrix[i+2][1]-matrix[i+1][1];
       if(determinante(x1,y1,x2,y2)>0) {
           izq++;
       }else if(determinante(x1,y1,x2,y2)<0){
           der++;
       }
   }
   cout<<izq<<" "<<der;
   return 0;
}

//Usando matrices dinámicos(puntero de punteros)
//-----------------------------------------------
#include <cmath>
#include <cstdio>
#include <vector>
#include <iostream>
#include <algorithm>
using namespace std;
int determinante(int x1,int y1, int x2, int y2){
   return x1*y2-y1*x2;   
}
int main() {
   int izq=0,der=0;   
   int filas, col;
   cin>>filas;
   col=2;
   //Reservando espacio en la memoria
   int **matrix = new int*[filas];
   for (int i = 0; i < filas; i++) {
       matrix[i] = new int[col];
   }
   //Poblando la matriz
   for(int i=0; i < filas ; i++) {
       cin>>matrix[i][0];
       cin>>matrix[i][1];
   }
   //calculando los giros
   for(int i=0; i <filas-2; i++){
       int x1=matrix[i+1][0]-matrix[i][0];
       int y1=matrix[i+1][1]-matrix[i][1];
       int x2=matrix[i+2][0]-matrix[i+1][0];
       int y2=matrix[i+2][1]-matrix[i+1][1];
       if(determinante(x1,y1,x2,y2)>0) {
           izq++;
       }else if(determinante(x1,y1,x2,y2)<0){
           der++;
       }
   }
   //Eliminando la matriz de la memoria
    for (int i = 0; i < filas; i++) {
           delete [] matrix[i];
       }
  
 cout<<izq<<" "<<der;   
 delete [] matrix;    
 return 0;
}
