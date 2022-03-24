#include<iostream>
#include<conio.h>
using namespace std;
int main();
class Hitung{
	friend ostream& operator<<(ostream&, const Hitung&);
	friend istream& operator>>(istream&, Hitung&);
public:
	Hitung();
	void hitung_jumlahnya(){jumlah=(a+b+c);}
private:
	int a,b,c;
	int jumlah;
};
Hitung::Hitung(){
	cout<<"program menghitung 3 integer\n";
	cout<<"selamat berkarya\n";
}
istream& operator>>(istream& in, Hitung& masukan){
	cout<<" Masukan nilai a :";
	cin>>masukan.a;
	cout<<"masukan nilai b :";
	cin>>masukan.b;
	cout<<"masukan nilai c :";
	cin>>masukan.c;
	
	return in;
	
}

ostream& operator<<(ostream& out, const Hitung& keluaran){
	cout<<" nilai a :"<<keluaran.a<<endl;
	cout<<" nilai b :"<<keluaran.b<<endl;
	cout<<" nilai c :"<<keluaran.c<<endl;
	cout<<"jumlah 3 integer di atas :"<<keluaran.jumlah<<endl;
	return out;
	

}

int main(){
	Hitung X;
	cin>>X;
	X.hitung_jumlahnya();
	cout<<X;
	getch();
	return 0;
}
