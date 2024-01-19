/*  Project 2 - Scenarios - Posts, claims, implementation  Week 2
Come up with a random scenario and claim one of your peer's scenarios, then code it.

Peer's scenario:
Scenario - Alien Encounter
You find yourself in the middle of an unexpected alien encounter. The success of your interaction with extraterrestrial beings depends on specific conditions. 
If you manage to communicate with them using a universal translator successfully, and you offer them a unique Earth souvenir, the encounter is considered friendly. 
However, if the universal translator malfunctions or if you fail to provide a suitable souvenir, the encounter turns hostile.
Additionally, if you attempt to run away or attack the aliens, it also results in a hostile outcome.
#include <stdio.h>
#include <string.h>
#include <stdlib.h>
#include <stdbool.h>
#include <time.h>  
#include <unistd.h>
#include <ctype.h>
 
bool checkMalfunction();
bool offerSouvenir();
bool getYesNo();
void turnedHostile();
void turnedFriendly();

int main(void) {
 
    printf("You find yourself in the middle of an unexpected alien encounter\n");
    printf("The extraterrestrial beings would like to communicate with you.\n\n");
    printf("⌿⌰⟒⏃⎅ ⍙⟟⏁⊑ ⏁⊑⟒ ⌰⏃⍙⊬⟒⍀ ⏁⍜ ⎅⍀⍜⌿ ⏁⊑⟒ ⌰⍜⌇⏁ ☊⏃⎍⌇⟒. ⏁⊑⟒ ⊬⍜⎍⋏☌ ☍⟟⎅ ⟊⎍⋔⌿⟒⎅ ⏁⊑⟒ ⍀⎍⌇⏁⊬ ☌⏃⏁⟒)\n\n");
    printf("What would you like to do ?\n");
 
    int userChoice;
    printf("Choose an option.\n");
    printf("\t1\t\tCommunicate\n");
    printf("\t2\t\tCommunicate with universal translator\n");
    printf("\t3\t\tRun away\n");
    printf("\t4\t\tAttack Aliens\n\n\n\n");
    scanf("%d", &userChoice);
    switch (userChoice) {
    case 1:     // Communication without translator.
        printf("The aliens were unable to understand you.\n");
        turnedHostile();
        break;
    case 2:     // Communication with translator.
        if (!checkMalfunction())
        {
            printf("The transaltor works! The aliens are surprised they found life on another planet.\n");
            if(offerSouvenir()){
            turnedFriendly();
            }
            else{
            turnedHostile();
            }
        }
        else {
            printf("Your translator malfunctioned. You offended the aliens.\n");
            turnedHostile();
        }
        break;
    case 3:     // Try to run away.
        printf("Too slow.\n");
        turnedHostile();
        break;
    case 4:     // Attack the Aliens.
        printf("You decided to choose the worst possible option.\n");
        turnedHostile();
        break;
    }
   return 0;
}
void turnedHostile(){
    printf("The interaction with the aliens turned hostile.\n");
    printf("You didn't make it.\n");
    getchar();
    exit(1);
}
void turnedFriendly(){
    printf("Since you provided an Earth souvenir and you were able to understand the Aliens as well as they understood you\n your interraction with the extra terrestrials were friendly.\n");
    getchar();
    exit(0);
}
bool getUserInput(){
    printf("Please type in \'Y\' for \"Yes\" or \'N\' for \"NO\".\n");
    char userInput;
    int userAttempts = 0;
    while(userInput != 'Y' && userInput != 'N'){
        scanf(" %c", &userInput);
        userInput = toupper(userInput); 
        if (userAttempts >= 3){
            turnedHostile();
        }
        else {
            userAttempts++;
        }
    }
        if (userInput == 'Y'){
            return true;}
            else{
            return false;
            }
       
    }
bool offerSouvenir(){
    printf("Would you like to give the aliens an Earth souvenir ?\n");
    return getUserInput();
}
bool checkMalfunction() {  
    srand((int)time(0));
    int tmp = (rand() % 10);
    if (tmp > 7) {
        return true;
    }
    else {
        return false;
    }
}
