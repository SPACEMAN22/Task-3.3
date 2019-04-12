# Task-3.3
buddy system 


int ledone = D6; 
int ledtwo = D5;

void wave(const char *event, const char *data) {

  
  digitalWrite(ledone, HIGH);
  delay(1000);
  digitalWrite(ledone, LOW);
  delay(1000);
  digitalWrite(ledone, HIGH);
  delay(1000);
  digitalWrite(ledone, LOW);
  delay(1000);
  digitalWrite(ledone, HIGH);
  delay(1000);
  digitalWrite(ledone, LOW);


}

void pat(const char *event, const char *data)
{
  digitalWrite(ledtwo, HIGH);
  delay(100);
  digitalWrite(ledtwo, LOW);
  delay(100);
  digitalWrite(ledtwo, HIGH);
  delay(100);
  digitalWrite(ledtwo, LOW);
  delay(100);
  digitalWrite(ledtwo, HIGH);
  delay(100);
  digitalWrite(ledtwo, LOW);
}
void setup() {


  pinMode(ledone, OUTPUT);
  pinMode(ledtwo, OUTPUT);
  Particle.subscribe("Deakin_RIOT_SIT210_Photon_Buddy", wave);
  Particle.subscribe("Deakin_RIOT_SIT210_Photon_Buddy", pat);
  
  Serial.begin(9600);

}


void loop() {



}
