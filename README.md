#include <iostream>
using namespace std;

#include <unordered_map>

#include <string>
int main(){
    unordered_map<string,int> m;
    //insert
    pair<string,int> p("abc",1);
    m.insert(p);
    pair<string,int> p1("def",2);
    m.insert(p1);
    m["ghi"]=3;
    //find
    cout<<m["abc"]<<endl;
    cout<<"size :"<<m.size()<<endl;
    cout<<m.at("def")<<endl;
    cout<<m["jkl"]<<endl;
    //checking
    if(m.count("jkl")>0){
        cout<<"it   is present"<<endl;
    }
    //deletion
    m.erase("ghi");
    cout<<"size:"<<m.size()<<endl;
    m["abc"]=5;
    cout<<m["abc"]<<endl;

}
