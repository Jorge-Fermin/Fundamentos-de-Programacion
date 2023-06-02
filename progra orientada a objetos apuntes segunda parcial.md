# jorge fermin gama i.c.i 2B
# programacion orientada a objetos 
# apuntes
#Unidad 2. Programación Orientada a Objetos con Dart

#Unidad 2. Programación Orientada a  Objetos con Dart

Clases

Ejemplo: creación de una clase

void main(List<String> args) { print("Clase: ${Persona().runtimeType}");

#class Persona ()

 Salida:

Clase: Persona

 Ejemplo: creación de una instancia de clase

void main(List<String> args) {

Persona persona = Persona(); print (persona);

 print("Clase: ${persona.runtimeType}");
}
 class Persona ()

Salida:

Instance of Persona Clase: Personal
Void main

Persona persona Persona(); print(persona.nombre);

print (persona.edad);

Ejemplo: uso de las propiedades de instancia void main(List<String> args) { Persona persona = Persona();

print (persona.nombre);

print(persona.edad); persona.nombre "Alex";

persona.edad 51;

print (persona.nombre); print(persona.edad);

class Persona ( String? nombre; int? edad:

Salida:

null

null Alex.

51

Ejemplo: creación de métodos en la clase void main(List<String> args) { Persona persona Persona(); persona.mostrarDatosPersona();

class Persona (

//Propiedades String? nombre;

int? edad,

//métodos
Ejemplo: Instancia de la clase Persona usando propiedades de instancia

void main(List<String> args) { Persona persona = Persona();

persona.nombre = "Hugo"; persona.edad= 10;

print("Nombre: $(persona.nombre)"); print("Edad: $(persona.edad)");

class Persona { //Propiedades

String? nombre; int? edad;

//Métodos

void mostrarDatosPersona() { print("Nombre: $nombre");

print("Edad: Sedad");

}

Salida:

Nombre: Hugo Edad: 10

void main(List<String> args) { Persona persona = Persona();

persona.nombre = "Hugo"; persona.edad = 10;

persona.mostrarDatos Persona();

class Persona {

//Propiedades

int? edad;

Constructores

Ejemplo: Constructor de la clase Persona void main(List<String> args) {

Persona persona Persona ("Hugo", 10); print("Nombre: ${persona.nombre)");

print("Edad: ${persona.edad)");

class Persona { //Propiedades

String? nombre; int? edad;

//Constructor Persona(String nom, int ed) {

nombre nom;

edad = ed;

//Métodos

void mostrarDatosPersona () { print("Nombre: $nombre");

print("Edad: Sedad");

Salida:

Nombre: Hugo Edad: 10

Clase Persona { String? nombre; int? edad;

//Constructor

Persona(String nombre, int edad) {

this.nombre = nombre; this.edad edad;

void mostrarDatos Persona () { print("Nombre: Snombre");

print("Edad: Sedad");

}

}

Salida:

Nombre: Hugo Edad: 10

Versión 2:

void main(List<String> args) { Persona persona = Persona ("Hugo", 10);

print("Nombre: ${persona.nombre}"); print("Edad: ${persona.edad)");

}

class Persona {

//Propiedades

String? nombre; int? edad;

Ejemplo: Constructor de la clase persona con argumentos opcionales y por defecto void main(List<String> args) {

Persona persona = Persona ("Hugo");

print("Nombre: $(persona.nombre}"); print("Edad: ${persona.edad)");

}

}

Archivo: lib/Motocicleta.dart

import 'Vehiculo.dart';

class Motocicleta extends Vehiculo { Motocicleta (super.color, super.velocidad) {

print("Constructor hijo Motocicleta");

} }

Archivo: bin/mi_app.dart

import 'package:mi_app/Carro.dart'; import 'package:mi_app/Motocicleta.dart';

void main(List<String> args) {

var carro1 Carro ("rojo", 100);

carrol.showVehicle();

print(carrol.maxVelocidad()); print(" 20);

var moto1 = Motocicleta ("Azul", moto1.showVehicle(); print (moto1.maxvelocidad()) }

Salida:

Constructor hijo

Color: rojo

Velocidad:

200

Constructor hijo Motocicleta

Color: Azul Velocidad: 60

120

Ejemplo: Clases Motocicleta y Carro que heredan de vehículo con propiedades en cada

clase hija

Archivo: lib/Vehiculo.dart

class Vehiculo (

String? _color;

int? _velocidad;

//Vehiculo(this._color, this. velocidad); Vehiculo() {

print("Costructor padre - Vehiculo");

set color (String color) => _color = color; set velocidad (int velocidad) => _velocidad = velocidad;

String get color => _color!; int get velocidad => _velocidad!;

int maxVelocidad () => _velocidad! . 2;

}

Archivo: lib/Carro.dart

import 'Vehiculo.dart';

class Carro extends Vehiculo {

String _marca;

Carro(this._marca) {

print("Constructor hijo Carro

}

}

Archivo: lib/Motocicleta.dart

import 'Vehiculo.dart';

String modelo;

print("Constructor hijo Motocicleta $_modelo"); exer

Arch

import 'package:mi_app/Carro.dart'; import 'package:mi_app/Motocicleta.dart';

void main(List<String> args) { var carro1= Carro("Ford");

carro1.color = "rojo"; carro1.velocidad = 100;

print(carro1.color); print(carrol.velocidad);

print(carrol.maxVelocidad()); print("-" 20);

var moto1 = Motocicleta ("REBEL 1100"); moto1.velocidad = 60;

moto1.color = "azul";

print (moto1.color);

print (moto1.velocidad); print(motol.maxVelocidad());

Salida:

Costructor padre Vehiculo Constructor hijo Carro Ford

rojo 100

200

Costructor padre Vehiculo

Constructor hijo Motocicleta REBEL

azul

60

120

Ejemplo: Clases Motocicleta y Carro nuevas propiedades vehículo con el constructor padre y

Archivo: lib/Vehiculo.dart

class Vehiculo (

String? _color; int? _velocidad;

Computación Intelige

print("Constructor padre - Vehiculo");

set col

set color(String color) => _color = color;

set velocidad (int velocidad) => velocidad velocidad;

String get color => _color!;

int get velocidad => _velocidad!;

int maxVelocidad() => _velocidad! 2;

void showVehicle() { print("Color: $_color"); print("Velocidad: $_velocidad");

Archivo: lib/Carro.dart

import 'Vehiculo.dart';

class Carro extends Vehiculo {

String _marca;

Carro (super.color, super.velocidad, this._marca) { print("Constructor hijo Carro");

Archivo: lib/Motocicleta.dart

import 'Vehiculo.dart';

class Motocicleta extends Vehiculo ( String _modelo;

}

Archivo: bin/mi_app.dart

void main(List<String> args)

var carrol Carro("rojo" 100, "Ford");

carrol.showVehicle();

print(carrol.maxVelocidad()); print( 20);

var motol = Motocicleta ("Azul", 68, "T1000");

moto1.showVehicle();

print (moto1.maxVelocidad());

Salida

Constructor padre - Vehiculo

Constructor hijo - Carro Color: rojo

Velocidad: 100 200

Constructor padre. Constructor hijo Vehiculo Motocicleta

Color: Azul Velocidad: 60

120

Ejemplo: Clases Motocicleta y Carro que heredan de vehículo con sobreescritura d método padre

Archivo: lib/Vehiculo.dart

class Vehiculo {

String? color; int? velocidad;

Vehiculo(this._color, this._velocidad) { print("Constructor padre - Vehiculo");

} set color(String color) => _color color; set velocidad (int velocidad) => velocid

String get color = int get velocidad

> _color!; => _velocidad!;

int maxvelocidad () => velocid

void showVehicle() (

}

Carro (super.color, super.velocidad, this._marca) {

Carro");

print("Constructor hijo

void showVehicle() { print("Color: $color");

print("Velocidad: $velocidad");

print("Marca: $_marca");

Archivo: lib/Motocicleta.dart

import 'Vehiculo.dart';

class Motocicleta extends Vehiculo {

String modelo;

Motocicleta (super.color, super.velocidad, this._modelo) Inteligente import 'package:mi_app/Motocicleta.dart'; utación

print("Constructor hijo Motocicleta");

Boverride

void showVehicle() { print("Color: $color");

print("Velocidad: Svelocidad");

print("Modelo: $_modelo");

}

}

Archivo: bin/mi_app.dart

import 'package:mi_app/Carro.dart';

void main(List<String> args) { var carrol Carro ("rojo", 100, "Ford");

carro1.showVehicle();

print(carrol.maxVelocidad());

print("" 20);

var moto1 Motocicleta ("Azul", 60, "T1000");

moto1.showVehicle();

Constructor padre.

Constructor hijo

Color: rojo Velocidad: 100

Marca: Ford 200 Constructor padre Constructor hijo Color: Azul Vehiculo Motocicleta

Velocidad: 60

Marca: T1000

120

Ejemplo: Constructor nombrado en la Clase Carro

Archivo: lib/Vehiculo.dart

class Vehiculo { String? _color;

int? velocidad;

Vehiculo(this._color, this._velocidad) { print("Constructor padre Vehiculo");

set color (String color) => _color = color;

set velocidad (int velocidad) => _velocidad = velocidad;

String get color => _color!;

int get velocidad => _velocidad!;

int maxvelocidad () => velocidad! void showVehicle() { print("Color: $_color"); Computacio Inteligente

print("Velocidad: $_velocida

Mata López

Archivo: lib/Carro.dart

Walxander

Sepia

Carro. Tipo (super.color, super.velocidad, this._marca, this._tipo) {

print("Constructor hijo - Carro tipo: $_tipo");

void showVehicle() {

print("Color: $color"); print("Velocidad: $velocidad");

Ejemplo: Clases genéricas

void main(List<String> args) {

Contador<double> doubles Contador<double>(); doubles.addAll([1.1, 1.2, 1.31);

doubles.total();

Contador<int> ints Contador<int>();

ints.addAll([1, 2, 3]); ints.total();

}

class Contador<T extends num> { List items = <T>[];

void addAll(Iterable<T> iterable) => items.addAll(

void add(T value) => _items.add(value);

T elementAt(int index) => _items.elementAt(index);

void total() { num value = 0;

for (var val in _items) { value += val as T;

print(value);

}

Salida:
3.6666666

Programación Asíncrona

Sirve para ejecutar aplicaciones en segundo plano

Ejemplo: Programa Sincrono import 'dart:io';

void main(List<String> args) { stdout.write("Dame tu nombre: ");

String? nombre stdin.readLineSync();

}

print("Hola $nombre");

Salida:

Dame tu nombre: Walter Hola Walter

Ejemplo: Programa asincrono que lee un archivo de texto

Archivo bin/contactos.txt

1. Hugo 2. Paco

3. Luis

4. Maria

5. Karla

Archivo: bin/mi_app.dart

import 'dart:io'; import 'dart: async';

Ejemplo: Future

Es el resultado de una operación asíncrona

Puede tener dos estados:

Incompleto

Completo import 'dart: async';

void main(List<String> args) {

print("Iniciando programa...");

saludo ("Probando un Future").then((value) => print(value)) print("Finalizando programa...");

Future<String> saludo (String msg) {

return Future.delayed (Duration (seconds: 5), ()

}

Salida:

Iniciando programa...

Finalizando programa... Hola, Probando un Future
