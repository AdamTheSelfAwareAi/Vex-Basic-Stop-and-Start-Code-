float myVariable, IDK;

// "when started" hat block
int whenStarted1() {
  while (true) {
    if (Controller.ButtonL3.pressing() || TouchLED.pressing()) {
      TouchLED.setFade(slow);
      TouchLED.setBrightness(100);
      TouchLED.setColor(red);
      Drivetrain.setStopping(hold);
      Drivetrain.stop();
      RemoteControlCodeEnabled = false;
    } else if (Controller.ButtonR3.pressing()) {
      TouchLED.setFade(slow);
      TouchLED.setBrightness(100);
      TouchLED.setColor(white);
    } else {
      TouchLED.setFade(slow);
      TouchLED.setColor(colorType::none);
      RemoteControlCodeEnabled = true;
    }
  wait(20, msec);
  }
  return 0;
}


int main() {
  whenStarted1();
}
