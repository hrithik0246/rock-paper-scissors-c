#include<stdio.h>
#include<stdlib.h>
#include<time.h>
int main(){
    int uChoice,cChoice,i=0;
    int pScore=0,cScore=0;
     srand(time(0));
   

    
    printf("WELCOME TO ROCK | PAPPER | SISSORS\n");
    printf("\n press 1 for ROCK!\n press 2 for PAPPER\n press 3 for SISSORS\n");
    do{
    printf("----------------------------------------------------------------------------\nPls Enter The Input _________\n");
    scanf("%d",&uChoice);
     cChoice=rand() %3+1;
    
    switch(cChoice){
        case 1: printf("Player 1: ROCK\n");
        break;
        case 2: printf("Player 1: PAPPER\n");
        break;
        case 3: printf("Player 1: SISSORS\n");
        break;
        default: printf("ENTER ALID NUMBER ONLY\nINSTUCTIONS\npress 1 for ROCK\npress 2 for PAPPER\n 3 for SISSORS\n");
        
    }
    
    if(cChoice==uChoice){
        printf("TIE!");
        
    }
    else if((uChoice == 1 && cChoice==3) || (uChoice == 2 && cChoice==1) || (uChoice == 3 && cChoice==2)){
        printf("HEY HEY YOU WIN!!!!*****!!!!");
        pScore++;
        
    }
    
    else{
        printf("you loose\n TRY AGAIN NEXT TIME \n");
        cScore++;
    }
    i++;
    }
    while(i<5);
    
    printf("---------------------FINAL SCORE-------------------\n");
    printf("your Score:%d\n",pScore);
    printf("Player 1's Score:%d\n",cScore);
    if(pScore>cScore){
        printf("You WIN with %d points",pScore);
    }
    else if(cScore>pScore){
        printf("YOU lose for %d Points with PLAYER 1!!!",cScore);
    }
    else{
        printf("Well Played Tie!!!!");
    }
    return 0;
    
}
