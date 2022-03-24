#include <iostream>
#include <conio.h>

using namespace std;
int main(){
	char x,nama[30];
	string jenis;
	int liter,total, bayar, kembali,pertamax,pertalite;
	
	cout<<"============TRANSAKSI SPBU============"<<endl;
	cout<<"Masukan Nama pelanggan :";
	cin.getline(nama,sizeof(nama));
	cout<<"Silahkan Pilih Jenis Transaksi"<<endl;
	cout<<"1. pertalite";
	cout<<endl;
    cout<<"2. Pertamax";
  	cout<<endl;
	cout<<"Masukkan Pilihan Anda (1/2) = ";
	cin>>x;
	cout<<endl;

	if (x=='1'){
		jenis="pertalite";

		cout<<"Harga pertalite Perliter : 7000"<<endl;
		cout<<"Jumlah Liter          : ";cin>>liter;
		cout<<"Masukkan Uang Bayar   : ";cin>>bayar;	
		pertalite=7000;
		total=pertalite*liter;
		kembali=bayar-total;
		
	}
	
	else if (x=='2'){
		jenis="pertamax";
	
		cout<<"Harga Pertamax Perliter : 9000"<<endl;
		cout<<"Jumlah Liter            : ";
		cin>>liter;
		cout<<"Masukkan Uang Bayar     : ";
		cin>>bayar;
		
		pertamax=9000;
		total=pertamax*liter;
		kembali=bayar-total;
	}
	cout<<endl;
	cout<<"==========STRUK==============\n"<<endl;
	
	cout<<"Nama pelanggan\t\t\t:"<<nama<<endl;
	cout<<"Total Liter\t\t\t:"<<liter<<endl;
	cout<<"jenis bensin\t\t\t:"<<jenis<<endl;
	cout<<"Total Bayar\t\t\t:"<<total<<endl;
	cout<<"Uang Kembali\t\t\t:"<<kembali<<endl<<endl;
	
}
