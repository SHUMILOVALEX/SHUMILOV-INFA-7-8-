Task 7.1

#include <ctime>
#include <iostream>
#include <vector>
using namespace std;
#include <iomanip>

int main() {
    
  int kolvo;
    cout <<"How many people?"<<endl;
    cin >> kolvo;
    srand(time(0));//рандомайзер
    
  vector<string> Surname = {"Smith", "Johnson", "Williams", "Brown", "Jones", "Miller", "Davis", "Wilson", "Anderson", "Taylor", "Thomas", "Moore", "Jackson", "White", "Harris", "Martin", "Thompson", "Garcia", "Martinez", "Robinson", "Clark", "Rodriguez", "Lewis", "Lee", "Walker", "Hall", "Allen", "Young", "Hernandez", "King", "Wright", "Lopez", "Hill", "Scott", "Green", "Adams", "Baker", "Gonzalez", "Nelson", "Carter", "Mitchell", "Perez", "Roberts", "Turner", "Phillips", "Campbell", "Parker", "Evans", "Edwards", "Collins", "Stewart", "Sanchez", "Morris", "Rogers", "Reed", "Cook", "Morgan", "Bell", "Murphy", "Bailey", "Rivera", "Cooper", "Richardson", "Cox", "Howard", "Ward", "Torres", "Peterson", "Gray", "Ramirez", "James", "Watson", "Brooks", "Kelly", "Sanders", "Price", "Bennett", "Wood", "Barnes", "Ross", "Henderson", "Coleman", "Jenkins", "Perry", "Powell", "Long", "Patterson", "Hughes", "Flores", "Washington", "Butler", "Simmons", "Foster", "Gibson", "Rodriguez", "Wallace", "Mendez", "Pearson", "Harrison", "Castillo"};
    
  vector<string> Name = {"John", "Emily", "Michael", "Sophia", "William", "Olivia", "James", "Ava", "Robert", "Isabella", "David", "Mia", "Charles", "Amelia", "Joseph", "Harper", "George", "Evelyn", "Henry", "Abigail", "Francis", "Elizabeth", "Daniel", "Victoria", "Anthony", "Grace", "Thomas", "Chloe", "Christopher", "Scarlett", "Paul", "Charlotte", "Mark", "Penelope", "Donald", "Violet", "Matthew", "Camila", "Stephen", "Layla", "Andrew", "Lucy", "Justin", "Luna", "Jonathan", "Zoe", "Peter", "Stella", "Kevin", "Claire", "Ryan", "Maya", "Brian", "Piper", "Jason", "Rose", "Eric", "Alice", "Adam", "Nova", "Nicholas", "Daisy", "Sean", "Julia", "Gregory", "Caroline", "Corey", "Valentina", "Louis", "Esme", "Timothy", "Genevieve", "Jack", "Skylar", "Benjamin", "Paisley", "Alexander", "Madelyn", "Brandon", "Selena", "Jeremy", "Blake", "Tyler", "Levi", "Logan", "Hudson", "Ethan", "Atticus", "Owen", "Maxwell", "Noah", "Theodore", "Samuel", "Asher", "Caleb", "Leo", "Ezra", "Silas", "Wyatt", "Grayson", "Lincoln", "Ian", "Easton", "Micah", "Atticus", "Finnegan", "Axel", "Xavier", "Beckett", "Callum", "Corbin", "Declan", "Ellis", "Flynn", "Grant", "Hayden", "Holden", "Jude", "Keaton", "Leon", "Luca", "Marcus", "Matteo", "Rhys", "Ryder", "Tristan", "Weston", "Zeus"};
                              
    
  double x_random=0;
    double y_random=0;
    double z_random=0;
    for(int i = 0; i != kolvo; ++i){
        int randoma, randomA, randoMA, randOMA;
        int last = 100;
        int first=0;
        int lasT = 5;
        int firsT = 0;
        int laST = 5;
        int firST = 0;
        int lAST = 5;
        int fiRST = 0;
        randoma = rand() % (last - first + 1) + first;//рандомайзер на имя , фамилию
        randomA = rand() % (lasT - firsT + 1) + firsT;//рандомайзер на 1 значения (---> 1 <--- 2 3)
        randoMA = rand() % (laST - firST + 1) + firST;//рандомайзер на 1 значения (1 ---> 2 <--- 3)
        randOMA = rand() % (lAST - fiRST + 1) + fiRST;//рандомайзер на 1 значения (1 2 ---> 3 <---)
        x_random = x_random + randomA;
        y_random = y_random + randoMA;
        z_random = z_random + randOMA;
        
        
  cout << Surname[randoma] << " " << Name[randoma] << " " <<randomA << " " << randoMA << " " << randOMA << " " <<  endl;
        
        
  }
    cout << std::setprecision(2);//сводим все value к одному знаку после запятой
    cout<< " 1) mid_value = " << x_random/kolvo<<" 2) mid value = "<<y_random/kolvo << " 3) mid value = "<<z_random/kolvo;
}
