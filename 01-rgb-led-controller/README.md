
//DEFINE Pins to match my physical wiring

#define BLUE 3
#define GREEN 5
#define RED 6

// Time to stay on each color (in milliseconds)
// 1000 ms = 1 seconds
#define HOLD_TIME 1000

void setup()
{
  // Configure pins as OUTPUTs
  pinMode(RED, OUTPUT);
  pinMode(GREEN, OUTPUT);
  pinMode(BLUE, OUTPUT);
}


void loop() {
  // 1. RED
  setColor(255, 0, 0);
  delay(HOLD_TIME);

  // 2. BLUE
  setColor(0, 0, 255);
  delay(HOLD_TIME);

  // 3. GREEN
  setColor(0, 255, 0);
  delay(HOLD_TIME);

  // 4. PURPLE (RED + BLUE)
  setColor(255, 0, 255);
  delay(HOLD_TIME);

  // 5. YELLOW (RED + GREEN)
  setColor(255, 255, 0);
  delay(HOLD_TIME);

  // 6. CYAN (GREEN + BLUE)
  setColor(0, 255, 255);
  delay(HOLD_TIME);

  // 7. WHITE (ALL ON)
  setColor(255, 255, 255);
  delay(HOLD_TIME);
}

//Helper function to set color value cleanly
void setColor(int red, int green, int blue) {
  analogWrite(RED, red);
  analogWrite(GREEN, green);
  analogWrite(BLUE, blue);
}
