# unit_testing
breaking a problem into methods and test those methods
look at JUnit 4

~~~java
public class Car{

  drive(){
    startCar(){
      checkSourceOfIgnition(){
      if (key) startKeyCar();
      else startFobCar();
    }
    }
    putSeatbeltOn(){
      grabSeatbelt;
      clickItOrTicket;
    }
    putInGear(){
      if (manual) shiftManual();
      else shiftAuto();
    }
    accellerate(){};
    turn(){};
    brake(){};
    }
  shiftManual(){
    pressClutch(){workClutch(true)}
    moveGearShift(gear);
    releaseClutch(){workClutch(false)}

  }

  boolean isClutchPress;
  private void workClutch(boolean press){
    if (press){
      isClutchPress = true;
    }
    else isClutchPress = false;
  }

  void testWorkClutch(){
    workClutch(true);
    assert(isClutchPress);
    workClutch(false);
    assert(!isClutchPress);
  }
}
~~~
CarTest
java -ea CarTest //ea = enable assertions
