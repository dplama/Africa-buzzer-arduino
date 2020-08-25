# Africa-buzzer-arduino


#include "pitches.h" 
const int buzzer = 10; 
const int songspeed = 1.5; //The bigger the number the slower the song

//Note order of song 
int melody[]={
  NOTE_CS5,0, NOTE_CS5, NOTE_CS5,0, NOTE_CS5, NOTE_CS5,0, NOTE_B4,0, NOTE_E5
  } ; 

  //Duration of each note in ms. Quarter note is set to 250 ms 
int  duration[]={
  500,100, 500, 250,125, 250, 250,125, 250, 125, 1000,
  }; 


void setup() {
 
}

void loop() {
   for (int i=0; i<11; i++){              //203 is the total number of music notes in the song
  int wait = duration[i] * songspeed;
  tone(buzzer, melody[i], wait);          //tone(pin,frequency,duration)
  delay(wait);}                        //delay is used so it doesn't go to the next loop before tone is finished playing
 

 delay (2000); 

}
