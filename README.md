# C-Code-Hotel-Management-Project
#This code contains the commands of creating a Hotel management system using C++ , this code uses commands like switch and break and many more 



#include <iostream>
using namespace std;
int main()
{
   
    int guests,bill=0,Round;
    char reservation, response,food;
    string name;
    string Reservation[10]={"Jatin"};
    string BILL[100];
    for(int i=0; i<55;i++)
    {
        cout<<"*";
    }
   
    cout<<" Welcome To The Restaurant";
   
    for(int i=0; i<58;i++)
    {
        cout<<"*";
    }
   
    cout<<endl;
   
    cout<<"NUMBER OF GUESTS:"<<endl;
    cin>>guests;
   
    cout<<"Do You Have A Reservation? Y/N"<<endl;
    cin>>reservation;
   
    if (reservation=='Y')
    {
        cout<<"Name of the Table Reserved Under ?"<<endl;
        cin>>name;
       
        cout<<"Checking Reservation List"<<endl;
        for(int j=0;j<=10;j++)
        {
            if (name==Reservation[j])
            {
                cout<<"Escorting to Table 5"<<endl;
                break;
            }
        }
    }
    else
    {
        cout<<"Escorting to a Available Table 7"<<endl;
    }
        cout<<"Presenting "<<guests-1<<" Menu Cards ";
        cout<<"Would you Like to Order off the menu?:";
        cin>>response;
        Round=0;
      do
      {
         
          cout<<"What would You like to Order? (S)oup|(E)ntree|(M)ain Course|(D)esserts:";
          cin>>food;
         
          switch (food)
          {
              case 'S':
              {
                  cout<<"Paya Soup \t  Rs.260 \n Sweet n Sour \t Rs.260 \n Manchurian Soup \t Rs.260"<<endl;
                  cin>>BILL[Round];
                  bill=bill+260;
                  break;
              }
             
              case 'E':
              {
                  cout<<"Paneer Starters \t Rs.320 \n Salad Starters \t Rs. 320 \n Chicken Starters \t Rs.320"<<endl;
                  cin>>BILL[Round];
                  bill=bill+320;
                  break;
              }
             
              case 'M':
              {
                  cout<<"Assortment of Breads \t Rs.200 \n Paneer Tikka Masala \t Rs.200 \n Butter Chicken \t Rs. 200"<<endl;
                 cin>>BILL[Round];
                 bill=bill+200;
                  break;
              }
             
              case 'D':
              {
                  cout<<" ICECREAMS \t Rs. 130 \n Gulab Jamun (2 Piece) \t Rs.130 \n Halwa \t Rs.130"<<endl;
                cin>>BILL[Round];
                bill=bill+130;
                   break;
              }
             
              default:
              {
                  cout<<"Invalid Choice!";
              }
             
          }
         
          cout<<"Would You like to Like to Order More?";
          cin>>response;
         
          Round++;
      } while(response!='N');
       
        for(int l=0; l<Round;l++)
        {
            cout<<BILL[l]<<endl;
        }
        cout<<"Bill: "<<bill;
       
       
   

    return 0;
}

