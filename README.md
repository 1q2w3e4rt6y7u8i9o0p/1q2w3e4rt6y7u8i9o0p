#include<bits/stdc++.h>
using namespace std;
void hanoi(int n,char qi,char zhon,char mu){
	if(n==0){
		return;
	}
	hanoi(n-1,qi,mu,zhon);
	printf("%c->%d->%c\n",qi,n,mu);
	hanoi(n-1,zhon,qi,mu);
}
int main(){
	int n;
	char a,b,c;
	cin>>n>>a>>b>>c;
	hanoi(n,a,c,b);
	return 0;
}
