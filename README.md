#include <iostream>
#include <cstdlib>

using namespace std;


struct Node
{
    Node* link;
    string item
    double cost;
};

class Shop
{
public:
  Shop();
  ~Shop();
  void buy(string item, double price);
  void remove;
  void sort;
  void output;
  int length;
  
private:
  int itemCount;
  Node start; //Points to the front of the list
  Node end; //Points to the end of the list
  int totalCost; //Track final cost
}

Shop::Shop(){//Initialize
  itemCount = 0;
  totalCost = 0;
  start = NULL;
  end = NULL;
}

Shop::~Shop(){
  Node *deleter;//Pointer to destruct nodes*
  while (start != NULL)//While elements remain, continue deleting.
 {
  deleter = start; //Set deleter to the start node.
  start = start->link; //Move start forward in the list.
  delete deleter; //Delete the node deleter is pointing at.
 }
 end = NULL;//Point end to NULL, finishing the list's destruction.
}

#include <iostream>
#include <string>
using namespace std;

//Function Prototypes
void sortArray(string[], int);

int main()
{
	const int NUMBER = 6;
	string names[NUMBER] = {"Bob", "Tina", "Peter", "Kara", "Emily", "Harry"};


	cout << "This program will sort an array of 6 strings.";
	sortArray(names, NUMBER);


	//Display
	for (int count = 0; count < NUMBER; count++)
		cout << names[count] << endl;


	system("PAUSE");
	return 0;

}


void sortArray(string names[], int size)
{
	
	bool flag;

	do
	{
		flag = 0;
		for( int count = 0; count < size; count++)
		{
			if (names[count] > names[count+1])
			{
				names[count].swap(names[count+1]);
				flag = 1;
			}
			
		}
	} while (flag = 1);

}
