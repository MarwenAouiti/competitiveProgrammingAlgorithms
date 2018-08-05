#include <bits/stdc++.h>
/**
    backtrakingAlgorithms(Permute a string)
    Pseudocode :
            fonction permute(s):
                if s is an empty string :
                    nothing to do
                else :
                    foreach character in s :
                        choose c to be first
                        permute the rest of s
                        un-choose c
**/
using namespace std;

void permute(string s);
void combin(string s, int len);
int main()
{
    permute("Google");
    return 0;
}

void permuteHelper(string s , string chosen,set<string>& alreadyPrinted) {
    cout<<"permuteHelper (\""<<s<<"\",\""<<chosen<<"\")"<<endl;
    /**
        File I/O
    **/

    if(s.empty()) {
            const bool is_in = alreadyPrinted.find(chosen) != alreadyPrinted.end();
            if(!(is_in))
            {
                cout<<chosen<<endl;
                alreadyPrinted.insert(chosen);
            }
    } else {
        for(int i=0;i<(int)s.length();i++) {

            /** choose */
            char c = s[i];
            chosen += c;
            s.erase(i,1);

            /**Explore*/
            permuteHelper(s,chosen,alreadyPrinted);

            /*** un-choose */
            s.insert(i,1,c);
            chosen.erase(chosen.length()-1,1);
        }
    }

}
void permute(string s) {
    set<string> chosen;
    permuteHelper(s, "",chosen);
}

