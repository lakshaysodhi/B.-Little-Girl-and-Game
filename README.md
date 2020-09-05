# B.-Little-Girl-and-Game
#include <bits/stdc++.h>
using namespace std;

int main()
{

    unordered_map<char,int> frequency;
    string S;
    cin>>S;
    for(int i=0;i<S.size();i++){
        frequency[S[i]]++;
    }
    int odd=0,even=0;
    for(auto i=frequency.begin();i!=frequency.end();i++){
        if((i->second)%2==0) even++;
        else odd++;
        }
        //if string length is odd first will always win because he is starting the game but if length is even then second will win because both are intelligent
        // they both don't allow each other to win but the first can win in the case if at the time of staring the string can be sorted as a palindrome 
        //it can happen in two ways weather all words have even frequency in fact this case have even string length still first win and 
        //second case is if 1 char have odd frequency and rest all have even like abcdddcba here also first win but it is having odd string length as well so first is going
        // to win this anyway.
    if(odd==0) cout<<"First";
    else if(S.size()%2==0) cout<<"Second";
    else cout<<"First";

}
