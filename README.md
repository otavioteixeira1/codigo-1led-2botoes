/* CODIGO PARA LIGAR E DESLIGAR UM LED COM DOIS BOTÕES
Otavio Augusto Santos Teixeira 
Curso IOT na pratica 2018 */

int botao    = D2; // define pino 9 como entrada botao liga
int botao1  = D5; //  define botao 8 como botao desliga
int saida = D1; // define pino 13 como saida


void setup() {

  pinMode (botao,  INPUT_PULLUP); // define como entrada
  pinMode (botao1, INPUT_PULLUP); // define como entrada
  pinMode (saida, OUTPUT);     // define como saida
}

void loop() {


  int valor =  digitalRead (botao);//  le o valor de botao
  int valor2 = digitalRead (botao1); // le o valor de botao1

  if (valor == HIGH && valor2 == LOW) {// Testa o estado dos botoes
    digitalWrite (saida, HIGH); //  envia saida para nivel alto
    delay (100);
  }

  if (valor == LOW && valor2 == HIGH) { // Testa saida dos botoes
    digitalWrite (saida,LOW); // envia a saida para nivel baixo
    delay (100);
 

  }
}
