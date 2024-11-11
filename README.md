# Operating-Hours-Checker
This C++ program displays operating hours based on a chosen day (1-5). Using a switch statement, it shows hours from 8:00 to 17:00 on days 1 and 5, and from 8:00 to 14:00 on days 2, 3, and 4. An invalid input results in "Closed." The user can check another day or exit the program.

    #include <iostream>
    using namespace std;
    
    int main()
    {
        int day;
        char choice = 'Y';

    while (choice == 'Y' || choice == 'y')
    {
        cout << "Choose a Day from 1 to 5: ";
        cin >> day;

        switch (day)
        {
        case 1:
            cout << "Open from 8:00 to 17:00\n";
            break;
        case 2:
        case 3:
        case 4:
            cout << "Open from 8:00 to 14:00\n";
            break;
        case 5:
            cout << "Open from 8:00 to 17:00\n";
            break;
        default:
            cout << "Closed\n";
            break;
        }

        cout << "Would you like to check another day? (Enter Y for Yes or N for No): "<<"\n";
        cin >> choice;
    }

    return 0;
    }
