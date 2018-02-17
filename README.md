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
