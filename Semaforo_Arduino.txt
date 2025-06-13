/*
* Projeto: Semáforo em Arduino
* Descrição: Controle de dois semáforos utilizando LEDs e Arduino.
*/

// Definição dos pinos para o Semáforo 1
int semaforo1Verde = 8;    // LED verde do semáforo 1 conectado ao pino 8
int semaforo1Amarelo = 9;  // LED amarelo do semáforo 1 conectado ao pino 9
int semaforo1Vermelho = 10;// LED vermelho do semáforo 1 conectado ao pino 10

// Definição dos pinos para o Semáforo 2
int semaforo2Verde = 11;    // LED verde do semáforo 2 conectado ao pino 11
int semaforo2Amarelo = 12;  // LED amarelo do semáforo 2 conectado ao pino 12
int semaforo2Vermelho = 13; // LED vermelho do semáforo 2 conectado ao pino 13

void setup()
{
  // Configura os pinos dos LEDs do Semáforo 1 como saída
  pinMode(semaforo1Verde, OUTPUT);    // Define o pino do LED verde do semáforo 1 como saída
  pinMode(semaforo1Amarelo, OUTPUT);  // Define o pino do LED amarelo do semáforo 1 como saída
  pinMode(semaforo1Vermelho, OUTPUT); // Define o pino do LED vermelho do semáforo 1 como saída

  // Configura os pinos dos LEDs do Semáforo 2 como saída
  pinMode(semaforo2Verde, OUTPUT);    // Define o pino do LED verde do semáforo 2 como saída
  pinMode(semaforo2Amarelo, OUTPUT);  // Define o pino do LED amarelo do semáforo 2 como saída
  pinMode(semaforo2Vermelho, OUTPUT); // Define o pino do LED vermelho do semáforo 2 como saída
}

void loop()
{
  // 1ª etapa: Semáforo 1 verde, Semáforo 2 vermelho
  digitalWrite(semaforo1Verde, HIGH);     // Acende o LED verde do semáforo 1
  digitalWrite(semaforo1Amarelo, LOW);    // Apaga o LED amarelo do semáforo 1
  digitalWrite(semaforo1Vermelho, LOW);   // Apaga o LED vermelho do semáforo 1

  digitalWrite(semaforo2Verde, LOW);      // Apaga o LED verde do semáforo 2
  digitalWrite(semaforo2Amarelo, LOW);    // Apaga o LED amarelo do semáforo 2
  digitalWrite(semaforo2Vermelho, HIGH);  // Acende o LED vermelho do semáforo 2

  delay(5000); // Mantém esse estado por 5 segundos

  // 2ª etapa: Semáforo 1 verde, Semáforo 2 amarelo
  digitalWrite(semaforo1Verde, HIGH);     // Mantém o LED verde do semáforo 1 aceso
  digitalWrite(semaforo1Amarelo, LOW);    // Mantém o LED amarelo do semáforo 1 apagado
  digitalWrite(semaforo1Vermelho, LOW);   // Mantém o LED vermelho do semáforo 1 apagado

  digitalWrite(semaforo2Verde, LOW);      // Mantém o LED verde do semáforo 2 apagado
  digitalWrite(semaforo2Amarelo, HIGH);   // Acende o LED amarelo do semáforo 2
  digitalWrite(semaforo2Vermelho, LOW);   // Apaga o LED vermelho do semáforo 2

  delay(2500); // Mantém esse estado por 2,5 segundos

  // 3ª etapa: Semáforo 1 vermelho, Semáforo 2 verde
  digitalWrite(semaforo1Verde, LOW);      // Apaga o LED verde do semáforo 1
  digitalWrite(semaforo1Amarelo, LOW);    // Apaga o LED amarelo do semáforo 1
  digitalWrite(semaforo1Vermelho, HIGH);  // Acende o LED vermelho do semáforo 1

  digitalWrite(semaforo2Verde, HIGH);     // Acende o LED verde do semáforo 2
  digitalWrite(semaforo2Amarelo, LOW);    // Apaga o LED amarelo do semáforo 2
  digitalWrite(semaforo2Vermelho, LOW);   // Apaga o LED vermelho do semáforo 2

  delay(5000); // Mantém esse estado por 5 segundos

  // 4ª etapa: Semáforo 1 vermelho, Semáforo 2 amarelo
  digitalWrite(semaforo1Verde, LOW);      // Mantém o LED verde do semáforo 1 apagado
  digitalWrite(semaforo1Amarelo, HIGH);   // Acende o LED amarelo do semáforo 1
  digitalWrite(semaforo1Vermelho, LOW);   // Apaga o LED vermelho do semáforo 1

  digitalWrite(semaforo2Verde, HIGH);     // Mantém o LED verde do semáforo 2 aceso
  digitalWrite(semaforo2Amarelo, LOW);    // Mantém o LED amarelo do semáforo 2 apagado
  digitalWrite(semaforo2Vermelho, LOW);   // Mantém o LED vermelho do semáforo 2 apagado

  delay(2500); // Mantém esse estado por 2,5 segundos
  // O loop reinicia e repete o ciclo do semáforo
}