#include<bits/stdc++.h>
using namespace std;
int optimizedseclarg(vector<int>& arr) {
    int n=arr.size();
    int lar=arr[0];
    int seclar=INT_MIN;
    for(int i=1;i<n;i++){
        if (arr[i]>lar){
            seclar=lar;
            lar=arr[i];
            
        }
        else{
            if(arr[i]<lar){
                if(arr[i]>seclar){
                    seclar=arr[i];
            }
        }
    }
}return seclar,lar;
}

int main(){
    int arr[]={1,4,6,8,3,5};
    int lar=optimizedseclarg(arr);
    int seclar=optimizedseclarg(arr);
    cout<<"second largest element is"<<seclar<<endl;
    cout<<"largest element is"<<lar<<endl;
}
