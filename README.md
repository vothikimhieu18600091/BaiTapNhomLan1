# BaiTapNhomLan1
Bài tập nhóm lần 1
#in ra nguyên tố , mà nguyên tố đó <100
#include<iostream>
#define MAX 100
using namespace std;
void nhapmang(int a[], int n) {
	for (int i =0 ; i < n; i++) {
		cout << "\nnhap a["<<i << "]=";
		cin >> a[i];
	}
}
void xuatmang(int a[], int n) {
	for (int i = 0; i < n; i++) {
		cout << a[i] << " ";
	}
}

int kiemtra(int n) {
	int dem = 0;
	if (n < 2)
	{
		cout << "\nkhong co so nguyen to";
	}
	if (n >= 2) {
		for (int i = 1; i <= n; i++) {
			if (n%i == 0) {
				dem++;
			}
		}
		if (dem == 2) {
			return 1;
		}
		else {
			return 0;
		}
	}
}
void nguyeton(int a[], int n) {
	for (int i = 0; i < n; i++) {
		if (kiemtra(a[i]) == 1 && a[i] < 100)
		{
			cout << a[i] << "  ";
		}
	}
}
int tongam(int a[], int n) {
	int tong = 0;
	for (int i = 0; i < n; i++) {
		if (a[i] < 0) {
			tong += a[i];
		}
	}
	return tong;
}
void main(){
	int a[MAX], n;
	do{
		cout << "\nNhap vao so phan tu cua mang : ";
		cin >> n;
		if (n < 0 || n >100) {
			cout << "\Vui long kiem tra lai";
		}
	} while (n <0 || n > 100);
	nhapmang(a, n);
	xuatmang(a, n);
	nguyeton(a, n);
	cout << "\ns=" << tongam(a, n);
		system("pause");
	}
