# CONNECT-4-GAME
Code for CONNECT FOUR Game using C Language




#include <stdio.h>
int main()
{
  char row1[7]={0,0,0,0,0,0,0},row2[7]={0,0,0,0,0,0,0},row3[7]={0,0,0,0,0,0,0},row4[7]={0,0,0,0,0,0,0}, row5[7]={0,0,0,0,0,0,0},
  row6[7]={0,0,0,0,0,0,0},row7[7]={0,0,0,0,0,0,0};
  
   int move,win=0,j,i,one=0,two=0;
  char x='y';
  for(i=0;i<7;++i)
    {
      row1[0]='0';
      row2[0]='1';
      row3[0]='2';
       row4[0]='3';
       row5[0]='4';
      row6[0]='5';
      row7[0]='6';
    }
 for(i=1;i<7;i++)
            {
              row1[i]='O';
              row2[i]='O';
              row3[i]='O';
              row4[i]='O';
              row5[i]='O';
              row6[i]='O';
              row7[i]='O';            }

  while(x=='Y'||x=='y')
{
 for(i=0;i<7;i++)
        {
          if(i==0)
            printf("\n\n\n   %c %c %c %c %c %c %c  \n  ---------------\n", row1[i], row2[i], row3[i], row4[i], row5[i], row6[i], row7[i]);
          if(i>0&&i<6)
            printf(" | %c %c %c %c %c %c %c |\n", row1[i], row2[i], row3[i], row4[i], row5[i], row6[i], row7[i]);
          if(i==6)
            printf("  ---------------\n |               |\n\n\n");
        }
      while(win==0)
        {
                  if(win==0)
            {
              printf("Player1:  ");
              scanf("%d", &move);
              printf("\n\n");
             while(move<1||move>7||(move==1&&(row1[1]=='1'||row1[1]=='2'))||(move==2&&(row2[1]=='1'||row2[1]=='2'))||(move==3&&(row3[1]=='1'||row3[1]=='2')\
                                                                                                                           )||(move==4&&(row4[1]=='1'||row4[1]=='2'))|\
|(move==5&&(row5[1]=='1'||row5[1]=='2'))||(move==6&&(row6[1]=='1'||row6[1]=='2'))||(move==7&&(row7[1]=='1'||row7[1]=='2'\
                                                                                                                                                                       \
                                                                                                 )))
                {
                  printf("ERROR: cannot read slot number\n\n\n\nPlayer1:  ");
                  scanf("%d", &move);
                }
              if(move==1)
                {
                  j=6;
                  while(row1[j]=='1'||row1[j]=='2')
                    {
                      j--;
                    }
                  row1[j]='1';
                }
              else if(move==2)
                {
                  j=6;
                  while(row2[j]=='1'||row2[j]=='2')
 {
                      j--;
                    }
                  row2[j]='1';
                }
              else if(move==3)
                {
                  j=6;
                  while(row3[j]=='1'||row3[j]=='2')
                    {
                      j--;
                    }
                  row3[j]='1';
                }
              else if(move==4)
                {
                  j=6;
                  while(row4[j]=='1'||row4[j]=='2')
                    {
                      j--;
  }
                  row4[j]='1';
                }
              else if(move==5)
                {
                  j=6;
                  while(row5[j]=='1'||row5[j]=='2')
                    {
                      j--;
                    }
                  row5[j]='1';
                }
              else if(move==6)
                {
                  j=6;
                  while(row6[j]=='1'||row6[j]=='2')
                    {
                      j--;
                    }
                  row6[j]='1';
                }
  else if(move==7)
                {
                  j=6;
                  while(row7[j]=='1'||row7[j]=='2')
                    {
                      j--;
                    }
                  row7[j]='1';


                }
              //      printf('*', move);
            }
                  for(i=0;i<7;++i)
            {
              if(i==0)
printf("\n\n\n   %c %c %c %c %c %c %c  \n  ---------------\n", row1[i], row2[i], row3[i], row4[i], row5[i], row6[i], row7[i]);
              if(i>0&&i<7)
                printf(" | %c %c %c %c %c %c %c |\n", row1[i], row2[i], row3[i], row4[i], row5[i], row6[i], row7[i]);
              if(i==6)
                printf("  ---------------\n |               |\n\n\n");
   }


          for(i=6;i>0;--i)
            {
               if((row1[i]=='1'&&row2[i]=='1'&&row3[i]=='1'&&row4[i]=='1')||(row5[i]=='1'&&row2[i]=='1'&&row3[i]=='1'&&row4[i]=='1')||(row5[i]=='1'&&row6[i]==\
                                                                                                                                      '1'&&row3[i]=='1'&&row4[i]=='1')|\
|(row5[i]=='1'&&row6[i]=='1'&&row7[i]=='1'&&row4[i]=='1'))
                win=1; //for horizontal
            }
          for(i=6;i>2;--i)
            {
              if((row1[i]=='1'&&row1[i-1]=='1'&&row1[i-2]=='1'&&row1[i-3]=='1')||(row2[i]=='1'&&row2[i-1]=='1'&&row2[i-2]=='1'&&row2[i-3]=='1')||(row3[i]=='1\
'&&row3[i-1]=='1'&&row3[i-2]=='1'&&row3[i-3]=='1')||(row4[i]=='1'&&row4[i-1]=='1'&&row4[i-2]=='1'&&row4[i-3]=='1')||(row5[i]=='1'&&row5[i-1]=='1'&&row5[i-2]=='1'&&row5\
\
                                                                                                                     [i-3]=='1')||(row6[i]=='1'&&row6[i-1]=='1'&&row6[i\
-2]=='1'&&row6[i-3]=='1')||(row7[i]=='1'&&row7[i-1]=='1'&&row7[i-2]=='1'&&row7[i-3]=='1'))
                win=1; //for vertical
              if((row1[i]=='1'&&row2[i-1]=='1'&&row3[i-2]=='1'&&row4[i-3]=='1')||(row2[i]=='1'&&row3[i-1]=='1'&&row4[i-2]=='1'&&row5[i-3]=='1')||(row3[i]=='1\
'&&row4[i-1]=='1'&&row5[i-2]=='1'&&row6[i-3]=='1')||(row4[i]=='1'&&row5[i-1]=='1'&&row6[i-2]=='1'&&row7[i-3]=='1'))
                                win=1; //for diagonally up right
if((row7[i]=='1'&&row6[i-1]=='1'&&row5[i-2]=='1'&&row4[i-3]=='1')||(row6[i]=='1'&&row5[i-1]=='1'&&row4[i-2]=='1'&&row3[i-3]=='1')||(row5[i]=='1\
'&&row4[i-1]=='1'&&row3[i-2]=='1'&&row2[i-3]=='1')||(row4[i]=='1'&&row3[i-1]=='1'&&row2[i-2]=='1'&&row1[i-3]=='1'))
                win=1; //for diagonally up left
            }
          ////////////////////////////////////////////////////////
          if(win==0)
            {
              printf("Player 2:  ");
              scanf("%d", &move);
              printf("\n\n");
              while(move<1||move>7||(move==1&&(row1[1]=='1'||row1[1]=='2'))||(move==2&&(row2[1]=='1'||row2[1]=='2'))||(move==3&&(row3[1]=='1'||row3[1]=='2'))||(mo\
ve==4&&(row4[1]=='1'||row4[1]=='2'))||(move==5&&(row5[1]=='1'||row5[1]=='2'))||(move==6&&(row6[1]=='1'||row6[1]=='2'))||(move==7&&(row7[1]=='1'||row7[1]=='2')))
                {
                  printf("ERROR: cannot read slot number\n\n\n\nPlayer 2:  ");
                  scanf("%d", &move);
                }


              if(move==1)
                {
                  j=6;
                  while(row1[j]=='1'||row1[j]=='2')
 {
                      j--;
                    }
                  row1[j]='2';
                }
              else if(move==2)
                {
                  j=6;
                  while(row2[j]=='1'||row2[j]=='2')
                    {
                      j--;
                    }
                  row2[j]='2';
                }
              else if(move==3)
                {
                  j=6;
                  while(row3[j]=='1'||row3[j]=='2')
                    {
            }
                  row3[j]='2';
                }
              else if(move==4)
                {
                  j=6;
                  while(row4[j]=='1'||row4[j]=='2')
                    {
                      j--;
                    }
                  row4[j]='2';
                }
              else if(move==5)
                {
                  j=6;
                  while(row5[j]=='1'||row5[j]=='2')
                    {
                      j--;
                    }
                  row5[j]='2';
                }
 else if(move==6)
                {
                  j=6;
                  while(row6[j]=='1'||row6[j]=='2')
                    {
                      j--;
                      {
                        j--;
                      }
                      row6[j]='2';
                    }
                }
                  else if(move==7)
                    {
if(row7[1]=='1'||row7[1]=='2')
                        printf("ERROR");
                      else
                        {
                          j=6;
                          while(row7[j]=='1'||row7[j]=='2')
 {
                              j--;
                            }
                          row7[j]='2';
                        }
                    }

              // printf('X', move);
            }

              for( i=0;i<7;++i)
                {
                  if(i==0)
                    printf("\n\n\n   %c %c %c %c %c %c %c  \n  ---------------\n", row1[i], row2[i], row3[i], row4[i], row5[i], row6[i], row7[i]);
                  if(i>0&&i<7)
                    printf(" | %c %c %c %c %c %c %c |\n", row1[i], row2[i], row3[i], row4[i], row5[i], row6[i], row7[i]);
                  if(i==6)
                    printf("  ---------------\n |               |\n\n\n");
                }
for(i=6;i>0;--i)
                {
    if((row1[i]=='2'&&row2[i]=='2'&&row3[i]=='2'&&row4[i]=='2')||(row5[i]=='2'&&row2[i]=='2'&&row3[i]=='2'&&row4[i]=='2')||(row5[i]=='2'&&row6[i]=='2'&&row3[i]=='2'&&r\
ow4[i]=='2')||(row5[i]=='2'&&row6[i]=='2'&&row7[i]=='2'&&row4[i]=='2'))
                    win=2; //for horizontal
                }
              for(i=6;i>2;--i)
                {
                  if((row1[i]=='2'&&row1[i-1]=='2'&&row1[i-2]=='2'&&row1[i-3]=='2')||(row2[i]=='2'&&row2[i-1]=='2'&&row2[i-2]=='2'&&row2[i-3]=='2')||(row3[i]=='2'&&row\
3[i-1]=='2'&&row3[i-2]=='2'&&row3[i-3]=='2')||(row4[i]=='2'&&row4[i-1]=='2'&&row4[i-2]=='2'&&row4[i-3]=='2')||(row5[i]=='2'&&row5[i-1]=='2'&&row5[i-2]=='2'&&row5[i-3]=\
='2')||(row6[i]=='2'&&row6[i-1]=='2'&&row6[i-2]=='2'&&row6[i-3]=='2')||(row7[i]=='2'&&row7[i-1]=='2'&&row7[i-2]=='2'&&row7[i-3]=='2'))
                    win=2; //for vertical
                  if((row1[i]=='2'&&row2[i-1]=='2'&&row3[i-2]=='2'&&row4[i-3]=='2')||(row2[i]=='2'&&row3[i-1]=='2'&&row4[i-2]=='2'&&row5[i-3]=='2')||(row3[i]=='2'&&row\
4[i-1]=='2'&&row5[i-2]=='2'&&row6[i-3]=='2')||(row4[i]=='2'&&row5[i-1]=='2'&&row6[i-2]=='2'&&row7[i-3]=='2'))
                    win=2; //for diagonally up right
                  if((row7[i]=='2'&&row6[i-1]=='2'&&row5[i-2]=='2'&&row4[i-3]=='2')||(row6[i]=='2'&&row5[i-1]=='2'&&row4[i-2]=='2'&&row3[i-3]=='2')||(row5[i]=='2'&&row\
4[i-1]=='2'&&row3[i-2]=='2'&&row2[i-3]=='2')||(row4[i]=='2'&&row3[i-1]=='2'&&row2[i-2]=='2'&&row1[i-3]=='2'))
                    win=2; //for diagonally up left
                }

            }


          if(win==2)
            {
              ++two;
              printf("Victory! Player2 has won!\n\n ");
            }
          else if(win==1)
            {
              ++one;
              printf("Victory! Player1 has won!\n\n\n ");
            }


          scanf("%c" ,&x);


          while(x!='Y'&&x!='y'&&x!='N'&&x!='n')
            {
              printf("Would you like to play again? (Y/N): ");
              scanf("%c", &x);
            }


          printf("\n\n\n\n\n\n");


          win=0;


          for(i=1;i<7;i++)
            {
              row1[i]='O';
              row2[i]='O';
              row3[i]='O';
              row4[i]='O';
              row5[i]='O';
              row6[i]='O';
              row7[i]='O';            }
        }
      printf("Thanks for Playing!\n\n");
      return 0;
    }

