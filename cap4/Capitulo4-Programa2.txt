/*
	Capitulo 4 de Arduino desde cero en Español.
	Segundo programa que maneja el brillo del LED mediante el potenciometro.

	Autor: bitwiseAr  

*/

int LED = 3;				// LED en pin 3
int BRILLO;
int POT = 0;				// potenciometro en pin A0

void setup(){
	pinMode(LED, OUTPUT);		// pin 3 como salida
	// las entradas analogicas no requieren inicializacion
}

void loop(){
	BRILLO = analogRead(POT) / 4;	// valor leido de entrada analogica divido por 4
	analogWrite(LED, BRILLO);	// brillo del LED proporcional al giro del potenciometro
}
