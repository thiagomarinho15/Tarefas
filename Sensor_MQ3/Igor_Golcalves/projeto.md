## Tarefa: prototipar a detecção de etanol
### Esquema montado no Tinkercad
![image](https://github.com/luizkeng/IC-Igor_Goncalves/blob/main/Arduino%20da%20aula%20de%20ic.png)
---
### Código C
```int LED = A1;
const int gas = 0;
int MQ2pin = A0;


void setup() {
  Serial.begin(9600);
}

void loop() {
  float sensorValue,MQ2pin;
sensorValue = analogRead(MQ2pin); // read analog input pin 0

  if(sensorValue >= 470){
    digitalWrite(LED,HIGH);
    Serial.print(sensorValue);
    Serial.println(" |Fumaça detectada!");
    
  
  }
  else{
  	digitalWrite(LED,LOW);
    Serial.println("Valor do Sensor: ");
    Serial.println(sensorValue);
  } 
  delay(1000);
}
	float getsensorValue(int pin){
  	return (analogRead(pin));
}
```
---
### Link do Tinkercad 
https://www.tinkercad.com/things/a4t7IMtvGpH

